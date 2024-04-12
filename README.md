# Database-week-6
SQL Queries
-- Step 1: Create a new MySQL database named "UniversityDB"
CREATE DATABASE UniversityDB;

-- Step 2: Design a table named "Students" with the specified attributes
CREATE TABLE Students (
    StudentID INT PRIMARY KEY,
    FirstName VARCHAR(50),
    LastName VARCHAR(50),
    Age INT,
    Major VARCHAR(50)
);

-- Step 3: Insert at least 5 records into the "Students" table with sample data
INSERT INTO Students (StudentID, FirstName, LastName, Age, Major) VALUES
(1, 'John', 'Doe', 20, 'Computer Science'),
(2, 'Jane', 'Smith', 22, 'Biology'),
(3, 'Michael', 'Johnson', 21, 'Mathematics'),
(4, 'Emily', 'Davis', 19, 'English'),
(5, 'David', 'Brown', 23, 'History');

-- Step 4: Alter the "Students" table to add a new column named "GPA"
ALTER TABLE Students
ADD GPA DECIMAL(3, 2);

-- Step 5: Insert GPA values for the existing records in the "Students" table
UPDATE Students
SET GPA = 3.5
WHERE StudentID IN (1, 2, 3, 4, 5);

-- Step 6: Rename the table from "Students" to "EnrolledStudents"
ALTER TABLE Students
RENAME TO EnrolledStudents;

-- Step 7: Create a new table named "Courses" with the specified attributes
CREATE TABLE Courses (
    CourseID INT PRIMARY KEY,
    CourseName VARCHAR(100),
    Instructor VARCHAR(100),
    Credits INT
);

-- Step 8: Insert at least 3 records into the "Courses" table with sample data
INSERT INTO Courses (CourseID, CourseName, Instructor, Credits) VALUES
(1, 'Introduction to Computer Science', 'Dr. Smith', 3),
(2, 'Biology 101', 'Prof. Johnson', 4),
(3, 'Calculus I', 'Dr. Brown', 4);

-- Step 9: Drop the "EnrolledStudents" table from the database
DROP TABLE EnrolledStudents;

