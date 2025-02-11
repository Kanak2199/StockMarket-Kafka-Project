## Stock Market Data Pipeline using Kafka and AWS

# Overview
This project demonstrates a real-time stock market data processing pipeline using Apache Kafka, AWS Services like AWS EC2, S3, AWS Glue Crawler, AWS Glue Data Catalog and AWS Athena and Python. The architecture enables ingestion, storage, and querying of stock market data efficiently.

# Architecture
The system is structured as follows:

Dataset (CSV Format):

The pipeline starts with a stock market dataset stored in CSV format.
The dataset is used to simulate stock price fluctuations.
Producer - Stock Market App Simulation (Python & Boto3):

A Python-based stock market simulator reads data from the CSV file.
Uses Boto3 SDK to interact with AWS.
Sends stock market data as real-time messages to Kafka.
Apache Kafka (Running on Amazon EC2):

Kafka acts as a distributed message broker.
It enables real-time streaming of stock market data.
The producer sends stock price updates to a Kafka topic.
Consumer - Processing and Storage:

A Kafka consumer retrieves stock market data messages.
The consumer processes and stores data into Amazon S3.
AWS Glue (Crawler & Data Catalog):

AWS Glue Crawler scans the stock data stored in Amazon S3.
It updates the AWS Glue Data Catalog, making the data queryable.
Amazon Athena:

Athena enables SQL-based querying of the stored stock market data.
Users can analyze stock trends and perform insights on real-time and historical data.
Technologies Used
Apache Kafka (Running on AWS EC2)
Python (Data producer and consumer)
Boto3 SDK (AWS SDK for Python)
AWS S3 (Data storage)
AWS Glue (Data cataloging and ETL)
AWS Athena (SQL querying)

