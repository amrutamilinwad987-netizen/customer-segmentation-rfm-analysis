# customer-segmentation-rfm-analysis
E-Commerce Customer Segmentation using RFM (Recency, Frequency, Monetary) analysis in SQL and Python.
# 🎯 E-Commerce Customer Segmentation via RFM Analysis (SQL & Python)

An end-to-end customer analytics project leveraging the **RFM (Recency, Frequency, Monetary)** framework to segment online retail customers based on purchasing behavior. This project analyzes transactional logs to identify high-value VIP buyers, at-risk customers, and inactive segments to optimize marketing and retention strategies.

---

## 📌 Business Problem & RFM Framework

E-commerce businesses need to tailor customer engagement rather than applying one-size-fits-all marketing. By evaluating customer value across three dimensions:

* **Recency (R):** How recently did the customer make a purchase? (Days since last transaction)
* **Frequency (F):** How often does the customer purchase? (Total distinct transactions)
* **Monetary Value (M):** How much money does the customer spend? (Total lifetime revenue)

---

## 📊 Customer Segmentation Mapping

Customers are scored on a scale of 1–5 across R, F, and M using quintiles, then grouped into actionable business segments:

| Segment Name | RFM Criteria | Business Strategy |
| :--- | :--- | :--- |
| **Champions / VIPs** | High R, High F, High M | Reward loyalty, offer early access to new products. |
| **Loyal Customers** | Moderate-High R, High F, High M | Cross-sell and upsell premium offerings. |
| **At Risk / About to Sleep** | Low R, Moderate F, High M | Send automated win-back emails and discount incentives. |
| **New Customers** | High R, Low F, Low M | Provide onboarding offers and welcome drip campaigns. |
| **Lost / Churned** | Low R, Low F, Low M | Minimize marketing spend; run re-engagement surveys. |

---

## 🛠️ Data Pipeline & Analytics Workflow

1. **Data Ingestion & Cleaning:** Filter out canceled orders (`InvoiceNo` starting with 'C'), remove negative/zero quantities and unit prices, and handle missing `CustomerID`s.
2. **Feature Engineering (SQL/Pandas):** Aggregate transaction timestamps, invoice counts, and total spend per `CustomerID`.
3. **Quantile Scoring:** Calculate N-tile thresholds (1 to 5 scores) for Recency, Frequency, and Monetary metrics.
4. **Segmentation Rule Mapping:** Classify composite RFM scores into customer tiers.

---

## 🧰 Tech Stack Used

* **Languages:** SQL, Python (3.x)
* **Libraries:** `pandas`, `numpy`, `matplotlib`, `seaborn`
* **Database/Engine:** PostgreSQL / SQLite / BigQuery
* **Tooling:** Jupyter Notebook / VS Code, GitHub
