# Database for bank system  

#### note that : The documents are in PDF and TXT format and can be opened with a PDF reader or a text editor.

## This repository contains the documentation for a bank database. The documents are:

## ERD
#### The ERD shows the entities and relationships in the database.
#### BANK_ERD.pdf: The Entity-Relationship Diagram (ERD) for the database.


## Conceptual Model: 
#### The conceptual model shows the overall structure of the database.
#### Conceptual Model.pdf : The conceptual model of the database.


## DFD: 
#### The DFD shows the flow of data through the database.
#### DFD.pdf : The Data Flow Diagram (DFD) for the database.


## Data_Dictionary: 
#### The data dictionary defines the data elements in the database.
#### Data_Dictionary.pdf : The data dictionary for the database.


## Mapping:
#### The mapping shows how the ERD and the DFD are related
#### Mapping.pdfThe : mapping between the ERD and the DFD.


## Relationship Matrix :
#### The relationship matrix shows the relationships between the entities in the database.
#### Relationship Matrix.pdf : The relationship matrix for the database.


## define database schema : 
#### The database schema is the actual definition of the database tables and columns.
#### database schema.txt : The database schema ( SQL sentax which creats the tables ).


## queries file :
#### The SQL queries in the QUERY_ANALYSIS.txt file can be used to analyze the data in the database.
#### QUERY_ANALYSIS.txt : The SQL queries used to analyze the database.



## Schemas

### DEPARTMENT schema
```sql
CREATE TABLE DEPARTMENT(DNAME varchar(45), 
DNUMBER INT PRIMARY KEY, 
MGRSSN INT, 
MGRSTARTDATE INT);

### EMPLOYEE schema
```sql
CREATE TABLE EMPLOYEE(FNAME varchar(45), 
MINIT varchar(45),SSN INT PRIMARY KEY, 
BDATE date,ADDRESS varchar(45), 
SEX varchar(45), 
SALARY float, 
SUPERSSN INT, 
DNO INT, 
foreign key(DNO) REFERENCES DEPARTMENT (DNUMBER)); 


### PROJECTS schema
```sql
CREATE TABLE PROJECTS ( 
    PNAME varchar(45), 
    PNUMBER INT PRIMARY KEY, 
    DNUM INT, 
    PLOCATION varchar(45), 
   foreign key(DNUM) REFERENCES DEPARTMENT(DNUMBER) 
); 


### DEPT_LOCATIONS schema
```sql
CREATE TABLE DEPT_LOCATIONS(DNUMBER INT,DLOCATION INT PRIMARY KEY, 
foreign key(DNUMBER)REFERENCES DEPARTMENT(DNUMBER)); 



### WORKS_ON schema
```sql
CREATE TABLE WORKS_ON(PNO INT, 
HOURS INT, 
ESSN INT, 
foreign key(PNO) REFERENCES PROJECTS(PNUMBER), 
foreign key(ESSN) REFERENCES EMPLOYEE(SSN) 
); 


### DEPENDENT schema
```sql
CREATE TABLE DEPENDENT ( 
    DEPARTMENT_NAME varchar(45), 
    ESSN INT, 
    SEX varchar(45), 
   BDATE date, 
    RELATRIONSHIP varchar(45), 
   foreign key(ESSN) REFERENCES EMPLOYEE(SSN) 
);




