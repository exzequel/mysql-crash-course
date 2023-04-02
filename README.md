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

