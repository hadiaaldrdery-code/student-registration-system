# student-registration-system

# Assignment III: SQL Table Manipulation

## Project Overview
**Project:** Student Registration System  
**DBMS:** MySQL 8.0 or later  
**Student name:** Replace with your full name  
**Student ID:** Replace with your student ID  

This project demonstrates how to create a relational database, create related tables, insert records, retrieve data, join tables, update records, and alter table structures.

> **Before submission:** Replace the example database name with the required format `yourname_studentid_projectname`. Run the SQL file in MySQL and add screenshots of your actual results. The ERD must be generated from your actual database application and saved as `erd.png`.

## Database and Tables

### 1. `departments`
- `department_id`: automatically generated primary key.
- `department_name`: department name; required.
- `location`: department location.

### 2. `students`
- `student_id`: automatically generated primary key.
- `student_name` (renamed to `full_name` in Q4.1): student's name.
- `email`: student's email; must be unique when supplied.
- `age`: student's age.
- `phone` (added in Q4.3): student's phone number.

### 3. `registrations`
- `registration_id`: automatically generated primary key.
- `student_id`: foreign key referencing `students(student_id)`.
- `department_id`: foreign key referencing `departments(department_id)`.
- `registration_date`: date of registration.

## Relationships
- One student can have registration records in `registrations`.
- Each registration references one existing student.
- Each registration references one existing department.
- The foreign keys protect referential integrity by preventing registrations from referring to nonexistent students or departments.

## How to Run
1. Install and open MySQL 8.0+ (for example, using MySQL Workbench).
2. Open `assignment_iii.sql`.
3. Replace the database name with your required name and student ID.
4. Execute the statements from top to bottom in a fresh database.
5. Check the results of each `SELECT`, `UPDATE`, `ALTER TABLE`, and `INSERT` operation.
6. Save screenshots of actual query output and successful changes in this repository.
7. Generate the ERD from MySQL Workbench (`Database → Reverse Engineer`) and export it as `erd.png`.
8. Add the generated `erd.png` to this repository.

## Practical Tasks Included
- **Q1.1–Q1.3:** SELECT — selected columns, conditions, and sorting.
- **Q2.1–Q2.3:** JOIN — INNER JOIN, LEFT JOIN, and multi-table JOIN.
- **Q3.1–Q3.3:** UPDATE — one record, multiple records, and conditional update.
- **Q4.1–Q4.3:** ALTER TABLE — rename a column, change a column definition, and add a column.
- **Q5.1–Q5.3:** INSERT — one record, multiple records, and a related record.

## Important Notes
- This repository is a starter project. SQL output screenshots and `erd.png` must come from your own actual execution; they are not fabricated here.
- Run the file in a new/empty database to avoid duplicate records or unexpected auto-generated IDs.
- Q5.3 uses student ID `6`, which should be Fatima's ID in a fresh database when the statements are run in order. Verify with `SELECT student_id, full_name FROM students;` before executing it.
- Read and understand each statement because the assignment includes a class discussion and quiz.

## Conclusion
This project provides practice in creating relational tables, using primary and foreign keys, inserting and retrieving records, joining related tables, safely updating data, and changing table structures with `ALTER TABLE`.
