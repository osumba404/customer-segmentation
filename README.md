# Customer Segmentation

Customer segmentation of the **Online Retail II** dataset using **RFM (Recency, Frequency, Monetary)** features and **K-Means clustering** in Python.

## Overview

This project segments customers of a UK-based online retail company (gift items, 2009–2011) into actionable groups: e.g. **Retain**, **At Risk**, **Champions**, **Pamper**. The analysis is in `customer-segmentation.ipynb` with step-by-step explanations.

## Dataset

- **Name:** [Online Retail II](https://archive.ics.uci.edu/dataset/502/online+retail+ii) (UCI)
- **File:** `online_retail_II.xlsx` (place in project folder or set path in the notebook)
- **Variables:** Invoice, StockCode, Description, Quantity, InvoiceDate, Price, Customer ID, Country

## What the Notebook Does

| Step | Description |
|------|-------------|
| 1 | **Imports** — pandas, numpy, matplotlib, seaborn, scikit-learn |
| 2 | **Data exploration** — load data, shape, info, describe, missing values, cancellations, negative quantities, StockCode patterns |
| 3 | **Data cleaning** — drop null Customer ID, valid invoices only, valid StockCodes, remove zero/negative prices |
| 4 | **Feature engineering (RFM)** — Recency, Frequency, Monetary per customer |
| 5 | **Outlier handling** — separate high monetary/frequency outliers |
| 6 | **Scaling** — StandardScaler on RFM |
| 7 | **K-Means** — choose k (e.g. silhouette), fit, assign cluster labels |
| 8 | **Segment labels** — name clusters and outlier groups |
| 9 | **Visualization** — segment counts and summaries |

## Requirements

- Python 3.x
- See `requirements.txt`: pandas, matplotlib, seaborn, scikit-learn, openpyxl

## Run

1. `cd customer-segmentation`
2. `pip install -r requirements.txt`
3. Put `online_retail_II.xlsx` in the project folder.
4. `jupyter notebook customer-segmentation.ipynb` — run cells top to bottom.
