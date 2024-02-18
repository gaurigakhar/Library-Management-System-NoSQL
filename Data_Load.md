#### MongoDB Script to generate (create/insert/update): 
- Exactly 20 books check-outs for exactly 10 different borrowers and exactly 10 different books. Same borrower should not check out same book more than once
- Exactly 10 of the above checkouts should have returned the book

db.Book_Copies.updateOne({$and:[{book_id:'0226743497'},{branch_id:1}]},{$set:{"book_loans":[{"borrower_id":'ID000499',"checkin_date":ISODate("2022-12-10T12:10:05Z"),"checkout_date":ISODate("2022-12-06T12:10:05Z"),"due_date":ISODate("2022-12-20T12:10:05Z")},{"borrower_id":'ID000002',"checkin_date":ISODate("2022-09-06T12:10:05Z"),"checkout_date":ISODate("2022-04-12T12:10:05Z"),"due_date":ISODate("2022-05-29T12:10:05Z")}]}})

db.Book_Copies.updateOne({$and:[{book_id:'0345293711'},{branch_id:1}]},{$set:{"book_loans":[{"borrower_id":'ID000227',"checkin_date":ISODate("2022-12-10T12:10:05Z"),"checkout_date":ISODate("2022-11-06T12:10:05Z"),"due_date":ISODate("2022-11-20T12:10:05Z")},{"borrower_id":'ID000219',"checkin_date":ISODate("2022-10-06T12:10:05Z"),"checkout_date":ISODate("2022-09-12T12:10:05Z"),"due_date":ISODate("2022-10-29T12:10:05Z")}]}})

db.Book_Copies.updateOne({$and:[{book_id:'3404121686'},{branch_id:1}]},{$set:{"book_loans":[{"borrower_id":'ID000379',"checkin_date":ISODate("2022-11-10T12:10:05Z"),"checkout_date":ISODate("2022-11-06T12:10:05Z"),"due_date":ISODate("2022-11 20T12:10:05Z")},{"borrower_id":'ID000103',"checkin_date":ISODate("2022-09-06T12:10:05Z"),"checkout_date":ISODate("2022-09-01T12:10:05Z"),"due_date":ISODate("2022-09-29T12:10:05Z")}]}})

db.Book_Copies.updateOne({$and:[{book_id:'0915811642'},{branch_id:1}]},{$set:{"book_loans":[{"borrower_id":'ID000636',"checkin_date":ISODate("2022-06-10T12:10:05Z"),"checkout_date":ISODate("2022-06-06T12:10:05Z"),"due_date":ISODate("2022-06-02T12:10:05Z")},{"borrower_id":'ID000574',"checkin_date":ISODate("2022-05-06T12:10:05Z"),"checkout_date":ISODate("2022-05-04T12:10:05Z"),"due_date":ISODate("2022-05-12T12:10:05Z")}]}})

db.Book_Copies.updateOne({$and:[{book_id:'0312312261'},{branch_id:1}]},{$set:{"book_loans":[{"borrower_id":'ID000762',"checkin_date":ISODate("2022-01-10T12:10:05Z"),"checkout_date":ISODate("2022-01-06T12:10:05Z"),"due_date":ISODate("2022-01-20T12:10:05Z")},{"borrower_id":'ID000318',"checkin_date":ISODate("2022-01-19T12:10:05Z"),"checkout_date":ISODate("2022-01-12T12:10:05Z"),"due_date":ISODate("2022-01-09T12:10:05Z")}]}})

db.Book_Copies.updateOne({$and:[{book_id:'0192815466'},{branch_id:1}]},{$set:{"book_loans":[{"borrower_id":'ID000318',"checkin_date":ISODate("2022-08-15T12:10:05Z"),"checkout_date":ISODate("2022-08-06T12:10:05Z"),"due_date":ISODate("2022-08-10T12:10:05Z")},{"borrower_id":'ID000762',"checkin_date":ISODate("2022-08-16T12:10:05Z"),"checkout_date":ISODate("2022-08-01T12:10:05Z"),"due_date":ISODate("2022-08-11T12:10:05Z")}]}})

db.Book_Copies.updateOne({$and:[{book_id:'0881848581'},{branch_id:1}]},{$set:{"book_loans":[{"borrower_id":'ID000574',"checkin_date":ISODate("2022-04-10T12:10:05Z"),"checkout_date":ISODate("2022-04-06T12:10:05Z"),"due_date":ISODate("2022-04-15T12:10:05Z")},{"borrower_id":'ID000636',"checkin_date":ISODate("2022-04-06T12:10:05Z"),"checkout_date":ISODate("2022-04-01T12:10:05Z"),"due_date":ISODate("2022-04-11T12:10:05Z")}]}})

db.Book_Copies.updateOne({$and:[{book_id:'0771020139'},{branch_id:1}]},{$set:{"book_loans":[{"borrower_id":'ID000103',"checkin_date":ISODate("2022-03-21T12:10:05Z"),"checkout_date":ISODate("2022-03-06T12:10:05Z"),"due_date":ISODate("2022-03-20T12:10:05Z")},{"borrower_id":'ID000379',"checkin_date":ISODate("2022-03-06T12:10:05Z"),"checkout_date":ISODate("2022-02-12T12:10:05Z"),"due_date":ISODate("2022-03-29T12:10:05Z")}]}})

db.Book_Copies.updateOne({$and:[{book_id:'0060974494'},{branch_id:1}]},{$set:{"book_loans":[{"borrower_id":'ID000219',"checkin_date":ISODate("2022-01-10T12:10:05Z"),"checkout_date":ISODate("2022-01-06T12:10:05Z"),"due_date":ISODate("2022-01-20T12:10:05Z")},{"borrower_id":'ID000227',"checkin_date":ISODate("2022-02-06T12:10:05Z"),"checkout_date":ISODate("2022-02-01T12:10:05Z"),"due_date":ISODate("2022-02-29T12:10:05Z")}]}})

db.Book_Copies.updateOne({$and:[{book_id:'1551668971'},{branch_id:1}]},{$set:{"book_loans":[{"borrower_id":'ID000002',"checkin_date":ISODate("2022-02-10T12:10:05Z"),"checkout_date":ISODate("2022-02-06T12:10:05Z"),"due_date":ISODate("2022-02-20T12:10:05Z")},{"borrower_id":'ID000499',"checkin_date":ISODate("2022-03-06T12:10:05Z"),"checkout_date":ISODate("2022-03-01T12:10:05Z"),"due_date":ISODate("2022-03-05T12:10:05Z")}]}})

db.Book_Copies.find({$and:[{book_id:{$in:['0226743497','0345293711','3404121686','0915811642','0312312261','0192815466','0881848581','0771020139','0060974494','1551668971']}},{"branch_id":1}]})
