# Project 1: Modeling Data with PostgreSQL
## Summary of the project
Sparkify wants to analize their data of songs and the user activity in the platform. We decided to create with their data a Star schema for doing analytics modeling the information in the correct way so we can query data in a fast way and generate aggregations with the data. In the project we converted JSON files into PostgreSQL tables to convert the data in something more easy to read.
## How to run?
First run the create_tables.py to create the database and the table for the project. Then, for running the project execute the etl.py to create the databases (python etl.py). Then, you can use test.ipynb to see what information get stored with running the ETL.
## Explanation of each file
- data: Folder with the log data of the user activities and the songs data. Both of them are in JSON format
- create_tables.py: Script used to create the database and then create the tables where we will store the information.
- etl.ipynb: Used for testing the ETL pipeline before executing
- etl.py: Script for running the ETL. In the ETL we convert the info and store the processed info in the tables.
- sql_queries.py: Some util queries for create, drop, insert and select data of our tables.
- test.ipynb: Test to query the tables to see if the information was succesfully loaded.
