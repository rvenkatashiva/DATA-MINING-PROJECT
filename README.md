# DATA MINING PROJECT

Data warehousing, OLAP analysis, and customer churn prediction using an e-commerce retail transactions dataset (`data.csv`).

## Group Members

| Name | Enrollment No |
| --- | --- |
| U.Rohan Reddy | 2402320145 |
| K.Tharun | 2402320148 |
| V.Bhupathi sai | 2402320146 |

## Project Files

- `experiment-1-section-a-b-c.ipynb` — Main Jupyter notebook covering data loading, cleaning, outlier detection, star schema data warehouse creation, RFM discretization, OLAP operations, and Random Forest churn prediction.
- `data.csv` — Raw retail transaction dataset (`541,909` rows, `8` columns).
- `fact_sales.csv` — Star schema sales fact table (`392,692` rows, `7` columns).
- `dim_customer.csv` — Customer dimension table (`4,338` customers) with RFM metrics and discretized categories.
- `dim_product.csv` — Product dimension table (`3,922` products).
- `dim_date.csv` — Date dimension table (`305` date records).

## Summary of Workflow & Results

1. **Data Cleaning & Preprocessing**: Removed `5,268` duplicate rows, filtered `9,251` cancelled transactions (`InvoiceNo` starting with `C`), and kept `524,878` valid sales records. Detected `37,827` unit-price outliers using IQR bounds.
2. **Data Warehouse (Star Schema)**: Built and verified `fact_sales`, `dim_customer`, `dim_product`, and `dim_date` tables with primary/foreign key integrity checks.
3. **OLAP Operations**: Implemented Roll-up (yearly sales), Drill-down (year/month sales), Slice (2011), Dice (Q1 2011 transactions with `TotalAmount > 100`), and Pivot (year-wise monthly revenue).
4. **Customer Churn Prediction**: Trained a `RandomForestClassifier` on `3,370` customers using a 90-day cutoff (`80/20` train/test split), achieving `64.39%` accuracy, `57.14%` precision, `68.97%` recall, `62.5%` F1 score, and `0.7089` ROC-AUC.
# DATA-MINING-PROJECT
