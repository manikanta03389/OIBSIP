# EDA on Retail Sales Data

**Oasis Infobyte SIP — Data Analytics Track — Level 1, Task 1**

## Objective
Perform a thorough Exploratory Data Analysis on a retail sales dataset to uncover patterns, customer behaviour trends, and actionable business insights.

## Contents
- `EDA_Retail_Sales.ipynb` — full analysis notebook (load → inspect → descriptive stats → time series → customer segment/fulfillment analysis → product analysis → correlation heatmap → discount/profit insight → regional & sub-category breakdown → conclusion)
- `Sample - Superstore.csv` — dataset used
- `README.md` — this file

## Dataset
**Source:** [Superstore Dataset](https://www.kaggle.com/datasets/vivek468/superstore-dataset-final) by Vivek Chowdhury, Kaggle.

9,994 real orders from a US superstore, spanning **2014–2017**, with 21 columns: order/ship dates, ship mode, customer segment, geography (region, state, city), product category/sub-category/name, quantity, discount, sales, and profit.

> **Note:** This dataset does not include individual customer age or gender. The demographics section of the notebook analyses the customer attributes that are genuinely present in the data instead — customer segment (Consumer / Corporate / Home Office) and shipping mode preference — rather than fabricating fields that don't exist in the source.

## Tech Stack
Python, pandas, numpy, matplotlib, seaborn, Jupyter Notebook

## Key Findings
- Sales show genuine year-over-year growth with strong Q4 seasonality (holiday-driven retail pattern).
- The Consumer segment drives the majority of revenue; nearly 60% of orders use Standard (slower, cheaper) shipping.
- Revenue is well-balanced across Technology, Furniture, and Office Supplies — no single category dominates.
- **Discounts above 20% turn orders unprofitable** — 18.7% of all orders (1,871 orders) were sold at an outright loss, totaling -$156,131.
- **Tables and Bookcases** (Furniture sub-categories) are structurally unprofitable despite reasonable sales volume.
- The **South region** underperforms in order volume despite a comparable average order value to other regions.

## How to Run
1. Open `EDA_Retail_Sales.ipynb` in Jupyter Notebook / JupyterLab / VS Code.
2. Ensure `Sample - Superstore.csv` is in the same directory.
3. Run all cells top to bottom (`Kernel → Restart & Run All`).

## Folder Placement (per OIBSIP guidelines)
Place this folder in your `OIBSIP` GitHub repo as:
```
OIBSIP/DataAnalytics-L1-EDARetailSales/
```