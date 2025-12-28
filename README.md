
# 📚 Library Management System 

---

## **Project Overview**

The **Library Management System** is a database-driven project designed to manage books, authors, members, and borrowing transactions in a library.
This project uses **MySQL** to store and manipulate data and demonstrates the practical use of **SQL concepts** such as CRUD operations, joins, subqueries, aggregate functions, window functions, and constraints.

---

## **Objective**

* To manage library data efficiently using a relational database.
* To track book availability and borrowing history.
* To understand and apply core SQL concepts in a real-world scenario.
* To maintain data integrity using primary and foreign keys.

---

## **Database Schema**

The database consists of **four main tables**:

1. **Authors**
2. **Books**
3. **Members**
4. **Transactions**

Relationships:

* Each **Book** is linked to an **Author**.
* Each **Transaction** links a **Member** with a **Book**.
* Foreign key constraints ensure referential integrity.
* `ON DELETE CASCADE` is used to automatically delete transactions when a member is removed.

---

## **Table Description**

### **1. Authors Table**

| Column Name | Description                             |
| ----------- | --------------------------------------- |
| author_id   | Unique ID for each author (Primary Key) |
| name        | Author name                             |
| email       | Author email address                    |

---

### **2. Books Table**

| Column Name      | Description                           |
| ---------------- | ------------------------------------- |
| book_id          | Unique ID for each book (Primary Key) |
| title            | Book title                            |
| author_id        | References Authors table              |
| category         | Book category                         |
| isbn             | Unique ISBN number                    |
| published_date   | Date of publication                   |
| price            | Book price                            |
| available_copies | Number of copies available            |

---

### **3. Members Table**

| Column Name     | Description                             |
| --------------- | --------------------------------------- |
| member_id       | Unique ID for each member (Primary Key) |
| name            | Member name                             |
| email           | Member email                            |
| phone_number    | Contact number                          |
| membership_date | Date of registration                    |

---

### **4. Transactions Table**

| Column Name    | Description                         |
| -------------- | ----------------------------------- |
| transaction_id | Unique transaction ID (Primary Key) |
| member_id      | References Members table            |
| book_id        | References Books table              |
| borrow_date    | Book borrowing date                 |
| return_date    | Book return date                    |
| fine_amount    | Fine charged (if any)               |

---

## **SQL Operations Covered**

* **CRUD Operations** (INSERT, SELECT, UPDATE, DELETE)
* **Filtering** using WHERE, AND, OR, NOT
* **Sorting & Grouping** using ORDER BY and GROUP BY
* **Aggregate Functions** (COUNT, SUM, AVG, MAX, MIN)
* **Subqueries**
* **Joins** (INNER, LEFT, RIGHT)
* **Window Functions** (RANK, cumulative count)
* **CASE Expressions**
* **Date & Time Functions**
* **String Functions**
* **Primary & Foreign Key Constraints**

---

## **Queries Implemented**

* Insert new authors, books, and members.
* Update book availability on borrow and return.
* Delete inactive members using foreign key cascade.
* Retrieve available books.
* Filter books by category, price, and publication year.
* Sort books alphabetically.
* Count books borrowed by each member.
* Find the most borrowed book.
* Calculate total fines collected.
* Use subqueries to find inactive members.
* Rank books based on borrowing frequency.
* Assign membership status using CASE expressions.
* Categorize books as New Arrival, Classic, or Regular.
* Format dates and manipulate strings.

---

## **Conclusion**

The **Library Management System** successfully demonstrates how SQL can be used to design, manage, and query a relational database.
This project provides hands-on experience with real-world database operations and ensures data accuracy using constraints and relationships.
It is suitable for academic learning and can be extended into a full-scale library application.


