# Stock Market Data Pipeline using Kafka and AWS

## Overview
This project demonstrates a real-time stock market data processing pipeline using Apache Kafka, AWS Services like AWS EC2, S3, AWS Glue Crawler, AWS Glue Data Catalog and AWS Athena and Python. The architecture enables ingestion, storage, and querying of stock market data efficiently.

## Architecture
The system is structured as follows:

1. Dataset:
The pipeline starts with a stock market dataset stored in CSV format. The dataset is used to simulate stock price fluctuations.

2. Producer - Stock Market App Simulation (Python & Boto3):
A Python-based stock market simulator reads data from the CSV file. Uses Boto3 SDK to interact with AWS. Sends stock market data as real-time messages to Kafka.

3. Apache Kafka (Running on Amazon EC2):
Kafka acts as a distributed message broker. It enables real-time streaming of stock market data. The producer sends stock price updates to a Kafka topic.

4. Consumer - Processing and Storage:
A Kafka consumer retrieves stock market data messages. The consumer processes and stores data into Amazon S3.

5. AWS Glue (Crawler & Data Catalog):
AWS Glue Crawler scans the stock data stored in Amazon S3. It updates the AWS Glue Data Catalog, making the data queryable.

6. Amazon Athena:
Athena enables SQL-based querying of the stored stock market data. Users can analyze stock trends and perform insights on real-time and historical data.

## Technologies Used

1. **Apache Kafka (Running on AWS EC2)**
2. **Python (Data producer and consumer)**
3. **Boto3 SDK (AWS SDK for Python)**
4. **AWS S3 (Data storage)**
5. **AWS Glue (Data cataloging and ETL)**
6. **AWS Athena (SQL querying)**

## Setup & Installation
1. Setup Kafka on AWS EC2
Launch an EC2 instance and install Kafka. Configure Kafka topics for stock market data streaming.

2. Run the Producer and consumer in Jupyter Notebook.
   
3. Configure AWS Glue & Athena
Create an AWS Glue Crawler to catalog data in S3. Use Amazon Athena to run SQL queries on the data.

