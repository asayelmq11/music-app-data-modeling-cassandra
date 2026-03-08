# Music App Data Modeling with Cassandra

This project implements an ETL pipeline and data modeling solution using Apache Cassandra to analyze music streaming event data.
The pipeline extracts raw event logs, transforms them into a clean dataset, and loads them into Cassandra tables optimized for specific analytical queries.

## Project Overview 

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
## Project Structure

```
music-app-data-modeling-cassandra/
├── data/
│   ├── event_datafile_new.csv
│   └── event_data/
│       ├── 2018-11-01-events.csv
│       ├── 2018-11-02-events.csv
│       └── …etc
├── notebooks/
│   └── cassandra_etl_pipeline.ipynb
├── images/
├── README.md
└── requirements.txt
```
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

## Example Queries

### Query 1
Retrieve artist name, song title, and song length for:
sessionId = 338 and itemInSession = 4

### Query 2
Retrieve artist name, song name (sorted by itemInSession), and user name
for userId = 10 and sessionId = 182

### Query 3
Retrieve all users who listened to the song:
"All Hands Against His Own"
