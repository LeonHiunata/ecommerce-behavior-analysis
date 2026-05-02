# E-Commerce Behavior Analysis
> Analyzing 42M+ transactions from a multi-category e-commerce platform to uncover customer behavior patterns, revenue drivers, and actionable business insights.

![Python](https://img.shields.io/badge/Python-3.11-blue?logo=python)
![DuckDB](https://img.shields.io/badge/DuckDB-latest-yellow?logo=duckdb)
![Data](https://img.shields.io/badge/Data-42M%2B%20Rows-green)
![Size](https://img.shields.io/badge/Dataset-5.28GB-orange)

---

## Business Questions Answered

| # | Business Question | Method |
|---|---|---|
| 1 | Who are our most valuable customers? | RFM Segmentation |
| 2 | Which categories & brands drive the most revenue? | Revenue vs Volume Analysis |
| 3 | When is the best time to run flash sales? | Time Pattern & Heatmap |
| 4 | How well do we retain customers week over week? | Cohort Retention Analysis |
| 5 | Are there suspicious transactions or data anomalies? | IQR & Z-Score Detection |

---

## Key Findings

### Customer Segmentation
- **3M+ customers** segmented into 8 behavioral groups using RFM Analysis
- **Champions (17.6% of users)** generate **56.6% of total revenue** — Pareto principle confirmed
- **338K At-Risk customers** represent **$1.76B revenue at stake** — urgent win-back campaign needed

### Revenue Intelligence
- **Electronics dominates** at $6.65B (54% of total revenue)
- **Apple alone** generates $3.43B — more than Samsung + Xiaomi combined
- **Smartphones** account for 81.7% of electronics revenue ($5.43B)
- Clear gap between high-volume (appliances) vs high-value (computers) categories

### Time Patterns
- Peak transaction hours identified for optimal flash sale scheduling
- Weekly seasonality patterns detected across all major categories
- New vs returning user ratio tracked daily

### Retention Crisis
- **75.4% of users never return** after their first purchase (Week 0→1 drop)
- Retention stabilizes at ~20% from Week 2 onwards
- Critical window: **first 7 days** after acquisition is make-or-break

### Anomaly Detection
- Price outliers identified using IQR method
- Suspicious bot-like users flagged for fraud investigation
- Daily transaction anomalies detected using Z-Score analysis

---

## Project Structure
ecommerce-behavior-analysis/
├── 📁 data/
│   └── sample/          ← 0.5% sample data (public)
├── 📁 notebooks/
│   ├── 00_data_validation.ipynb
│   ├── 01_preprocessing.ipynb
│   ├── 02_eda_overview.ipynb
│   ├── 03_customer_segmentation.ipynb
│   ├── 04_revenue_analysis.ipynb
│   ├── 05_time_pattern.ipynb
│   ├── 06_cohort_analysis.ipynb
│   └── 07_anomaly_detection.ipynb
├── 📁 reports/figures/  ← All visualization outputs
├── 📄 requirements.txt
└── 📄 README.md

---

## ⚙️ Tech Stack

| Tool | Purpose |
|---|---|
| **Python 3.11** | Core programming language |
| **DuckDB** | High-performance SQL query engine for 42M rows |
| **Pandas / PyArrow** | Data manipulation & Parquet conversion |
| **Matplotlib / Seaborn** | Statistical visualizations |
| **GitHub** | Version control & portfolio hosting |

---

## 🚀 How to Run

```bash
# 1. Clone repository
git clone https://github.com/LeonHiunata/ecommerce-behavior-analysis.git
cd ecommerce-behavior-analysis

# 2. Create virtual environment
python -m venv venv
venv\Scripts\activate       # Windows
source venv/bin/activate    # Mac/Linux

# 3. Install dependencies
pip install -r requirements.txt

# 4. Download dataset
# https://www.kaggle.com/datasets/mkechinov/ecommerce-behavior-data-from-multi-category-store?select=2019-Oct.csv

# 5. Place CSV in data/raw/ and run notebooks in order
# Start from 00_data_validation.ipynb
```

---

## 📊 Dashboard

> Tableau dashboard coming soon — will cover customer segmentation,
> revenue breakdown, and time pattern analysis.

---

## 💡 Business Recommendations

| Priority | Segment | Action | Expected Impact |
|---|---|---|---|
| HIGH | At-Risk (338K users) | Win-back campaign + exclusive discount | Recover $1.76B at-risk revenue |
| HIGH | One-time buyers | 2nd purchase trigger within 7 days | Improve Week 0→1 retention from 24.6% |
| 🟡 MED | New Customers (340K) | Onboarding flow + personalized reco | Convert to Loyal segment |
| 🟡 MED | Champions (532K) | Loyalty program + early access | Maintain 56.6% revenue base |
| 🟢 LOW | Lost segment | Aggressive discount or accept churn | Selective recovery only |

---

*Dataset source: [E-Commerce Behavior Data — Kaggle](https://www.kaggle.com/datasets/mkechinov/ecommerce-behavior-data-from-multi-category-store?select=2019-Oct.csv)*