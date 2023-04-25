# Spotify End-to-End ETL Project
### Overview
In this project we are going to extract, transform and load spotify top global songs playlist data for every week using spotify API on AWS.

![this is a screenshot](etl_pipeline.jpg)

### Understanding Dataset/API
[Spotify API](https://developer.spotify.com/documentation/web-api) to retrieve spotify data. The data contains artists, songs and album names from top global songs spotify playlist. Using that data we can depict top 50 songs of the week, artist name for that song, name of the album that song belong to and how many songs that album has. We are going to transform the extracted data into readable format and load data into respective tables.

### Services Used
1. S3
2. AWS Lambda
3. CloudWatch
4. Glue Crawler
5. Data Catalog
6. Amazon Athena

### Execution Steps
1. Create a S3 Bucket.
2. Create a AWSLambda Function to extract data using spotify api.
3. Create a AWSLambda Function to transform extracted data.
4. Add triggers to functions to extract data at desired rate and process the data once it is extracted.
5. Create Crawler to automatically identify the data format or infer schema of the processed data to create a Data Catalog.
6. Data Catalog is used to manage data that can be used by other services.
7. Query data with Amazon Athena.
