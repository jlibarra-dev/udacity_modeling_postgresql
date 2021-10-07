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
## Star model schema
### Fact Table
* songplays - records in log data associated with song plays i.e. records with page NextSong

songplay_id, start_time, user_id, level, song_id, artist_id, session_id, location, user_agent
### Dimension Tables
* users - users in the app

user_id, first_name, last_name, gender, level
 
* songs - songs in music database

song_id, title, artist_id, year, duration

* artists - artists in music database

artist_id, name, location, latitude, longitude

* time - timestamps of records in songplays broken down into specific units

start_time, hour, day, week, month, year, weekday

![udacityPostgre drawio](https://user-images.githubusercontent.com/54164818/136455768-fbed7934-43c6-4aa7-bcea-2e9373ed738e.png)

