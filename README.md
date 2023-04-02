# MySQL Full Course (Bro Code) Notes

## MySQL INTRO & Installation

Structured - Query - Language

SQL is used to create, retrieve, update, and delete data

**RELATIONAL VS NON-RELATIONAL DATA BASES**

### RELATIONAL

Tables resemble an excel sheet
"Keys"

Uses SQL

### NON-RELATIONAL

Data is organized in any format but tables

NoSQL

## DBMS

DATABASE MANAGEMENT SYSTEM

Workspace to write SQL statements

**MySQL**, Microsoft SQL Server, Oracle, PostgreSQL

## INSTALLATION

Head to the downloads tab of [mysql.com](mysql.com)
Click MySQL Community downloads
Find installer for Windows

Or just download from this link:
[Download](https://dev.mysql.com/downloads/installer/)

Open the installer
Select Custom install
Install only the latest version of the MySQL Server and Workbench

Keep Configuration settings as default, for the mean time
When the MySQL Workbench pops up you're done

## DATABASES

WHAT IS A DATABASE

- LIKE A FOLDER, ACTS AS A CONTAINER
- TABLES ARE THE FILES OF THE CONTAINER

```mySQL

// creating a database (not case sensitive, but recommended to use CAPITAL letters)
CREATE DATABASE databaseName;

// set current database to default
USE databaseName;

// drop or remove a database
DROP DATABASE databaseName;

// set database to read only mode (cannot modify)
ALTER DATABASE myDB READ ONLY = 1;

// disable read only mode
ALTER DATABASE myDB READ ONLY = 0;

```

## TABLES

(IN A RELATIONAL DATABASE)
CONSISTS OF ROWS AND COLUMNS

```mySQL

// create a table
// each column is separated by a comma (,)
// declare the data type after the name of each value
CREATE TABLE employees (
	employee_id INT,
    first_name VARCHAR(50),
    last_name VARCHAR(50),
    hourly_pay DECIMAL(5, 2),
    hire_date DATE
);

// to select a table
SELECT * FROM employees;

// to rename a table
RENAME TABLE originalName TO newName;
RENAME TABLE employees TO workers;

// to drop a table
DROP TABLE nameOfTable;
DROP TABLE employees;

// to alter a table
ALTER TABLE employees
ADD phone_number VARCHAR(15);

// to alter a column from a table
ALTER TABLE employees
RENAME COLUMN phone_number to email;

// modify a data type from column
ALTER TABLE employees
MODIFY COLUMN email VARCHAR(100);

// to move position of a column
ALTER TABLE employees
MODIFY email VARCHAR(100)
AFTER last_name;

// if you need a column to be first
ALTER TABLE employees
MODIFY email VARCHAR(100)
FIRST;

// to drop a column
ALTER TABLE employees
DROP COLUMN email;

```

## INSERT ROWS

```MySQL

// to insert rows or values into columns
// NOTE: follow the format of the columns when adding rows (data types, and position)
// COLUMN REFERENCE: employee_id, first_name, last_name, hourly_pay, hire_date
INSERT INTO employees
VALUES (1, "Eugene", "Krabs", 25.50, "2023-01-02");

// to insert multiple rows or values into columns
// NOTE: each row must be in a parentheses () and separated by a comma ,
INSERT INTO employees
VALUES (2, "Squidward", "Tentacles", 15.00, "2023-01-23"),
	(3, "Spongebob", "Squarepants", 12.50, "2023-01-04"),
	(4, "Patrick", "Star", 12.50, "2023-01-05"),
	(5, "Sandy", "Cheeks", 17.25, "2023-01-06");

// inserting data with incomplete values
INSERT INTO employees (employee_id, first_name, last_name)
VALUES (6, "Sheldon", "Plankton");

```
