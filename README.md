McStream: Real-Time Order & Payment Pipeline

Project Overview

McStream is a real-time data streaming pipeline that simulates the ordering and payment processes of a fast-food chain (McDonald's). It leverages Apache Kafka for data streaming, Avro for data serialization, MongoDB Atlas for cloud storage, and ksqlDB for stream processing. The entire pipeline is deployed across Azure (Kafka brokers) and AWS (Schema Registry).

This project demonstrates a real-world application of cloud-based, scalable, and efficient data engineering practices.

Technologies Used

Component

Technology Used

Data Generator

Python

Data Streaming

Apache Kafka (Confluent Cloud - Azure)

Data Serialization

Avro + Confluent Schema Registry (AWS)

Data Storage

MongoDB Atlas

Stream Processing

ksqlDB

Cloud Infrastructure

Azure (Kafka), AWS (Schema Registry), MongoDB Atlas

Architecture Flow

Python Mock Data Producer

Generates mock order and payment data every few seconds.

Publishes data to Kafka topics: macd_orders and macd_payments.

Kafka Streaming

Kafka topics hosted on Confluent Cloud (Azure Central India).

Data serialized using Avro, validated by Schema Registry (AWS ap-south-1).

Stream Processing with ksqlDB

Real-time joins between orders and payments using order_id.

SQL-like queries to transform and aggregate streaming data.

Storage

(Optional) Store final processed output into MongoDB Atlas for analytics.

File Structure

.
├── mock_data_producer.py        # Python script to generate and publish mock data
├── orders_avro_schema.json      # Avro schema for order records
├── payments_avro_schema.json    # Avro schema for payment records
├── ksql_db_commands.sql         # ksqlDB queries for stream processing

How to Run the Project

Set up Confluent Cloud resources

Create Kafka cluster on Azure Central India

Set up Schema Registry on AWS ap-south-1

Create two topics: macd_orders and macd_payments

Configure Environment Variables

Update the kafka_config and schema_registry_client sections inside mock_data_producer.py with your Confluent Cloud credentials.

Install Dependencies

pip install confluent_kafka
pip install fastavro

Run the Data Producer

python mock_data_producer.py

Set up ksqlDB Queries

Execute queries from ksql_db_commands.sql in the ksqlDB editor.

Optional: Integrate MongoDB Sink

Configure a Kafka MongoDB sink connector to push joined data into MongoDB Atlas.

Key Learnings

Setting up real-time data pipelines on the cloud

Using Avro schemas for data validation and evolution

Handling cross-region cloud deployments (Azure + AWS)

Performing real-time stream joins using SQL-like queries in ksqlDB

Building scalable data ingestion systems for analytics

Future Enhancements

Automate end-to-end deployment using Terraform

Visualize processed data using Grafana or Metabase

Implement real-time anomaly detection and alerting

Integrate machine learning models for predictive analytics

Contributors

Pavan Kumar G - LinkedIn Profile

Poojith Ramesh - LinkedIn Profile

