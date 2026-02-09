# StreamSmart Data Pipeline

This project implements a small-scale end-to-end data pipeline for **StreamSmart**, a subscription-based digital content company. The pipeline simulates real-world data engineering tasks including ingestion, cleaning, feature engineering, API enrichment, and database loading.

---

## Project Objectives

- Consolidate data from multiple sources (CSV and JSON)
- Clean and standardise messy raw data
- Engineer analytical features to support business decisions
- Enrich data using an external public API with error handling
- Load structured data into a relational database
- Demonstrate reproducible workflows using Git and Python

---

## Tech Stack

- **Python** (Pandas, NumPy)
- **Jupyter Notebook**
- **SQLAlchemy**
- **SQLite**
- **REST Countries API**
- **Git / Command Line**

---

## Project Structure
streamsmart-pipeline/
│
├── notebooks/
│ └── StreamSmart_Pipeline.ipynb
│
├── data/
│ ├── raw/ # Original raw CSV and JSON files
│ ├── processed/ # Cleaned and enriched datasets
│ └── db/ # SQLite database
│
└── README.md


---

## Pipeline Overview

1. **Ingestion**
   - Load raw CSV and JSON datasets
   - Preserve raw data without modification

2. **Cleaning & Validation**
   - Standardise text fields
   - Handle missing values using business rules
   - Enforce data integrity (drop invalid identifiers)

3. **Feature Engineering**
   - Subscription activity flags
   - Revenue estimation
   - Subscription duration metrics

4. **API Enrichment**
   - Fetch country names from a public API
   - Implement retry logic and graceful failure handling

5. **Database Loading**
   - Normalised relational schema:
     - `users`
     - `subscriptions`
     - `analytics_summary`
   - Load data using SQLAlchemy and SQLite

6. **Analysis & Documentation**
   - Basic business metrics
   - Documented assumptions and limitations
   - Version-controlled development history

---

## How to Run

1. Create and activate a Python virtual environment
2. Install dependencies:

pip install pandas numpy requests sqlalchemy jupyter

3. Launch Jupyter:
jupyter notebook
4. Open and run:
notebooks/StreamSmart_Pipeline.ipynb

---

## Notes

- Revenue estimates are simplified and intended for analytical insights, not financial reporting.
- External API failures do not break the pipeline by design.
- This project is structured to be easily extended or automated.

---

## Author

**Pravallika**  
GitHub: https://github.com/Pravallika-0202
