# Data Modeling with Postgres  

<br />

## Introduction


In this Notebook we will use PostgreSQL along with Python to create a database schema and ETL pipeline with data collected by the startup Sparkify, who is interested in what songs users are listening too on their newly created app.

At the moment they do not have an easy way to query their data, which resides in a directory of JSON logs on user activity on the app, as well as a directory with JSON metadata on the songs in their app.

We will be defining fact and dimension tables for s star schema for a particular analytic focus.

We will also be creating an ETL pipeline that transfers data from two JSON files stored locally into Postgres using Python and SQL.

Then we will be testing this database and ETL pipeline by running queries givento us by the Sparkify analytics team to compare results with theirs. 

<br />

## Datasets


The dataset is a subset of real data from the Million Song Dataset. 

Each file is in JSON format and contains metadata about a song and the artist of that song. 

The files are partitioned by the first three letters of each song's track ID. 

For example, here are filepaths to two files in this dataset:  

<br />


> song_data/A/B/C/TRABCEI128F424C983.json
>
> song_data/A/A/B/TRAABJL12903CDCF1A.json  

<br />  

And, an example what a single song file looks like:  

<br /> 

> {"num_songs": 1, "artist_id": "ARJIE2Y1187B994AB7", "artist_latitude": null, "artist_longitude": null, "artist_location": "", "artist_name": "Line Renaud", "song_id": "SOUPIRU12A6D4FA1E1", "title": "Der Kleine Dompfaff", "duration": 152.92036, "year": 0}  

<br /> 

## Repository 

The files in the repsitory include: 

* Data Folder - Contains Log and Song Data

* etl.ipynb - Notebook to develop the ETL process for each of your tables before completing the etl.py file to load the whole datasets.

* test.ipynb - Runs first few rows of each table to test the database.

* create_tables.py - Drops and creates taqbles. This file is run to reset tables before each time ETL scripts is ran.

* etl.py - Reads and procesess files from song_dat and log_data and loads them into tables.

* README.md - Read Me file, includes project description, description of data, files, etc.

* sql_queries.py - Contains all SQL queries.

<br /> 

## How to Run

1. Run create_tables.py to create tables and database.
2. Run etl.py for Extracting, and Loading data.
3. Run test.py to test functionality of database.
