# Automate-Data-Pipelines-with-Airflow

This project leverages Apache Airflow to create a data pipeline that are dynamic and 
built from reusable tasks, can be monitored, and allow easy backfills.
The dataset is comprised of two different datasets called log and song datasets reside in S3 buckets.
The first dataset is called song_data, which is a subset of real data from the Million Song Dataset.
Each file of the song_data dataset is in JSON format and contains metadata about a song and the artist of that song.
The second dataset is called log_data consists of log files in JSON files, where each file covers the users activities over a given day. 
JSON data residing in S3 is fed trough a data pipeline defined in Apache Airflow.
The pipeline stages data into Redshift before inserting data into suitable tables for analysis.
Tests are run on the dataset after the ETL steps to identify any error in the pipeline. 
The end result is a Redshift cluster with data organized into a star schema with fact and dimension tables. 
