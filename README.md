**# Employee-Performance-and-Bonus-Evaluation-System**
##CODING##
CREATE TABLE EMPLOYEE (
employee_id INT PRIMARY KEY,
first_name VARCHAR(30) NOT NULL,
last_name VARCHAR(30) NOT NULL,
email VARCHAR(50),
department VARCHAR(20),
salary NUMERIC(10,2),
joining_date DATE,
age INT
);
SELECT * FROM EMPLOYEE
 ----homework
 ---Question1. Calculate the Annual Salary and Salary Increment by 5% - show the monthly new salary as well
 SELECT FIRST_NAME, SALARY,
 (SALARY*12) AS ANNUAL_SALARY,
 (SALARY*0.5) AS SALARY_INCREMENT,
 (SALARY+SALARY*0.5) AS NEW_MONTHLY_SALARY
 FROM EMPLOYEE;
---Question2.. Retrieve the first_name, salary, and calculate a 10% bonus on the salary
SELECT FIRST_NAME, SALARY,
 (SALARY*0.1) AS BONUS FROM EMPLOYEE;
 ---Write a query to find employees whose age is exactly 30.
 SELECT FIRST_NAME,AGE FROM EMPLOYEE WHERE AGE IN ('30');
 ---Retrieve all employees whose age is not 25.
  SELECT FIRST_NAME,AGE FROM EMPLOYEE WHERE AGE NOT IN ('25');
 ---Find all employees whose age is above 40.
 SELECT FIRST_NAME,AGE FROM EMPLOYEE WHERE AGE > 40;
 ---Find all employees whose salary is more than 70,000.
 SELECT FIRST_NAME,AGE, SALARY FROM EMPLOYEE WHERE SALARY > 70000; 
---List all employees whose age is below 30. & Find employees whose salary is less than 40,000.
  SELECT FIRST_NAME,AGE, SALARY FROM EMPLOYEE WHERE AGE < 30 AND
  SALARY < 40000;
   SELECT FIRST_NAME,AGE, SALARY FROM EMPLOYEE WHERE AGE < 30 OR SALARY < 40000;
---Greater than or equal to (>=)
--Show employees whose age is 35 or older & Show employees whose salary is at least 60,000.
 SELECT FIRST_NAME,AGE, SALARY FROM EMPLOYEE WHERE AGE >= 35 AND SALARY =60000;
 SELECT FIRST_NAME,AGE, SALARY FROM EMPLOYEE WHERE AGE >= 35 OR SALARY =60000; 
---6. Less than or equal to (<=)
--Display all employees whose salary is 50,000 or less.
 SELECT FIRST_NAME,AGE, SALARY FROM EMPLOYEE WHERE SALARY <= 50000;
--Display all employees whose age is 28 or below.
SELECT FIRST_NAME,AGE, SALARY FROM EMPLOYEE WHERE AGE <= 28;
---7. AND
--Find employees whose age is greater than 25 AND salary is greater than 50,000.
 SELECT FIRST_NAME,AGE, SALARY FROM EMPLOYEE WHERE AGE > 25 AND SALARY >50000;
--Retrieve employees who are in the 'IT' department AND earn more than 70,000.
 SELECT FIRST_NAME,AGE, SALARY, DEPARTMENT FROM EMPLOYEE WHERE DEPARTMENT IN  ('IT') AND SALARY >70000;
---8. OR
--Find employees whose age is less than 25 OR salary is less than 40,000.
 SELECT FIRST_NAME,AGE, SALARY FROM EMPLOYEE WHERE AGE < 25 OR SALARY <40000;
--Show employees who are in 'HR' OR 'Finance' department.
SELECT FIRST_NAME,DEPARTMENT FROM EMPLOYEE WHERE DEPARTMENT = 'HR' OR DEPARTMENT='FINANCE';
---9. NOT
--Show all employees NOT in the 'IT' department.
SELECT FIRST_NAME,DEPARTMENT FROM EMPLOYEE WHERE DEPARTMENT NOT IN ('IT') ;
--List employees whose age is NOT 30.
SELECT FIRST_NAME,AGE FROM EMPLOYEE WHERE AGE NOT IN ('30');
 
