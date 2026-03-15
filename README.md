# 📚 Library Management Database

## 🔎 Project Overview
This project demonstrates the design and querying of a Library Management Database using SQL.  
It simulates how libraries manage books, members, and borrowing activities. It covers:
Database creation, Schema design, Data insertion, Retrieval queries, Analytical insights using MySQL  

## ❓ Problem Project Statement
Libraries manage large collections of books and must track which members borrow them and when they are returned.  
Without a structured database, it becomes difficult to:

- Track available books  
- Monitor borrowed books  
- Identify overdue loans  
- Manage member records  

This project builds a relational database system to solve these problems using SQL.

## 🛠 Tools Used
-  Editor: MySQL Workbench  
- Database: MySQL  
- Data Source: Google Sheet (CSV)  

## 🗂 Database Schema Design
The database **`library_db`** contains three main tables:

### Books Table: Stores information about books in the library.
 
### Members Table: Stores information about registered library members. 

### Loans Table: Tracks book borrowing activities.

### The raw data used for this project can be found in the data folder.

📊 Key Query Performed
. Filtering data: Find books published after 2015.
. using logical operations to Count number of books available.
. sorting and pagination for data reporting 
View all books

SELECT * FROM books;

View registered members

SELECT member_id, first_name, last_name FROM members;

Find loans on a specific date

SELECT loan_id, book_id, member_id 
FROM loans 
WHERE borrow_date = '2026-03-07';

Books with more than 3 copies available

SELECT book_id, title, author, copies_available 
FROM books 
WHERE copies_available > 3;

Books published after 2015

SELECT book_id, title, author, publication_year 
FROM books 
WHERE publication_year > 2015;

Members who joined before 2022
sql
SELECT member_id, first_name, last_name, membership_date 
FROM members 
WHERE membership_date < '2022-01-01';

Loans not yet returned
sql
SELECT loan_id, book_id, member_id, borrow_date, due_date 
FROM loans 
WHERE return_date IS NULL;

✨ Features
Track book availability
Manage member records
Monitor overdue loans
Generate analytical insights with SQL queries

✅ Conclusion
This project demonstrates core SQL skills including:
Database creation
Schema design
Data insertion
Filtering & sorting
Analytical queries
