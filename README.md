# dbms
Create the following tables with the mapping given below  book ( book-name, author, price, quantity) customer (cust_id, cust-name, Adder, ph-no,  pan-no)
--CODE
CREATE TABLE book (
    book_name VARCHAR(255) PRIMARY KEY,
    author VARCHAR(255),
    price DECIMAL(10, 2),
    quantity INT
);

CREATE TABLE customer (
    cust_id INT PRIMARY KEY AUTO_INCREMENT,
    cust_name VARCHAR(255),
    address VARCHAR(255),
    ph_no VARCHAR(20),
    pan_no VARCHAR(10) UNIQUE
);
--Example For Insert into

INSERT INTO book (book_name, author, price, quantity) VALUES
('The Lord of the Rings', 'J.R.R. Tolkien', 29.99, 100),
('Pride and Prejudice', 'Jane Austen', 19.99, 50);

INSERT INTO customer (cust_name, address, ph_no, pan_no) VALUES
('John Doe', '123 Main St', '555-1234', 'ABCDE1234F'),
('Jane Smith', '456 Oak Ave', '555-5678', 'FGHIJ5678K');


Practical No:10(A)
AIM: Advanced SQL queries using PL-SQL.
Solve the following PL-SQL programs.
A) Write a pl/sql program to swap two numbers.
Code:
DECLARE
@num1 INT = 10,
@num2 INT = 20,
@temp INT;
PRINT 'Original Numbers: num1 = ' + CAST(@num1 AS VARCHAR) + ', num2 = ' +
CAST(@num2 AS VARCHAR);
-- Swap the numbers using a temporary variable
SET @temp = @num1;
SET @num1 = @num2;
SET @num2 = @temp;
-- Display the swapped numbers
PRINT 'Swapped Numbers: num1 = ' + CAST(@num1 AS VARCHAR) + ', num2 = ' +
CAST(@num2 AS VARCHAR);


PRACTICAL No 10(B)
B) Write a pl/sql program to find the largest of two numbers.
Code:
DECLARE
@num1 INT = 10, -- Replace with your first number
@num2 INT = 20, -- Replace with your second number
@result INT;
-- Compare the two numbers and store the larger one in the result variable
IF @num1 > @num2
SET @result = @num1;
ELSE
SET @result = @num2;
-- Display the result
PRINT 'The largest number is: ' + CAST(@result AS VARCHAR);

Practical No:11
AIM: Advanced SQL queries usingPROCEDURE AND FUNCTION
A]Write syntax of Procedure and Function.
B] Create a procedure to print the odd numbers from 1 to 10.
Code:
-- T-SQL Equivalent for SQL Server
DECLARE @i INT = 1;
WHILE @i <= 10
BEGIN
IF @i % 2 <> 0
PRINT @i;
SET @i = @i + 1;
END;
