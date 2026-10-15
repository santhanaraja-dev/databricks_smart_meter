
# Databricks Smart Meter Data Pipeline

An end-to-end data engineering project on Databricks that takes raw smart meter data through a Raw → Silver → Gold medallion pipeline and presents the results in dashboards.

## Architecture
Raw smart meter data → Silver (cleaned data) → Gold (aggregated business tables) → Dashboards

## Dataset
- Source: [e.g. sample / synthetic / public dataset and where it came from]
- Format: [CSV / JSON / Parquet]
- Size: [approx. number of rows and meters]
- Main fields: [e.g. meter ID, timestamp, energy usage, voltage, alarms]

## Pipeline
**Silver layer: loading and cleansing**
- Loaded raw files into Databricks using PySpark
- [Cleaning steps you did, e.g. removed duplicates, handled nulls, fixed data types, standardised timestamps, filtered invalid readings]

**Gold layer: aggregation**
- Built aggregated tables for business analysis
- [Aggregations you did, e.g. daily and monthly usage by meter or region]

## Dashboards
| Notebook | Purpose |
|----------|---------|
| Executive Overview dashboard | High-level KPIs for management |
| Utility Usage dashboard | Electricity consumption trends |
| Meter Health & Alarms dashboard | Meter status and alarm monitoring |
| Power Quality dashboard | Power quality metrics |
| Data Quality & Operations dashboard | Data quality checks and operational monitoring |
| Electricity Business Analysis dashboard | Business-level analysis of electricity data |

## Repository Contents
| File | Description |
|------|-------------|
| Loading and cleansing of data (silver).ipynb | Loads raw data and creates the Silver layer |
| Aggregated Table ( silver - gold ).ipynb | Builds aggregated tables from Silver to Gold |
| gold_electricity_business_analysis.ipynb | Gold layer tables for business analysis |
| *_dashboard*.ipynb | Notebooks behind each dashboard |

## Screenshots
![Executive Overview](screenshots/executive_overview.png)

## Tech Stack
Databricks, PySpark, Python, SQL, Medallion Architecture

## How to Run
1. Import the notebooks into a Databricks workspace (or clone this repo as a Git folder).
2. Upload the source data and update the file path in the Silver notebook.
3. Run the notebooks in order: Silver → Gold → dashboards.
