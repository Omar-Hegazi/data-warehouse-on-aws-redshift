## Introduction
A music streaming startup, Sparkify, has grown their user base and song database and want to move their processes and data onto the cloud. Their data resides in S3, in a directory of JSON logs on user activity on the app, as well as a directory with JSON metadata on the songs in their app.


## Details
Building an ETL pipeline that extracts their data from S3, stages them in Redshift, and transforms data into a set of dimensional tables.
### Datasets
I worked with two datasets that reside in S3. Here are the S3 links for each:

Song data: s3://udacity-dend/song_data

Log data: s3://udacity-dend/log_data

Log data json path: s3://udacity-dend/log_json_path.json

#### Song Dataset
The first dataset is a subset of real data from the Million Song Dataset. Each file is in JSON format and contains metadata about a song and the artist of that song. 

#### Log Dataset
The second dataset consists of log files in JSON format generated by this event simulator based on the songs in the dataset above. These simulate app activity logs from an imaginary music streaming app based on configuration settings.


## Files
- `create_tables.py`  to connect to the database and create these tables.
- `dwh.cfg` Configure Redshift cluster and data import.
- `etl.py`  to load data from S3 to staging tables on Redshift.
- `sql_queries.py` code to create and drop tables and insert new data into dimensions tables

## How to run
- Configure the dwh.cfg file into you cluster details
- In terminal run, `python create_tables.py`
- In terminal run, `python etl.py`
  
