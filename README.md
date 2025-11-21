📊 BigQuery Analytics Pipeline

A beginner-friendly but professionally structured analytics pipeline that simulates how data flows into BigQuery for downstream analysis.
Built using Python, Pandas, and a mock BigQuery layer, so it works on any machine without needing Google Cloud.

🚀 Project Overview

This project demonstrates the core steps of a data engineering analytics workflow:

Extract CSV data

Transform the data with Python + Pandas

Load into a Mock BigQuery Warehouse (simulating a real DWH)

Display aggregated results

This mirrors the daily workflow of data engineers working with GCP BigQuery, Data Lakes, and analytical pipelines — exactly the type of work PayPay, LINE, Yahoo!, and other Japanese fintech companies do.

🧠 Why This Project Matters

It shows you understand:

Data extraction & file-based ingestion

Data cleaning & transformation

Analytical SQL-style aggregation with Python

Warehouse loading patterns

Structuring a real data engineering project

Recruiters will view this as evidence you understand ETL fundamentals.

🧱 Architecture Diagram
┌─────────────┐      ┌──────────────┐      ┌────────────────────────┐
│   CSV File   │ ──► │  ETL Script  │ ──► │  BigQuery Mock Storage │
└─────────────┘      └──────────────┘      └────────────────────────┘

Extract   →   Clean   →   Aggregate   →   Load

📁 Project Structure
bigquery-analytics-pipeline/
│── data/
│    └── transactions.csv
│
│── pipeline/
│    └── bigquery_mock.py
│
│── main.py
│── requirements.txt
│── README.md

🧪 Example Result

The pipeline outputs a mock BigQuery table:

=== 📦 BigQuery Mock Storage ===

Table: customer_totals
   customer_id  amount
0          101   35.98
1          102    5.99
2          103  199.99

🛠️ Technologies Used

Python 3.11+

Pandas

PyArrow

Mock BigQuery API

CSV ingestion

No cloud account needed — this simulates the full workflow locally.

⚙️ Setup & Run
1️⃣ Install requirements
pip install -r requirements.txt

2️⃣ Run the pipeline
python main.py


The result prints instantly to your terminal.

🧩 How It Works
✔ Extract

Reads incoming CSV data containing transaction logs.

✔ Transform

Cleans data

Removes bad rows

Aggregates totals per customer

✔ Load

Loads results into a mock BigQuery object that behaves like a table storage layer.

✔ Display

Prints final BigQuery-style table.

🌱 Future Enhancements

These are great additions if you want to expand the project later:

Export aggregated table into Parquet

Add SQL querying layer

Add Airflow orchestration

Integrate actual BigQuery if you get a GCP free trial

Write unit tests for transformations

🙋‍♂️ Author

Christian Fletcher
GitHub: https://github.com/CFletcher00
