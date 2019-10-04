# sql_ref
Reference Sheet to start SQL

## How to create a database

Basic Syntax: CREATE DATABASE DatabaseName;
so, creating a new database <newDB> would look like: CREATE DATABASE newDB;

## How to create a table

CREATE TABLE table_name(
   column1 datatype,
   column2 datatype,
   column3 datatype,
   .....
   columnN datatype,
   PRIMARY KEY( one or more columns )
);

EXAMPLE:

CREATE TABLE CUSTOMERS(
   ID   INT              NOT NULL,
   NAME VARCHAR (20)     NOT NULL,
   AGE  INT              NOT NULL,
   ADDRESS  CHAR (25) ,
   SALARY   DECIMAL (18, 2),       
   PRIMARY KEY (ID)
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

SELECT column1, column2....columnN
FROM   table_name;

## How to get one thing from a single table with a "where" clause

SELECT column1, column2....columnN
FROM   table_name
WHERE  CONDITION;

## How to add something to a table

INSERT INTO table_name( column1, column2....columnN)
VALUES ( value1, value2....valueN);

## How to edit something inside of a table

UPDATE table_name
SET column1 = value1, column2 = value2....columnN=valueN
[ WHERE  CONDITION ];

## How to remove something from a table

DELETE FROM table_name
WHERE  {CONDITION};

