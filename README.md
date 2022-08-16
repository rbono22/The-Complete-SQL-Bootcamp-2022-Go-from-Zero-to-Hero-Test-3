# The-Complete-SQL-Bootcamp-2022-Go-from-Zero-to-Hero-Test-3

## Create a new database called "School" this database should have two tables: teachers and students.

To create the database in PGAdmin 4 simply right-click on the databases drop down menu and select "New Database".

## The students table should have columns for student_id, first_name,last_name, homeroom_number, phone,email, and graduation year.
To create the students table:<br>

CREATE TABLE students(<br>
student_id serial PRIMARY KEY,<br>
first_name VARCHAR(45) NOT NULL,<br>
last_name VARCHAR(45) NOT NULL, <br>
homeroom_number integer,<br>
phone VARCHAR(20) UNIQUE NOT NULL,<br>
email VARCHAR(115) UNIQUE,<br>
grad_year integer);

## The teachers table should have columns for teacher_id, first_name, last_name, homeroom_number, department, email, and phone.
To create the teachers table:<br>

CREATE TABLE teachers(<br>
teacher_id serial PRIMARY KEY,<br>
first_name VARCHAR(45) NOT NULL,<br>
last_name VARCHAR(45) NOT NULL, <br>
homeroom_number integer,<br>
department VARCHAR(45),<br>
email VARCHAR(20) UNIQUE,<br>
phone VARCHAR(20) UNIQUE);

## Once you've made the tables, insert a student named Mark Watney (student_id=1) who has a phone number of 777-555-1234 and doesn't have an email. He graduates in 2035 and has 5 as a homeroom number.
Then for inserting the student information: <br>

INSERT INTO students(first_name,last_name, homeroom_number,phone,grad_year)VALUES ('Mark','Watney',5,'7755551234',2035);

## Then insert a teacher names Jonas Salk (teacher_id = 1) who as a homeroom number of 5 and is from the Biology department. His contact info is: jsalk@school.org and a phone number of 777-555-4321.
Then for inserting the teacher information:<br>

INSERT INTO teachers(first_name,last_name, homeroom_number,department,email,phone)VALUES ('Jonas','Salk',5,'Biology','jsalk@school.org','7755554321');
