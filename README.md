# Introduction to Database

A database is an organized collection of related data that allows users to store, retrieve, update, and manage information efficiently. Databases are widely used in organizations to maintain records such as employee details, salaries, attendance, and leave information.

A Database Management System (DBMS) is software that enables users to interact with the database. When data is stored in tables with relationships between them, it is called a Relational Database Management System (RDBMS). Examples include MySQL, PostgreSQL, Oracle, and SQL Server.

Your SQL file represents an HR (Human Resources) Management Database, which is designed to manage employee-related information. Instead of maintaining records manually, the HR department can use this database to store and retrieve employee data quickly and accurately.

# Database Structure

The HR database consists of the following tables:

Table Name	Description
employees	Stores employee information such as Employee ID, Name, Department, Position, Salary, Date of Joining, Contact Number, and Email.
attendance	Maintains employees' daily attendance records including attendance date and attendance status (Present/Absent).
payroll	Stores salary payment information such as basic salary, allowances, deductions, net salary, and payment date.
leave_requests	Records employee leave applications, including leave type, start date, end date, reason, and approval status.
Relationships Between Tables

The database uses Employee ID as the primary identifier to connect different tables.

The employees table is the main table.
The attendance table references employees through Employee ID.
The payroll table stores salary details for each employee using Employee ID.
The leave_requests table stores leave records linked to Employee ID.

This relationship helps eliminate duplicate data and maintains data consistency.

# Purpose of the HR Database

The HR database is developed to:

Store employee information securely.
Track daily attendance.
Manage payroll and salary processing.
Handle employee leave requests.
Generate reports for management.
Reduce manual paperwork and improve efficiency.
Advantages of the Database
Centralized data storage
Faster data retrieval
Reduced data redundancy
Improved data accuracy
Better security through controlled access
Easy report generation
Efficient employee management
Technologies Used
Database: MySQL
Query Language: SQL (Structured Query Language)
Sample Operations

# Using SQL, users can perform operations such as:

View all employees.
Search employees by department.
Calculate total salary expenses.
Check employee attendance.
Display approved leave requests.
Generate payroll reports.

# What is a DBMS?
DBMS stands for Database Management System.

It is software that acts as an intermediary between you (the user or an application) and the actual database (the stored data). It allows you to create, retrieve, update, and manage data in a structured and efficient way.

Think of it like a digital filing cabinet:

The data is the actual files and documents.

The DBMS is the system of drawers, folders, labels, and a search mechanism that lets you find any file instantly, add new ones, or reorganize everything without making a mess.

# A DBMS allows you to:

Store data in structured tables

SQL is the standard language used to interact with databases. We use SQL to:

Query (Read) data from tables.

Insert (Create) new data.

Update (Modify) existing data.

Delete (Remove) data.

# Example :
	SELECT * FROM employees;
Example using SELECT Retrieve all employee data.

<img width="1002" height="400" alt="image" src="https://github.com/user-attachments/assets/ea62f129-ece1-4336-8fdc-a44d7b01207a" />

# What is RDBMS?

RDBMS stands for Relational Database Management System.

It is a type of DBMS that stores data in tables (relations) with rows and columns, and links these tables using relationships.

Feature	Explanation:

Tables - Data is organized in rows and columns

Keys - PRIMARY KEY uniquely identifies each row; FOREIGN KEY links tables

<img width="335" height="235" alt="Screenshot 2026-08-05 114340" src="https://github.com/user-attachments/assets/d217897f-dc90-4302-b691-ad4835bb0484" />

# SQL Commands - Complete Classification

SQL commands are divided into 5 main categories based on their functionality:

# 1. DDL - Data Definition Language

Used to define or modify database structure.

Command	Purpose	Example:

CREATE	Create database or table	CREATE TABLE employees (...);

ALTER	Modify table structure	ALTER TABLE employees ADD email VARCHAR(50);

DROP	Delete database or table	DROP TABLE employees;

TRUNCATE	Remove all rows from table	TRUNCATE TABLE employees;

RENAME	Rename database object	RENAME TABLE emp TO employees;

# 2. DML - Data Manipulation Language:

(Used to manage data inside tables)

Command	Purpose	Example:

SELECT	Retrieve data	SELECT * FROM employees;

INSERT	Add new rows	INSERT INTO employees VALUES (1, 'John', ...);

UPDATE	Modify existing rows	UPDATE employees SET salary = 50000 WHERE id = 1;

DELETE	Remove rows	DELETE FROM employees WHERE id = 1;

# 3. DCL - Data Control Language:

Used to control permissions and access.

Command	Purpose	Example:

GRANT	Give permissions	GRANT SELECT ON employees TO user1;

REVOKE	Take back permissions	REVOKE SELECT ON employees FROM user1;

# 4. TCL - Transaction Control Language

Used to manage transactions

Command	Purpose	Example:

COMMIT	Save all changes permanently	COMMIT;

ROLLBACK	Undo changes since last commit	ROLLBACK;

SAVEPOINT	Set a point to rollback to	SAVEPOINT sp1;

SET TRANSACTION	Set transaction properties	SET TRANSACTION READ ONLY;

# 5. DQL - Data Query Language:

Used only for querying data - often considered part of DML

Command	Purpose	Example:

SELECT	Query data	SELECT first_name, salary FROM employees;

# Quick Reference Table

Category	Commands	Purpose

DDL	CREATE, ALTER, DROP, TRUNCATE, RENAME	Define/Modify structure

DML	SELECT, INSERT, UPDATE, DELETE	Manage data

DCL	GRANT, REVOKE	Manage permissions

TCL	COMMIT, ROLLBACK, SAVEPOINT	Manage transactions

DQL	SELECT	Query data
