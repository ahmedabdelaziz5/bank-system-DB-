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


## Schemas
### User schema
sql
CREATE TABLE users (
id INT NOT NULL AUTO_INCREMENT,
name VARCHAR(255) NOT NULL,
address VARCHAR(255) NOT NULL,
email VARCHAR(255) NOT NULL,
phone_number VARCHAR(255) NOT NULL,
account_number VARCHAR(255) NOT NULL,
PRIMARY KEY (id)
);

## queries file :
#### The SQL queries in the QUERY_ANALYSIS.txt file can be used to analyze the data in the database.
#### QUERY_ANALYSIS.txt : The SQL queries used to analyze the database.


