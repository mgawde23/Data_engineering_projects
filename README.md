1. Sensory Data Autoloader Handson :Technical Summary of the Project

Title: Real-Time IoT Sensor Lakehouse via Delta Live Tables (DLT)

Architecture: Built a scalable, streaming Medallion Architecture using Databricks Auto Loader and PySpark DLT to process high-velocity sensor data.

Ingestion (Bronze): Leveraged Auto Loader (cloudFiles) with schema inference to incrementally ingest raw CSV files from Cloud Volumes into a streaming Bronze table.

Data Quality (Silver): Implemented DLT Expectations (Data Quality Gates) to enforce business rules:

Warning level: Flagged null timestamps.

Enforcement level: Automatically dropped records with out-of-range temperature/humidity values to ensure downstream data integrity.

Aggregation (Gold): Developed a streaming Gold layer using Watermarking and Windowing functions to calculate minutely sliding averages for sensor metrics, handling late-arriving data effectively.
