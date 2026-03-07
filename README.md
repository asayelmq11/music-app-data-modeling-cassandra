# music-app-data-modeling-cassandra
Cassandra ETL Pipeline for Music Streaming Data
This project builds an ETL pipeline and data model using Apache Cassandra to analyze music streaming event data.

## Project Overview

The pipeline processes event data generated from a music streaming application.

Steps performed:

1. Extract event data from multiple CSV files
2. Transform and combine the files into a single dataset
3. Load the processed data into Apache Cassandra tables
4. Query the data using optimized Cassandra data models

---

## Technologies Used

- Python
- Apache Cassandra
- Pandas
- Jupyter Notebook

---

## Dataset

The dataset contains music streaming activity with the following columns:

- artist
- firstName
- gender
- itemInSession
- lastName
- length
- level
- location
- sessionId
- song
- userId

---

## Data Modeling in Cassandra

Cassandra requires designing tables based on query patterns.

Three tables were created to support specific analytical queries.

Table:
