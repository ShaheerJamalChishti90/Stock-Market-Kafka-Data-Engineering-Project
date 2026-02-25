## Stock Market Kafka Real-Time Data Engineering Project 

This project demonstrates how to build an end-to-end real-time data engineering pipeline using stock market data. The main focus is on the operational side of data engineering, meaning designing, building, and managing a scalable data pipeline rather than just analyzing data.

The pipeline simulates real-time stock market data streaming through **Apache Kafka**. A Python producer reads stock market data from a CSV file and publishes it to a Kafka topic. A Kafka consumer then processes the streaming data and stores it in **Amazon S3** for further use.

On the AWS side, multiple services are integrated:

* **Amazon EC2** is used to host and run Kafka.
* **Amazon S3** acts as the data lake where streaming data is stored.
* **AWS Glue Crawler** scans the data stored in S3 and creates metadata tables.
* **AWS Glue Data Catalog** stores the schema and table definitions.
* **Amazon Athena** is used to query the stored data directly from S3 using SQL.

The architecture showcases how real-time streaming data flows from ingestion (Kafka) to storage (S3), then to metadata management (Glue), and finally to analytics (Athena).

Overall, this project highlights:

* Real-time data ingestion using Apache Kafka
* Cloud-based data lake architecture on AWS
* Automated schema detection using Glue
* Serverless querying using Athena
* End-to-end integration between streaming systems and cloud analytics

It’s a practical example of how modern data engineering systems handle streaming financial data in a scalable and cost-effective way.
