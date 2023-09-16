# Data Storage Paradigms: Data Lake vs. Data Lakehouse vs. Delta Lake - CDC Use Case

![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)

## Overview

In today's data-driven landscape, selecting the appropriate data storage solution is critical. This project explores three key data storage paradigms and their relevance to Change Data Capture (CDC):

1. **Data Lakes**: Imagine Data Lakes as vast reservoirs capable of storing massive volumes of raw data in various formats. They offer flexibility for handling diverse datasets, making them suitable for data variety and scalability.
![Data Lake](https://raw.githubusercontent.com/amar5075kumar/CDC-use-case/main/Images/Data_Lake.png)
![Data Lake](https://raw.githubusercontent.com/amar5075kumar/CDC-use-case/main/Images/Data_Lake_Flow.png)

2. **Data Lakehouses**: Data Lakehouses strike a balance between the flexibility of Data Lakes and the structured querying of data warehouses. They aim to organize data effectively, ensuring data quality and consistency while facilitating analytics on raw data.
![Data Lakehouse](https://raw.githubusercontent.com/amar5075kumar/CDC-use-case/main/Images/Data_Lakehouse.png)
![HUDI File Strorage](https://raw.githubusercontent.com/amar5075kumar/CDC-use-case/main/Images/HUDI_Architecture.png)

**HUDI File Strorage**: Apache Hudi (Hadoop Upserts Deletes and Incrementals) is an open-source data management framework that simplifies the process of managing large-scale, incremental data. It provides support for both real-time and batch data processing and is particularly valuable for CDC operations.

**Key features of Apache Hudi**:

- ACID Compliance: Hudi ensures Atomicity, Consistency, Isolation, and Durability (ACID) compliance for data operations, critical for maintaining data integrity during CDC.
- Incremental Processing: Hudi allows for efficient incremental data ingestion and processing, making it suitable for real-time data changes.
- Time Travel: The framework offers time-travel capabilities, enabling you to access data at different points in time, essential for historical analysis and auditing.

**Types of HUDI Tables**: Copy On Write & Merge On Read
![HUDI File Strorage](https://raw.githubusercontent.com/amar5075kumar/CDC-use-case/main/Images/HUDI_COW_Architecture.png)
![HUDI File Strorage](https://raw.githubusercontent.com/amar5075kumar/CDC-use-case/main/Images/HUDI_MOR_Architecture.png)

3. **Delta Lake**: Delta Lake builds upon Data Lakes by introducing essential ACID transactions, enhancing data reliability and security. Features like schema enforcement, time travel, and data versioning further bolster data management.
![Delta Lake](https://raw.githubusercontent.com/amar5075kumar/CDC-use-case/main/Images/Delta_Lake_Architecture.png)

## The CDC Use Case: Keeping Data in Sync

**Change Data Capture (CDC)** is a technique for capturing and tracking changes in data so that downstream applications can respond swiftly to those changes. The project explores a real-world use case where CDC plays a pivotal role:

**Use Case**: Imagine an e-commerce platform where real-time inventory management is crucial. When new products arrive or existing ones are sold, you want your inventory system to update instantly. This is where CDC shines.

### How Each Paradigm Handles CDC

- **Data Lake**: CDC can be implemented using tools like Apache Kafka or Apache Nifi to ingest and process real-time data changes in a Data Lake. While feasible, ensuring reliability and consistency can be demanding.

- **Data Lakehouse**: A Data Lakehouse simplifies CDC with its structured environment for real-time data processing. The structured nature makes querying and integration smoother, streamlining inventory management and CDC implementation.

- **Delta Lake**: Delta Lake, with its ACID transactions and time-travel capabilities, offers a robust solution for CDC. It guarantees data consistency even in high-velocity data scenarios, seamlessly integrating CDC operations for real-time updates to the inventory system while preserving data integrity.

## Project Structure

This project is divided into four parts:

- **Part 1: CDC in Data Lakes**: An exploration of Data Lakes with a CDC twist. Hands-on code examples demonstrate how Data Lakes capture real-time changes.

- **Part 2: Data Lakehouses and CDC**: A dive into Data Lakehouses and their connection with CDC. Code examples illustrate how Data Lakehouses enhance accessibility and organization of changing data.

- **Part 3: Delta Lake and CDC**: An examination of Delta Lake as the guardian of your data, particularly in the context of CDC. Practical code examples showcase Delta Lake's role in ensuring data integrity.

- **Part 4: Comparing CDC Across the Trio**: A comprehensive comparison of CDC implementations in Data Lakes, Data Lakehouses, and Delta Lakes. We discuss their strengths, limitations, and real-world applications.

By the end of this project, you will have a well-defined roadmap for selecting the ideal data storage solution for your CDC-driven data needs.

For the full project and code, visit the [GitHub Repository](https://github.com/amar5075kumar/CDC-use-case).

## Get Started

To get started with this project, simply explore the different parts and follow the provided code examples. Each part provides in-depth insights into the respective data storage paradigm and its application in CDC.

Enjoy your journey through the world of data storage paradigms and Change Data Capture!

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.
