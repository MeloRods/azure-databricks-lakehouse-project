## 📓 Notebooks
<ul>
  <li>
    <a href="Notebooks/Bronze - Ingest and Querying in DBFS.ipynb" target="_blank">
      Bronze - Ingest and Querying in DBFS.ipynb
    </a>
  </li>
  <li>
    <a href="Notebooks/Silver - Table Transformation.ipynb – Data cleansing and transformations" target="_blank">
      Silver - Table Transformation.ipynb – Data cleansing and transformations
    </a>
  </li>
  <li>
    <a href="Notebooks/Gold - Tables Creation and Data Transformation.ipynb – Star schema (facts & dimensions)" target="_blank">
      Gold - Tables Creation and Data Transformation.ipynb – Star schema (facts & dimensions)
    </a>
  </li>
</ul>



# Azure Databricks Lakehouse Analytics Project – Divvy Bikeshare

A complete Azure Lakehouse implementation using Delta Lake and PySpark to deliver analytics-ready datasets through a Star Schema model.



<img width="3341" height="2268" alt="Star Schema Diagram" src="https://github.com/user-attachments/assets/9427d9ff-0e77-4bcd-8c57-702130edaf88" />

## 🚲 Project Overview

This project analyzes Divvy Bikeshare data from Chicago, USA, a public bike sharing program that allows riders to unlock bikes at stations across the city and return them to the same or different locations. The City of Chicago provides anonymized trip data publicly, enabling detailed analysis of ride behavior and usage patterns.

To support richer analytical scenarios, synthetic rider, account, and payment data were generated and combined with the real trip and station datasets. This makes it possible to explore both behavioral and financial aspects of the service, such as user segmentation, temporal patterns, and revenue analysis.

The solution was implemented using Azure Databricks and Delta Lake, following a Lakehouse architecture with Bronze, Silver, and Gold layers, and delivering an analytics-ready Star Schema in the Gold layer.

## ☁️ Platform & Architecture

The platform is based on Azure Databricks with Delta Lake as the storage layer. The focus of the implementation is on data modeling, transformation logic, and analytics readiness, reflecting patterns commonly used in production analytics platforms rather than infrastructure provisioning.

All transformations follow an ELT approach, progressively refining data across Bronze, Silver, and Gold layers.

## 🧠 Data Modeling Approach

The original dataset follows a normalized relational model consisting of Rider, Account, Payment, Trip, and Station tables. While suitable for transactional systems, this structure is not optimized for analytical workloads.

To address this, the data was transformed into a Star Schema in the Gold layer, separating fact and dimension tables to enable efficient aggregations, simplified queries, and BI-friendly analytics.

## 📊 Analytics Use Cases

The Lakehouse architecture and dimensional model were designed to support the following analytical use cases:

### Ride Behavior Analysis
- Analyze ride duration across time dimensions such as day of week and time of day.
- Compare rides based on starting and ending stations.
- Analyze ride duration by rider demographics, including age and membership type.

### Revenue Analysis
- Analyze total spending over time (monthly, quarterly, yearly).
- Compare spending patterns between members and casual riders.
- Analyze revenue distribution by rider age at account start.

### Advanced Analytics
- Analyze rider spending based on average rides per month.
- Relate monthly ride duration per rider to their spending behavior.

This project reflects common patterns used in production-grade analytics platforms and demonstrates practical experience with data engineering, ELT pipelines, and dimensional modeling in a cloud-based Lakehouse architecture.
``
