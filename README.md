# sql_ref
Reference Sheet to start SQL

## How to create a database

Basic Syntax: CREATE DATABASE DatabaseName;
so, creating a new database <newDB> would look like: CREATE DATABASE newDB;

## How to create a table

CREATE TABLE table_name(<br/>
   column1 datatype,<br/>
   column2 datatype,<br/>
   column3 datatype,<br/>
   .....<br/>
   columnN datatype,<br/>
   PRIMARY KEY( one or more columns )<br/>
);

EXAMPLE:

CREATE TABLE CUSTOMERS(<br/>
   ID   INT              NOT NULL,<br/>
   NAME VARCHAR (20)     NOT NULL,<br/>
   AGE  INT              NOT NULL,<br/>
   ADDRESS  CHAR (25) ,<br/>
   SALARY   DECIMAL (18, 2),<br/>
   PRIMARY KEY (ID)<br/>
);

You can verify if your table has been created successfully by looking at the message displayed by the SQL server, otherwise you can use the DESC command as follows −

DESC CUSTOMERS;

| Field   | Type          | Null | Key | Default | Extra |
|---|---|---|---|---|---|
| ID      | int(11)       | NO   | PRI |         |       |
| NAME    | varchar(20)   | NO   |     |         |       |
| AGE     | int(11)       | NO   |     |         |       |
| ADDRESS | char(25)      | YES  |     | NULL    |       |
| SALARY  | decimal(18,2) | YES  |     | NULL    |       |

5 rows in set (0.00 sec)

## How to get everything from a single table

SELECT column1, column2....columnN FROM table_name;<br/>
e.g.  SELECT name FROM customers;<br/>
or... SELECT * FROM customers;

## How to get one thing or one row from a single table with a "where" clause

SELECT column1, column2....columnN FROM table_name WHERE CONDITION;</br>
e.g.  SELECT age FROM customers WHERE age < 18;<br/>
or... SELECT * FROM customers WHERE age < 18;

## How to add something to a table

INSERT INTO table_name( column1, column2....columnN) VALUES ( value1, value2....valueN);<br/>
e.g. INSERT INTO customers (name, age, address, salary) VALUES ('Joe', 23, '1234 Main St', 18,000);

## How to edit something inside of a table

UPDATE table_name SET column1 = value1, column2 = value2....columnN=valueN [ WHERE  CONDITION ];<br/>
e.g. UPDATE customers SET name = 'Johnnie' WHERE id = 3

## How to remove something from a table

DELETE FROM table_name WHERE  {CONDITION};<br/>
e.g. DELETE FROM customers WHERE age < 18

