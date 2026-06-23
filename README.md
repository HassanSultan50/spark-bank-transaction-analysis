# Spark Bank Transaction Analysis

A big-data analysis of a large bank-transaction dataset using Apache Spark (PySpark). The project loads multi-table financial data — transactions, cards, users, merchant-category (MCC) codes, and fraud labels — into Spark DataFrames for exploration and analysis at scale.

## What it does & why

Transaction datasets are too large to analyze comfortably with single-machine tools, which makes them a natural fit for a distributed engine like Spark. This notebook sets up a Spark session, ingests the dataset's CSV and JSON sources, and prepares the DataFrames needed to explore spending patterns and fraud signals across millions of records.

The dataset includes:
- `transactions_data.csv` — individual card transactions
- `cards_data.csv` — card metadata
- `users_data.csv` — cardholder information
- `mcc_codes.json` — merchant category codes
- `train_fraud_labels.json` — fraud labels for supervised analysis

## Tech stack

- **Apache Spark** via **PySpark** (`SparkSession`, Spark SQL functions)
- **Jupyter Notebook** (developed on a Jupyter/`jovyan` Spark environment)
- Python 3

## Project structure

```
bank_transaction_analysis.ipynb   Spark session setup, dataset download/ingestion, and analysis
```

## Setup & run

1. Install dependencies:
   ```bash
   pip install pyspark jupyter requests
   ```
2. Launch Jupyter and open the notebook:
   ```bash
   jupyter notebook bank_transaction_analysis.ipynb
   ```
3. Run the cells top to bottom. The notebook downloads and unzips the dataset, starts a local Spark session, and reads each source into a DataFrame.

> Note: the notebook references the course dataset via a download link and uses paths from the original Jupyter environment (`/home/jovyan/...`); adjust the dataset path to match where you extract the data locally.

## My role

This was a **team project** for a Big Data Processing course at the University of Oulu. I was the **primary developer**, leading the Spark data-ingestion pipeline and the transaction analysis.
