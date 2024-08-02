TO CREATE TABLES FOR ADMIN, CONSUMER, ELECTRICITY BILL, AND EMPLOYEES 
 
1. Admin Table: 
CREATE TABLE Admin ( admin_id INT PRIMARY KEY, username VARCHAR(50) NOT NULL, password 
VARCHAR(50) NOT NULL, contact_no VARCHAR(15), email VARCHAR(100) );  
2. Consumer Table: 
CREATE TABLE Consumer ( consumer_id INT PRIMARY KEY, name VARCHAR(100) NOT NULL, communication 
VARCHAR(100), address VARCHAR(200), payment DECIMAL(10, 2), feedback TEXT );  
3. Electricity Bill Table: 
CREATE TABLE ElectricityBill ( bill_id INT PRIMARY KEY, consumer_id INT, type ENUM('Domestic', 
'Commercial'), FOREIGN KEY (consumer_id) REFERENCES Consumer (consumer_id) );  
4. Employees Table: 
CREATE TABLE Employees ( employee_id INT PRIMARY KEY, employee_name VARCHAR(100) NOT NULL, 
consumer_data TEXT ); 
TO INSERT VALUES INTO THESE TABLES 
1. Inserting values into Admin table: 
INSERT INTO Admin (admin_id, username, password, contact_no, email) VALUES (1, 'admin123', 
'adminpass', '1234567890', 'admin@example.com');  
2. Inserting values into Consumer table: 
INSERT INTO Consumer (consumer_id, name, communication, address, payment, feedback) VALUES (1, 'John 
Doe', 'Phone', '123 Main St, City', 100.00, 'Great service!');  
3. Inserting values into Electricity Bill table: 
INSERT INTO ElectricityBill (bill_id, consumer_id, type) VALUES (1, 1, 'Domestic');  
4. Inserting values into Employees table: 
INSERT INTO Employees (employee_id, employee_name, consumer_data) VALUES (1, 'Employee 1', 
'Consumer data here');  
TO DISPLAY THE DATA FROM THE TABLES 
 
Displaying all records from the Admin table:  
SELECT * FROM Admin;  
Displaying all records from the Consumer table: 
SELECT * FROM Consumer;  
 
Displaying all records from the Electricity Bill table: 
SELECT * FROM ElectricityBill;  
 
Displaying all records from the Employees table: 
SELECT * FROM Employees;  
SOME EXAMPLE QUERIES FOR PERFORMING NECESSARY OPERATIONS 
 
1. Update Admin's contact number: 
UPDATE Admin SET contact_no = '5555555555' WHERE admin_id = 1;  
 
2. Update Consumer's payment amount: 
UPDATE Consumer SET payment = 180.00 WHERE consumer_id = 2;  
 
3. Update Employee's name: 
UPDATE Employees SET employee_name = 'New Employee Name' WHERE employee_id = 3;  
 
4. Retrieve all Consumers who have given feedback: 
SELECT * FROM Consumer WHERE feedback IS NOT NULL;  
 
5. Retrieve all Domestic Electricity Bills: 
SELECT * FROM ElectricityBill WHERE type = 'Domestic';  
 
6. Retrieve the total payment received from all Consumers: 
SELECT SUM(payment) AS total_payment FROM Consumer;  
SELECT c.*, e.employee_name FROM Consumer c INNER JOIN Employees e ON c.consumer_id = 
e.employee_id;  
 
8. Retrieve the Consumer with the highest payment: 
SELECT * FROM Consumer ORDER BY payment DESC LIMIT 1;  
 
9. Retrieve the average payment amount for Commercial Electricity Bills: 
SELECT AVG(payment) AS average_payment FROM Consumer WHERE consumer_id IN ( SELECT consumer_id 
FROM ElectricityBill WHERE type = 'Commercial' );  
 
10. Retrieve the total number of Consumers: 
SELECT COUNT(*) AS total_consumers FROM Consumer;  
 
11. Retrieve the Employee who handles the maximum number of Consumers: 
SELECT e.employee_id, e.employee_name, COUNT(c.consumer_id) AS consumer_count FROM Employees e 
JOIN Consumer c ON e.employee_id = c.employee_id GROUP BY e.employee_id, e.employee_name ORDER 
BY consumer_count DESC LIMIT 1;  
 
12. Retrieve the Consumers whose payment is overdue (payment greater than a specific threshold): 
SELECT * FROM Consumer WHERE payment > 100.00;  
 
13. Retrieve the Admin's email and the total number of Consumers assigned to each Admin: 
SELECT a.email, COUNT(c.consumer_id) AS consumer_count FROM Admin a JOIN Employees e ON 
a.admin_id = e.admin_id JOIN Consumer c ON e.employee_id = c.employee_id GROUP BY a.email;  
 
14. Retrieve the Consumers who have not provided feedback: 
SELECT * FROM Consumer WHERE feedback IS NULL;  
 
These queries demonstrate different scenarios and logic that can be applied to retrieve specific information 
from the tables. You can modify these queries or combine them with other conditions to suit your specific 
requirements in the Electricity Bill Management system.
