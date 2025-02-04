# Online Ticket Booking Stream Data Processing

## Overview
This project implements a real-time data processing pipeline for an online ticket booking system using Azure cloud services. The solution ingests, transforms, and stores streaming data from ticket bookings and payments into a structured data warehouse for analytics and reporting.

The data processing pipeline includes the following stages:

1. **Event Ingestion**: Publishing mock data into Booking and Payments Event Hub.
2. **Real-time Stream Processing**: Using Azure Stream Analytics Job to transform incoming data and perform window-based joins.
3. **Data Storage**: Writing processed data into Synapse Data Warehouse for analytics and reporting.

## Technology Stack

### Core Technologies
- **Programming**: Python
- **Query Language**: SQL

### Azure Services
- **Azure Event Hub**: Captures streaming event data.
- **Azure Stream Analytics**: Performs real-time transformations and window-based joins.
- **Azure Synapse Analytics**: Stores processed data for analytics.
- **Azure SQL Database**: Provides structured storage for transactional data.

## Architecture
![Screenshot 2025-02-04 170910](https://github.com/user-attachments/assets/effca953-8324-42d8-9ea0-54213edb6cde)

## Implementation Details

### 1. Data Ingestion
- Generate mock event data for ticket bookings and payments.
- Publish these events to respective Event Hubs for processing.

### 2. Stream Processing
- Use Azure Stream Analytics Job to perform:
  - **Real-time transformations**: Standardizing data format and ensuring data consistency.
  - **Window-based joins**: Combining booking and payment events within defined time windows.
  - **Filtering and enrichment**: Removing duplicate records and adding metadata.

### 3. Data Storage and Analytics
- Write the transformed and enriched data into an Azure Synapse table for further analysis.
- Use SQL queries to extract business insights and generate reports.

## Challenges and Solutions

### Technical Challenges
1. **Data Latency**
   - Challenge: Processing delays in streaming data.
   - Solution: Optimized Stream Analytics query performance using parallelism and partitioning.

2. **Schema Evolution**
   - Challenge: Handling changes in event schema over time.
   - Solution: Implemented versioning strategy and schema validation mechanisms.

3. **Window-based Joins**
   - Challenge: Ensuring bookings and payments are correctly correlated within a time window.
   - Solution: Used sliding window joins to maintain accuracy.

## Project Outcomes
- Successfully implemented a real-time stream processing pipeline.
- Achieved seamless integration between Azure Event Hub, Stream Analytics, and Synapse.
- Established a scalable solution for real-time ticket booking insights.


