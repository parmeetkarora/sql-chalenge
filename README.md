# sql-chalenge
Pewlett Hackard Company
Data Visualization Module 9 Challenge
Background
It’s been two weeks since you were hired as a new data engineer at Pewlett Hackard (a fictional company). Your first major task is to do a research project about people whom the company employed during the 1980s and 1990s. All that remains of the employee database from that period are six CSV files.
For this project, you’ll design the tables to hold the data from the CSV files, import the CSV files into a SQL database, and then answer questions about the data. That is, you’ll perform data modeling, data engineering, and data analysis, respectively.

Data Modeling
Inspect the CSV files, and then sketch an Entity Relationship Diagram of the tables. To create the sketch, feel free to use a tool like QuickDBDLinks to an external site..
Data Engineering
1.	Use the provided information to create a table schema for each of the six CSV files. Be sure to do the following:
o	Remember to specify the data types, primary keys, foreign keys, and other constraints.
o	For the primary keys, verify that the column is unique. Otherwise, create a composite keyLinks to an external site., which takes two primary keys to uniquely identify a row.
o	Be sure to create the tables in the correct order to handle the foreign keys.
2.	Import each CSV file into its corresponding SQL table.
Data Analysis
1.	List the employee number, last name, first name, sex, and salary of each employee.
2.	List the first name, last name, and hire date for the employees who were hired in 1986.
3.	List the manager of each department along with their department number, department name, employee number, last name, and first name.
4.	List the department number for each employee along with that employee’s employee number, last name, first name, and department name.
5.	List first name, last name, and sex of each employee whose first name is Hercules and whose last name begins with the letter B.
6.	List each employee in the Sales department, including their employee number, last name, and first name.
7.	List each employee in the Sales and Development departments, including their employee number, last name, first name, and department name.
8.	List the frequency counts, in descending order, of all the employee last names (that is, how many employees share each last name).

RESULTS
The resulting diagram shows
 The employees table with its primary key emp_no.
 The departments table with its primary key dept_no.
The salaries table linked to the employees table via emp_no.
The titles table linked to the employees table via emp_no.
The dept_emp table linking employees and departments tables via emp_no and dept_no.
The dept_manager table linking employees and departments tables via emp_no and dept_no.

Explanation of Relationships
•	employees:
o	Has a one-to-many relationship with salaries (one employee can have multiple salaries over time).
o	Has a one-to-many relationship with titles (one employee can have multiple titles over time).
o	Has a many-to-many relationship with departments through dept_Emp (an employee can work in multiple departments).
o	Has a many-to-many relationship with departments through dept_manager (an employee can manage multiple departments).
•	departments:
o	Has a many-to-many relationship with employees through dept_Emp (a department can have multiple employees).
o	Has a many-to-many relationship with employees through dept_manager (a department can have multiple managers).
•	dept_emp:
o	Connects employees and departments with foreign key references.
•	dept_manager:
o	Connects employees and departments with foreign key references.
 

DATA engineering and data analysis files are attached in this repository
References
Data generated by Mockaroo, LLCLinks to an external site., (2022). Realistic Data Generator.


