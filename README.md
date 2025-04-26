McStream: Real-Time Order & Payment Pipeline

This project builds a real-time cloud-native data pipeline simulating McDonald's order and payment processing.
It uses Python for data generation, Apache Kafka (Confluent Cloud - Azure) for streaming, Avro for data serialization with Schema Registry (AWS), ksqlDB for real-time stream processing, and MongoDB Atlas for data storage.

The pipeline demonstrates real-time ingestion, stream processing, and optional storage integration across multi-cloud infrastructure.
It was designed to handle real-time analytics, streaming joins, and scalable data management.

Key Technologies: Python, Kafka, Avro, Confluent Cloud, Schema Registry, ksqlDB, MongoDB Atlas

Main Features:

Mock McDonald's order and payment data generation

Streaming via Kafka topics with Avro serialization

Stream joins using ksqlDB

Secure cross-region cloud deployment (Azure Kafka + AWS Schema Registry)

Optional MongoDB integration for analytics storage

Contributors: Pavan Kumar G, Poojith Ramesh

