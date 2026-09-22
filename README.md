# 🗄️ Database Systems Lab Portfolio

### MySQL • SQL • Database Design • Normalization • Joins • Functions • DBMS Project

## 📌 About This Repository

Welcome to my **Database Systems Lab Repository**, a comprehensive collection of SQL laboratory exercises, database design tasks, normalization exercises, query-based assessments, and an Open-Ended Lab project developed as part of my Database Systems coursework.

This repository documents my practical journey through relational database concepts using **MySQL**, beginning with database software setup and fundamental SQL operations and progressing toward database normalization, filtering, joins, SQL functions, aggregate functions, and the implementation of a complete **CarGo Rentals Database Management System**.

The repository focuses on connecting database theory with practical SQL implementation by creating databases, designing relational tables, applying constraints, manipulating records, writing queries, and building relationships between entities.

> **From creating the first database table to designing a complete relational DBMS — this repository represents my practical exploration of Database Systems and SQL.**

# 🎯 Repository Objectives

The main objectives of this repository are to:

* Understand the fundamentals of Database Management Systems.
* Learn how relational databases are structured.
* Create and manage databases using MySQL.
* Design tables using appropriate primary and foreign keys.
* Understand candidate, alternate, composite, natural, and surrogate keys.
* Perform CRUD operations using SQL.
* Modify database structures using `ALTER TABLE`.
* Understand `TRUNCATE` and `DROP` operations.
* Apply database normalization from **1NF to 3NF**.
* Identify functional dependencies and database anomalies.
* Write filtering queries using SQL conditions.
* Work with `INNER JOIN`, `LEFT JOIN`, and `RIGHT JOIN`.
* Understand multi-table relationships.
* Use string, numeric, date, and aggregate functions.
* Create views, triggers, and stored procedures.
* Apply database optimization concepts.
* Design and implement a practical DBMS project.

# 🧰 Tools & Technologies

| Tool / Technology             | Purpose                                         |
| ----------------------------- | ----------------------------------------------- |
| **MySQL 8.x**                 | Relational database management system           |
| **MySQL Workbench**           | Database development and SQL execution          |
| **MySQL Command Line Client** | Command-line SQL execution                      |
| **XAMPP**                     | Local development environment / MySQL setup     |
| **SQL**                       | Database definition, manipulation, and querying |
| **Relational Database Model** | Database organization and relationships         |

# 🧪 Laboratory Work

The repository contains practical work progressing from database setup and fundamentals toward advanced SQL and DBMS implementation.

## 📘 Lab 01 — XAMPP Software Installation

### Focus: Database Development Environment Setup

The first laboratory introduces the software environment required for database development.

### Main Activities

* Installing **XAMPP**.
* Setting up the local development environment.
* Understanding the role of Apache and MySQL within XAMPP.
* Starting and stopping required services.
* Preparing the system for local database development.

### Concepts Covered

* XAMPP environment
* Local server environment
* MySQL service
* Database development setup

---

# 📘 Lab 02 — Point of Sale Database

### Focus: Introduction to Database Design and SQL

The second laboratory introduces database concepts through a **Point of Sale (POS) database**.

The exercise focuses on representing a real-world business scenario through relational database structures.

### Concepts Covered

* Database creation
* Table creation
* Entity-based database design
* Relational data
* Primary keys
* Foreign keys
* Basic SQL operations
* Business-oriented database modeling

> The POS database provides an early practical example of how real-world operations can be represented using relational tables.

---

# 📘 Lab 03 — Database Keys, Table Commands & CRUD Operations

### Focus: Relational Keys, Table Management and Data Manipulation

This laboratory uses a **University Database** containing departments, students, courses, instructors, and enrollments.

### Database Structure

```text
Department
    │
    ├── Students
    │
    ├── Courses
    │
    └── Instructors

Students ─── Enrollments ─── Courses
```

### Key Concepts

The lab explores several types of database keys:

* Primary Key
* Foreign Key
* Unique Key
* Composite Key
* Candidate Key
* Alternate Key
* Natural Key
* Surrogate Key
* Super Key

### SQL Operations

The laboratory demonstrates:

```sql
CREATE
ALTER
INSERT
SELECT
UPDATE
DELETE
TRUNCATE
DROP
```

### Practical Tasks

1. Create relational tables with constraints.
2. Insert sample records.
3. Retrieve records using `SELECT`.
4. Update student information.
5. Delete records while respecting foreign-key relationships.
6. Demonstrate `TRUNCATE` and `DROP`.
7. Add columns using `ALTER TABLE`.
8. Perform joins between students and courses.
9. Demonstrate different types of database keys.

---

# 📘 Lab 04 — Database Normalization: Online Bookstore

### Focus: 1NF → 2NF → 3NF

This laboratory applies normalization concepts to an **Online Bookstore** scenario.

The exercise begins with an unnormalized order relation and progressively transforms it into a better structured relational design.

### Functional Dependencies

The exercise identifies dependencies such as:

```text
OrderID → OrderDate, CustID
CustID → CustName, CustEmail
BookID → BookTitle, Publisher, UnitPrice
(OrderID, BookID) → Qty
```

### Normalization Stages

#### 1NF — First Normal Form

The raw order data is transformed so that:

* Values are atomic.
* Repeating groups are removed.
* Each order-book combination can be uniquely identified.

#### 2NF — Second Normal Form

Partial dependencies are removed by separating information related to:

* Orders
* Books
* Order lines

#### 3NF — Third Normal Form

Transitive dependencies are removed by separating entities such as:

* Customers
* Orders
* Books
* Order Lines

### Anomalies Studied

* Insertion anomaly
* Update anomaly
* Deletion anomaly

### Main Learning Outcome

The laboratory demonstrates how normalization can reduce redundancy and improve database consistency.

---

# 📘 Lab 05 — Database Normalization: Hospital Database

### Focus: Healthcare Database Normalization

This laboratory applies normalization concepts to a **Hospital Database**.

The database is progressively organized using:

```text
1NF
 ↓
2NF
 ↓
3NF
```

### Main Entities

The normalized design includes entities such as:

* Patient
* Department
* Doctor
* Visit

### Concepts Covered

* Functional dependencies
* Composite keys
* Partial dependencies
* Transitive dependencies
* Database anomalies
* 1NF
* 2NF
* 3NF
* Relational decomposition

This exercise demonstrates how a healthcare scenario can be transformed from a flat structure into a more organized relational database.

---

# 📘 Lab 06 — SQL Filtering

### Focus: Filtering Data Using SQL Conditions

This laboratory introduces SQL filtering techniques using an Employee database.

### Concepts Covered

* `WHERE`
* Comparison operators
* Logical conditions
* Filtering records
* Sorting
* `LIKE`
* `IN`
* `BETWEEN`
* `IS NULL`
* `AND`
* `OR`
* `ORDER BY`

The lab provides practical experience retrieving only the records that satisfy specific conditions.

---

# 📘 Lab 07 — SQL Filtering Assessment: Book Database

### Focus: Advanced Filtering and Query Conditions

This assessment uses a bookstore database containing information such as:

* Book title
* Author
* Genre
* Price
* Stock
* Published year
* Publisher
* Language

### Example Query Requirements

The assessment includes queries for:

* Books above a specific price.
* Books published within a year range.
* Books belonging to selected genres.
* Titles containing specific text.
* Titles beginning or ending with specific characters.
* Books with missing authors.
* Out-of-stock books.
* Books with missing publishers.
* Most expensive books currently in stock.
* Urdu books sorted by publication year.
* Books satisfying multiple conditions.

### SQL Techniques

```sql
WHERE
BETWEEN
IN
LIKE
IS NULL
AND
OR
ORDER BY
LIMIT
```

---

# 📘 Lab 08 — SQL Joins: Company Database

### Focus: Multi-Table Relational Queries

This laboratory works with a Company database containing:

```text
Department
Employee
Project
Assignment
```

### Join Concepts

The laboratory demonstrates:

* `INNER JOIN`
* `LEFT JOIN`
* `RIGHT JOIN`
* Self joins
* Multi-table joins
* Join conditions
* `NULL` handling
* `GROUP BY`
* `HAVING`
* `UNION`

### Example Relationships

```text
Department
    │
    ├── Employee
    │      │
    │      └── Manager
    │
    └── Project
           │
           └── Assignment
```

### Practical Queries

The exercises include queries for:

* Employees and their departments.
* Departments with or without employees.
* Employees and their managers.
* Employees earning more than managers.
* Employees working on projects.
* Project assignments.
* Employees working on specific projects.
* Employees from specific cities.
* Cross-department project relationships.

---

# 📘 Lab 09 — SQL Joins: Library Database

### Focus: Relational Queries Using Multiple Tables

This laboratory uses a Library database containing:

```text
Author
Book
Member
Loan
```

### Practical Join Exercises

The laboratory includes queries to:

* Display books with their authors.
* Display authors with their books.
* Find members who have never borrowed books.
* Display complete loan information.
* Find currently borrowed books.
* Display Pakistani authors and their books.
* Find books and their borrowers.
* Find authors whose books have never been borrowed.
* Emulate a `FULL OUTER JOIN` using `UNION`.
* Find members who borrowed books written by Pakistani authors.

### Important SQL Concepts

```sql
INNER JOIN
LEFT JOIN
RIGHT JOIN
UNION
GROUP BY
HAVING
IS NULL
DISTINCT
```

---

# 📘 Lab 10 — SQL String Functions

### Focus: String Manipulation and Data Cleaning

This laboratory uses Customer and Product tables to explore MySQL string functions.

### Functions Covered

```sql
TRIM()
UPPER()
LOWER()
CHAR_LENGTH()
CONCAT()
SUBSTRING()
LOCATE()
LEFT()
REPLACE()
LPAD()
```

### Practical Applications

The exercises include:

* Removing unwanted spaces.
* Converting names to uppercase and lowercase.
* Calculating string length.
* Generating greeting messages.
* Extracting usernames from email addresses.
* Extracting email domains.
* Extracting the first characters of names.
* Masking phone numbers.
* Creating product slugs.
* Padding product IDs.
* Locating text within product names.
* Extracting first names.

### Example

```sql
SELECT
    TRIM(CustName) AS CleanedName,
    UPPER(CustName) AS UpperName
FROM Customer;
```

---

# 📘 Lab 11 — Numeric & Date Functions

### Focus: Scalar, Numeric and Date-Based SQL Functions

This laboratory works with an Employee database and demonstrates SQL functions for manipulating employee information.

### String Operations

Examples include:

```sql
TRIM()
UPPER()
LOWER()
SUBSTRING()
CONCAT()
REPLACE()
```

### Numeric Functions

The exercises include:

```sql
ROUND()
FLOOR()
```

For example, employee salaries can be increased by a specified percentage and rounded to two decimal places.

### Date Functions

The laboratory also explores:

```sql
TIMESTAMPDIFF()
DATE_FORMAT()
YEAR()
```

### Practical Tasks

* Clean employee names.
* Extract email usernames.
* Mask phone numbers.
* Generate corporate email addresses.
* Calculate salary increases.
* Round salaries down to the nearest thousand.
* Calculate employee age.
* Calculate years of service.
* Format hiring dates.
* Find employees hired after a specified year.
* Build combined employee profile information.

---

# 📘 Lab 12 — Aggregate Functions

### Focus: Data Summarization and Group-Based Analysis

This laboratory focuses on **SQL aggregate functions**, which allow multiple rows to be summarized into meaningful results.

### Main Aggregate Functions

```sql
COUNT()
SUM()
AVG()
MIN()
MAX()
```

### Concepts Covered

* Counting records.
* Calculating totals.
* Finding averages.
* Finding minimum values.
* Finding maximum values.
* Grouping records.
* Filtering grouped results.

### Related SQL Concepts

```sql
GROUP BY
HAVING
ORDER BY
```

### Example

```sql
SELECT Department, AVG(Salary) AS AverageSalary
FROM Employee
GROUP BY Department;
```

Aggregate functions are essential for converting raw database records into useful statistical and business information.

---

# 🚗 Lab 13 — Open-Ended Lab: CarGo Rentals DBMS

## Focus: Complete Database Management System

The Open-Ended Lab brings together many of the concepts studied throughout the course into a practical **CarGo Rentals Database Management System**.

The project creates a database named:

```text
CarGoRentals
```

---

## 🏗️ Core Database Tables

The primary database design contains:

```text
Customers
Vehicles
Rentals
Payments
```

### Customers

Stores customer-related information.

### Vehicles

Stores vehicle information and rental-related details.

### Rentals

Connects customers with rented vehicles and stores rental information.

### Payments

Stores payment-related information associated with rentals.

---

# 🔄 OEL Normalization

The project also demonstrates database normalization from:

```text
UNF
 ↓
1NF
 ↓
2NF
 ↓
3NF
```

The SQL implementation includes demonstration structures such as:

```text
RentalRaw_UNF
Demo_Customer_2NF
Demo_Vehicle_2NF
Demo_Rental_2NF
Demo_Rental_3NF
Demo_Payment_3NF
```

This makes the OEL more than simply a database implementation — it also demonstrates the application of normalization principles to a realistic business scenario.

---

# 🔗 OEL Join Queries

The project includes relational queries involving customers, vehicles, and rentals.

Examples include:

* Customer names with vehicle numbers and models.
* Rental and return dates.
* All customers and the vehicles they rented.
* Vehicles with current rental information.
* Customers with no rental records.
* Total rentals made by each customer.

These queries demonstrate how multiple relational tables can be combined to answer practical business questions.

---

# 👁️ Database View

The CarGo Rentals project also implements a **database VIEW**.

Views provide a way of presenting selected information from one or more tables through a reusable query-based interface.

---

# ⚙️ Database Triggers

The OEL includes **database triggers** to demonstrate automated database actions based on specified events.

Triggers allow the database to respond automatically when particular operations occur.

---

# 📦 Stored Procedure

The project also implements a **stored procedure**, demonstrating how reusable SQL logic can be stored and executed directly inside the database.

---

# 🚀 Optimization Analysis

The final section of the OEL demonstrates basic **SQL optimization analysis**, connecting database implementation with performance considerations.

---

# 📊 Database Concepts Covered

Across the complete repository, the following Database Systems concepts are represented:

### Database Fundamentals

* DBMS
* Relational databases
* Tables
* Records
* Attributes
* Relationships
* Constraints

### Keys

* Primary Key
* Foreign Key
* Candidate Key
* Alternate Key
* Composite Key
* Super Key
* Natural Key
* Surrogate Key
* Unique Key

### SQL Data Definition

```sql
CREATE DATABASE
CREATE TABLE
ALTER TABLE
DROP TABLE
TRUNCATE TABLE
```

### SQL Data Manipulation

```sql
INSERT
SELECT
UPDATE
DELETE
```

### Querying

* `WHERE`
* `ORDER BY`
* `LIMIT`
* `DISTINCT`
* `LIKE`
* `IN`
* `BETWEEN`
* `IS NULL`

### Joins

* Inner Join
* Left Join
* Right Join
* Self Join
* Multi-table Join
* Full Outer Join emulation using `UNION`

### Normalization

```text
UNF
1NF
2NF
3NF
```

### SQL Functions

#### String

```text
TRIM
UPPER
LOWER
CONCAT
SUBSTRING
LOCATE
LEFT
REPLACE
LPAD
CHAR_LENGTH
```

#### Numeric

```text
ROUND
FLOOR
SUM
AVG
MIN
MAX
COUNT
```

#### Date

```text
YEAR
DATE_FORMAT
TIMESTAMPDIFF
```

### Advanced Database Features

* Views
* Triggers
* Stored Procedures
* Foreign-key constraints
* Referential integrity
* SQL optimization concepts

---

# 📁 Repository Structure

A recommended structure for the GitHub repository is:

```text
Database-Systems/
│
├── README.md
│
├── Lab 01 - XAMPP Installation/
│
├── Lab 02 - Point of Sale Database/
│
├── Lab 03 - Database Keys & CRUD/
│   ├── README.md
│   └── RollNo_Lab_DatabaseKeys_CRUD.sql
│
├── Lab 04 - Normalization Bookstore/
│   └── RollNo_Normalization_LabTasks.sql
│
├── Lab 05 - Normalization Hospital/
│   └── RollNo_Normalization_Assessment.sql
│
├── Lab 06 - SQL Filters/
│   └── RollNo_Filters.sql
│
├── Lab 07 - SQL Filters Assessment/
│   └── RollNo_Filters.sql
│
├── Lab 08 - SQL Joins Company/
│   └── RollNo_Lab8_Joins.sql
│
├── Lab 09 - SQL Joins Library/
│   └── RollNo_Lab9_Joins.sql
│
├── Lab 10 - String Functions/
│   └── RollNo_Lab10_StringFunctions.sql
│
├── Lab 11 - Numeric & Date Functions/
│   ├── RollNo_Lab11_NumericDateFunctions.sql
│   └── RollNo_Lab11_Assessment_EmployeeDB.sql
│
├── Lab 12 - Aggregate Functions/
│   └── Aggregate_Functions.sql
│
└── Lab 13 - OEL/
    ├── CarGo_Rentals_DBMS.sql
    └── CarGo_Rentals_Lab_Report.docx
```

---

# 📚 Laboratory Progression

The repository follows a progressive learning path:

```text
XAMPP Installation
        ↓
Point of Sale Database
        ↓
Database Keys & CRUD
        ↓
Normalization
        ↓
SQL Filtering
        ↓
SQL Joins
        ↓
String Functions
        ↓
Numeric & Date Functions
        ↓
Aggregate Functions
        ↓
Advanced DBMS Features
        ↓
CarGo Rentals DBMS
```

This progression moves from **database environment setup and basic relational concepts** toward **advanced SQL and complete database system implementation**.

---

# 🎓 Learning Outcomes

After completing these practical exercises, I developed hands-on experience with:

1. Setting up a local MySQL database environment.
2. Creating and managing relational databases.
3. Designing tables with appropriate constraints.
4. Identifying different types of database keys.
5. Performing CRUD operations.
6. Modifying database structures.
7. Understanding referential integrity.
8. Identifying functional dependencies.
9. Applying 1NF, 2NF, and 3NF.
10. Identifying insertion, update, and deletion anomalies.
11. Writing filtering queries.
12. Combining data using different types of joins.
13. Working with SQL string functions.
14. Performing numeric calculations using SQL.
15. Working with date and time functions.
16. Summarizing data using aggregate functions.
17. Using `GROUP BY` and `HAVING`.
18. Creating database views.
19. Implementing triggers.
20. Creating stored procedures.
21. Considering SQL optimization.
22. Designing and implementing a complete relational DBMS.

---

# 💡 Why This Repository Matters

Rather than containing only isolated SQL queries, this repository demonstrates the development of database skills across multiple stages.

The labs move from:

**"How do I create and manipulate data?"**

to:

**"How do I organize data correctly?"**

and eventually to:

**"How do I design and implement a complete database system?"**

The **CarGo Rentals DBMS** serves as the practical culmination of these concepts by combining database design, normalization, relationships, joins, views, triggers, stored procedures, and optimization analysis in a single project.

# 🚀 Future Improvements

Possible future extensions to this repository include:

* Adding ER diagrams for major database projects.
* Adding relational schema diagrams.
* Including SQL output screenshots.
* Adding sample datasets separately from query scripts.
* Adding more advanced subqueries.
* Adding Common Table Expressions (CTEs).
* Adding window functions.
* Adding indexing experiments.
* Adding query execution-plan analysis.
* Adding transaction and concurrency examples.
* Adding database backup and restore exercises.
* Connecting the CarGo Rentals database to a frontend application.
* Building a complete CRUD application around the CarGo Rentals DBMS.

# 🎓 Academic Context

**Course:** Database Systems
**Program:** Software Engineering
**Database System:** MySQL
**Primary Language:** SQL
**Development Environment:** XAMPP / MySQL Workbench / MySQL Command Line Client
**Repository Type:** Academic Laboratory Portfolio
**Open-Ended Project:** CarGo Rentals DBMS
