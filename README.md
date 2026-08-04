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
