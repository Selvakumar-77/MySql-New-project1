"# MySql-New-project1" 
# 📚 University Library Management System (MySQL)

A complete **University Library Management System** built using **MySQL**, demonstrating database design, data manipulation, constraints, joins, subqueries, views, indexes, and stored procedures.

This project is ideal for **DBMS coursework, lab exams, mini-projects, and interviews**.

---

## 🛠️ Technologies Used
- **Database:** MySQL
- **Language:** SQL
- **Tools:** MySQL Workbench / Command Line

---

## 🗂️ Database Overview

**Database Name:** `universitylibrary`

### Tables
1. **Book**
2. **Member**
3. **Issue_Records / Book_Issue_Records**

Each table includes proper:
- Primary Keys
- Foreign Keys
- Constraints
- Date fields

---

## 📘 Table Structure

### 📖 Book Table
Stores book-related information.
- `book_id` (PK)
- `title`
- `author`
- `genre`
- `price`
- `publication_year`
- `isbn` (Unique)
- `is_available`
- `added_date`

---

### 👤 Member Table
Stores library member details.
- `member_id` (PK)
- `member_name`
- `department`
- `email` (Unique)
- `contact_number`
- `membership_date`
- `is_active`
- `address`

---

### 🔄 Issue_Records Table
Tracks issued and returned books.
- `issue_id` (PK)
- `book_id` (FK)
- `member_id` (FK)
- `issue_date`
- `return_date`
- `status`

---

## 📥 Sample Data
- ✔ 10+ records inserted into each table
- ✔ Realistic sample data for testing queries

---

## ✏️ SQL Operations Covered

### 🔹 DDL (Data Definition Language)
- `CREATE DATABASE`
- `CREATE TABLE`
- `ALTER TABLE`
- `RENAME TABLE`
- `ADD CONSTRAINT`
- `CREATE VIEW`
- `CREATE INDEX`

---

### 🔹 DML (Data Manipulation Language)
- `INSERT`
- `UPDATE`
- `SELECT`
- `DELETE`

---

### 🔹 SQL Operators Used
- `AND`
- `OR`
- `NOT`
- `IN`
- `BETWEEN`
- `LIKE`
- `IS NOT NULL`
- `IFNULL`

---

## 🔗 Joins Implemented
- ✅ INNER JOIN
- ✅ LEFT JOIN
- ✅ FULL OUTER JOIN (using `UNION`)

---

## 📊 Aggregate Functions
- `COUNT()`
- `SUM()`
- `AVG()`
- `MIN()`
- `MAX()`
- Used with `GROUP BY` and `HAVING`

---

## 🔁 Subqueries
- Single-row subquery
- Multi-row subquery
- Correlated subquery
- Subquery inside `UPDATE`

---

## 📅 Date & Numeric Functions
- `CURDATE()`
- `DATE_SUB()`
- `MONTH()`
- `YEAR()`
- `ROUND()`

---

## 👁️ Views Created
- `Currently_Issued_Books`
- `Active_Members`

---

## ⚡ Indexes
- Index on `book_id` (Issue_Records)
- Index on `title` (Book)

---

## 🔄 Stored Procedures

### 1️⃣ IssueBook
Issues a book if available.

### 2️⃣ ReturnBook
Returns a book and updates availability.

### 3️⃣ ListCurrentlyIssuedBooks
Displays all currently issued books.

---

## ▶️ How to Run the Project

1. Open **MySQL Workbench**
2. Copy the SQL file
3. Execute step-by-step OR run the entire script
4. Use:
```sql
CALL ListCurrentlyIssuedBooks();
