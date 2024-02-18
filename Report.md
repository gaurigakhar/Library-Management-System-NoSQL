#### Book Search with Branch id = 1, Title and Authors name containing “Will”
db.Books.aggregate([{$lookup:{from: "Book_Copies", localField:"ISBN10", foreignField:"book_id", "as":"tmp_bc"}}, {$unwind: "$tmp_bc"}, {$match: {$or: [{"tmp_bc.branch_id" : 1},{"Title" : {$regex:/Will/}},{"Authors_arr" : {$regex:/Will/}}]}}, {$project: {"tmp_bc.branch_id" : 1, "Availibility_Status" : {$cond:{if:{$gte:["$tmp_bc.no_of_copies",1]}, then: "Book is available", else: "Book is not available"}}, "Title":1, "Authors_arr":1}}])

#### Book Search with Branch id = 5, Title and Authors name containing “Will”
db.Books.aggregate([{$lookup:{from: "Book_Copies", localField:"ISBN10", foreignField:"book_id", "as":"tmp_bc"}}, {$unwind: "$tmp_bc"}, {$match: {$or: [{"tmp_bc.branch_id" : 5},{"Title" : {$regex:/""/}},{"Authors_arr" : {$regex:/Will/}}]}}, {$project: {"tmp_bc.branch_id" : 1, "Availibility_Status" : {$cond:{if:{$gte:["$tmp_bc.no_of_copies",1]}, then: "Book is available", else: "Book is not available"}}, "Title":1, "Authors_arr":1}}])

#### Number of books (book copies) per library branch.
db.Book_Copies.aggregate([{$group:{_id:'$branch_id',count:{$sum:'$no_of_copies'}}}])

#### Book copies that were returned back late. Include all Book and Book copy attributes, including checkout and check-in attributes. You will need to "join" (lookup) two documents. 
db.Book_Copies.aggregate([{$match:{"book_loans":{$exists:true}}},{$lookup:{from:"Books",localField:"book_id",foreignField:"ISBN10",as:"book_details"}},{$unwind:"$book_loans"},{$match:{$expr:{$gt:["$book_loans.checkin_date","$book_loans.due_date"]}}}])

#### 10 books that don't have author attribute populated
db.Books.find({Authors_arr: null}).limit(10).pretty()
