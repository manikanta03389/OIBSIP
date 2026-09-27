# Customer Segmentation Analysis

**Oasis Infobyte SIP — Data Analytics Track — Level 1, Task 2**

## Objective
Apply clustering algorithms to segment an e-commerce company's customer base into distinct groups based on purchasing behaviour, enabling targeted marketing strategies.

## Contents
- `Customer_Segmentation.ipynb` — full analysis notebook (load → clean → RFM feature engineering → standardisation → elbow method → K-Means clustering → cluster visualisation → cluster profiling → marketing recommendations)
- `online_retail_II.csv` — dataset used
- `README.md` — this file

## Dataset
**Source:** [Online Retail II](https://archive.ics.uci.edu/dataset/502/online+retail+ii), UCI Machine Learning Repository.

Over 1 million transaction line-items from a UK-based online gift retailer, spanning December 2009 to December 2011. Columns: Invoice, StockCode, Description, Quantity, InvoiceDate, Price, Customer ID, Country.

> **Note on file size:** The raw CSV is ~90MB. GitHub allows files up to 100MB without Git LFS, so it should push fine, but it may take a minute depending on connection speed.

## Tech Stack
Python, pandas, numpy, scikit-learn (KMeans, StandardScaler), matplotlib, seaborn, Jupyter Notebook

## Methodology
1. Cleaned 1,067,371 raw transactions down to 805,549 valid ones across 5,878 identifiable customers (removed guest checkouts, cancelled orders, and invalid quantity/price rows).
2. Engineered **RFM features** (Recency, Frequency, Monetary) per customer.
3. Log-transformed and standardised the features before clustering.
4. Used the **Elbow Method** and **silhouette score** to select K=4 as the optimal number of clusters.
5. Applied **K-Means clustering** and profiled each resulting segment.

## Key Findings — Customer Segments
| Segment | Size | Avg Recency | Avg Frequency | Avg Monetary |
|---|---|---|---|---|
| **Champions** | 20.2% | ~27 days | ~19 orders | ~£11,014 |
| **At Risk** | 24.9% | ~228 days | ~5 orders | ~£2,002 |
| **Promising / New** | 21.3% | ~28 days | ~3 orders | ~£865 |
| **Hibernating / Lost** | 33.6% | ~396 days | ~1.4 orders | ~£326 |

Over half the customer base (58.5%) is either at-risk or fully dormant — retention marketing should be a top priority alongside acquisition.

## How to Run
1. Open `Customer_Segmentation.ipynb` in Jupyter Notebook / JupyterLab / VS Code.
2. Ensure `online_retail_II.csv` is in the same directory.
3. Run all cells top to bottom (`Kernel → Restart & Run All`). Note: clustering steps may take a few seconds longer than Task 1 given the dataset size (~1M rows before cleaning).

## Folder Placement (per OIBSIP guidelines)
Place this folder in your `OIBSIP` GitHub repo as:
```
OIBSIP/DataAnalytics-L1-CustomerSegmentation/
```