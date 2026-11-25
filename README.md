# Data Mining Project

This project explores an e-commerce retail transactions dataset through data cleaning, data warehousing, OLAP analysis, and customer churn prediction.

## Team

| Name | Enrollment No. |
| --- | --- |
| R. Venkata Siva | 2302320153 |
| Podili Anil | 2302320114 |
| D. Ramesh | 2302320099 |

## Project Files

| File | Description |
| --- | --- |
| `experiment-1-section-a-b-c.ipynb` | Main notebook for data preparation, warehouse design, OLAP analysis, and churn prediction. |
| `data.csv` | Raw retail transaction dataset (541,909 rows, 8 columns). |
| `fact_sales.csv` | Sales fact table (392,692 rows, 7 columns). |
| `dim_customer.csv` | Customer dimension (4,338 customers), including RFM metrics and categories. |
| `dim_product.csv` | Product dimension (3,922 products). |
| `dim_date.csv` | Date dimension (305 date records). |

## Getting Started

Install the notebook dependencies:

```bash
python -m pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

Open `experiment-1-section-a-b-c.ipynb` in Jupyter and run the cells from the project directory so the notebook can load `data.csv` and the generated CSV files.

## Workflow and Results

1. **Data cleaning and preprocessing:** Removed 5,268 duplicate rows, filtered 9,251 cancelled transactions (invoice numbers starting with `C`), and retained 524,878 valid sales records. Detected 37,827 unit-price outliers using the IQR method.
2. **Data warehouse:** Built a star schema with sales fact and customer, product, and date dimensions; checked primary- and foreign-key integrity.
3. **OLAP analysis:** Performed roll-up (yearly sales), drill-down (year/month sales), slice (2011), dice (Q1 2011 transactions with `TotalAmount > 100`), and pivot (monthly revenue by year).
4. **Customer churn prediction:** Trained a Random Forest classifier on 3,370 customers using a 90-day cutoff and an 80/20 train/test split. Reported results: 64.39% accuracy, 57.14% precision, 68.97% recall, 62.5% F1 score, and 0.7089 ROC-AUC.
