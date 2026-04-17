
# Azure Lakehouse Analytics Project – Divvy Bikeshare
A complete Azure Lakehouse implementation using Delta Lake and PySpark to deliver analytics-ready datasets through a Star Schema model.

This project implements a modern Azure Lakehouse solution for analyzing Divvy Bikeshare data from Chicago, USA.

<img width="3341" height="2268" alt="Mermaid-preview (1)" src="https://github.com/user-attachments/assets/9427d9ff-0e77-4bcd-8c57-702130edaf88" />

## 🚲 Project Overview

Divvy is a bike sharing program that allows riders to unlock bikes at stations across the city using a kiosk or mobile application and return them either to the same or a different station. The City of Chicago provides anonymized trip data publicly, enabling analytical studies on ride behavior and usage patterns.

To enrich the analytical capabilities, synthetic rider, account, and payment data were generated and combined with the real trip and station datasets. This allows the solution to support business-oriented analytics such as user segmentation, temporal analysis, and revenue insights.

The solution was built using Azure Databricks and Delta Lake, following a Lakehouse architecture with Bronze, Silver, and Gold layers, and culminates in an analytics-ready Star Schema.

## ☁️ Platform

This project was implemented using Azure Databricks with Delta Lake as the storage layer. The focus of the solution is on data modeling, transformation logic, and analytics readiness rather than infrastructure provisioning.

## 🧠 Data Modeling Approach

The original dataset follows a normalized relational model consisting of Rider, Account, Payment, Trip, and Station tables. While suitable for transactional systems, this structure is not optimized for analytical queries.

To address this, the data was transformed into a Star Schema in the Gold layer, separating facts and dimensions to enable efficient analytical queries, aggregation, and BI workloads.

## 📊 Analytics Use Cases

The data model and lakehouse architecture were designed to support the following analytical use cases:

### Ride Behavior Analysis
- Analyze ride duration across different time dimensions (day of week, time of day).
- Compare ride behavior based on starting and ending stations.
- Analyze ride duration based on rider demographics, including age and membership type.

### Revenue Analysis
- Analyze total payment amounts over time (monthly, quarterly, yearly).
- Compare spending patterns between members and casual riders.
- Analyze revenue distribution by rider age at account start.

### Advanced Analytics (Extended Use Cases)
- Analyze rider spending based on average rides per month.
- Analyze monthly ride duration per rider and its relationship to revenue.

This project reflects common patterns used in production-grade analytics platforms and demonstrates practical skills in data engineering, ELT pipelines, and dimensional modeling.

