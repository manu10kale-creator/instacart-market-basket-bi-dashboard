📊 Instacart Market Basket Analysis — Python + Power BI Dashboard

A BI + Analytics project exploring consumer behavior, product trends, and affinity insights.

🚀 Overview

This project analyzes 3.4M+ Instacart grocery orders using Python for data preparation and Power BI for dashboarding.
It highlights:

Customer shopping behavior

Top-selling products

Reorder patterns & loyalty

Product pairing / affinity analysis

KPI-driven business insights

This project is designed to showcase BI, analytics, and data storytelling skills—ideal for data/ML/BI job portfolios.

🧠 Key Features
🔹 Interactive Power BI Dashboard

Total Orders

Total Users

Average Basket Size

Reorder Rate (%)

Orders by Hour of Day

Orders by Day of Week

Top 10 Most Ordered Products

Product Affinity Matrix (Market Basket Analysis)

Slicers for Product, Aisle, Department

🔹 Python Data Preparation

Efficient loading of 32M+ rows (memory optimized)

Extraction of top products

Calculation of reorder probabilities

Generation of product co-occurrence pairs

Creation of clean CSVs for Power BI import

🔹 Data Modeling

Star schema with:

order_products_prior (fact)

products, orders (dimensions)

top_products, aisle_counts, user_reorder_rate, product_pairs (aggregated insight tables)

Clean relationships optimized for Power BI

DAX measures for KPIs and ranking

🔹 Business Insights

Peak shopping hours: 10 AM – 3 PM

Reorder rate around 59%, indicating strong loyalty

Fresh produce dominates top product categories

Product pairs reveal promo/bundle opportunities

📁 Repository Structure
instacart-market-basket-bi-dashboard/
│
├── README.md
├── notebook/
│   └── instacart_preprocessing.ipynb
│
├── data_prepared/
│   ├── top_products.csv
│   ├── aisle_counts.csv
│   ├── user_reorder_rate.csv
│   └── product_pairs.csv
│
└── screenshots/
    ├── 1.png
    └── 2.png

⚠️ PBIX File

GitHub does not allow uploading large PBIX files.
You can place your file in Google Drive and link it below:

📁 Power BI Dashboard (PBIX):
https://drive.google.com/file/d/1FALHlDtjH7HlLFo7GyQ_fQg0r3O2d_NX/view?usp=sharing

📊 Dashboard Preview


![Dashboard Screenshot](screenshots/2.png)
![Data Model](screenshots/1.png)

📦 Dataset

Dataset source (Kaggle):
https://www.kaggle.com/competitions/instacart-market-basket-analysis

Raw dataset is NOT included in this repo due to size limits.

🧮 Key DAX Measures
Total Orders = COUNT(orders[order_id])

Total Users = DISTINCTCOUNT(orders[user_id])

Avg Basket Size =
DIVIDE(
    COUNTROWS('order_products__prior'),
    DISTINCTCOUNT('order_products__prior'[order_id])
)

Reorder Rate =
AVERAGE('order_products__prior'[reordered])
)

🛠 Tech Stack

Python: Pandas, Numpy

Power BI: DAX, data modeling, visualization

Jupyter Notebook for transformation

Market Basket Analysis (affinity pairs)

🎯 What This Project Demonstrates

Ability to work with large datasets (32M rows)

Data modeling and star schema design

Business-focused analytics and KPI development

Clear storytelling via BI dashboards

Practical ML-adjacent insight generation (product pairs, reorder prediction logic)

🧑‍💼 For Recruiters / Interviewers

This project reflects skills in:

BI & dashboarding

Python transformation

DAX modeling

Consumer analytics

Data storytelling

Recommender system basics

📌 How to Use

Clone the repo

Open the Python notebook to see preprocessing steps

Load CSVs in Power BI

Open the dashboard (via Google Drive PBIX link)

Explore slicers & visuals

✨ Author

Hrishi Kale
