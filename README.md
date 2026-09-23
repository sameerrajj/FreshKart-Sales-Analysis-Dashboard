# FreshKart Sales Analysis 🛒📊

An end-to-end sales analytics project for **FreshKart**, covering data cleaning, exploratory data analysis (EDA) in Python, and an interactive **Power BI** dashboard — built to uncover revenue and profit drivers across products, channels, and regions.

---

## 📌 Problem Statement

Analyze FreshKart's sales data to identify key revenue and profit drivers across products, sales channels, and regions, uncover seasonal trends and outliers, and evaluate performance against sales targets and budgets. The goal is to generate actionable insights for optimizing pricing and promotions, improving product and regional performance, and supporting sustainable growth.

---

## 🗂️ Repository Structure

```
freshkart-sales-analysis/
├── README.md
├── data/
│   ├── final.csv                                    # Cleaned, merged, analysis-ready dataset
│   └── FreshKart_Sales_Analysis_Sales_Dataset.xlsx   # Raw multi-sheet source data
├── notebooks/
│   └── FreshKart_Sales_Analysis.ipynb                # Data cleaning, feature engineering & EDA
├── dashboard/
│   └── FreshKart_Sales_Dashboard.pbix                # Interactive Power BI dashboard
└── screenshots/
    └── dashboard_overview.png                        # (add your dashboard screenshots here)
```

---

## 📊 About the Data

The raw dataset (`FreshKart_Sales_Analysis_Sales_Dataset.xlsx`) contains six sheets:

| Sheet | Description |
|---|---|
| `Sales Orders` | Core transaction-level order data |
| `Customers` | Customer names and identifiers |
| `Products` | Product catalog and cost details |
| `Regions` | Delivery region mapping |
| `State Regions` | State-to-region lookup |
| `2017 Budgets` | Budgeted targets by product for 2017 |

These were merged, cleaned, and feature-engineered into a single analysis-ready file: **`final.csv`**.

**Dataset snapshot:**
- 📅 **Date range:** Jan 2014 – Dec 2018
- 🧾 **~64,000** order line items
- 📦 **30** unique products
- 🧑‍💼 **175** customers across **47** states
- 🚚 **3** sales channels: Wholesale, Distributor, Export
- 🗺️ **4** regions: South, Midwest, West, Northeast

---

## 🧹 What Was Done

**1. Data Cleaning & Wrangling**
- Merged Sales Orders with Customers, Products, Regions, State Regions, and 2017 Budgets
- Dropped redundant index/key columns left over from the merges
- Standardized and renamed columns to a consistent `snake_case` format
- Handled missing values and restricted budget figures to 2017 records only (the only year budgets were available for)

**2. Feature Engineering**
- `total_cost` — unit cost × order quantity
- `profit` — revenue minus total cost
- `profit_margin_pct` — profit as a percentage of revenue

**3. Exploratory Data Analysis**
- Monthly revenue trend and seasonality analysis
- Top & bottom 10 products by revenue
- Revenue breakdown by sales channel
- Order value distribution
- Unit price distribution per product
- Top 10 states by revenue and order count
- Average profit margin by channel
- Top & bottom 10 customers by revenue, with revenue-vs-margin segmentation
- Correlation heatmap across numeric features (quantity, price, revenue, cost, profit)

**4. Power BI Dashboard**
- Interactive visualization layer built on top of the cleaned dataset, letting users filter and drill into revenue/profit performance by product, channel, region, and time period

---

## 🛠️ Tools & Libraries

- **Python** — Pandas, NumPy, Matplotlib, Seaborn
- **Jupyter Notebook**
- **Power BI Desktop**
- **Excel / CSV** for source and processed data

---

## 🚀 How to Run

1. Clone the repo:
   ```bash
   git clone https://github.com/<your-username>/freshkart-sales-analysis.git
   cd freshkart-sales-analysis
   ```
2. Install dependencies:
   ```bash
   pip install pandas numpy matplotlib seaborn openpyxl jupyter
   ```
3. Launch the notebook:
   ```bash
   jupyter notebook notebooks/FreshKart_Sales_Analysis.ipynb
   ```
4. Open `dashboard/FreshKart_Sales_Dashboard.pbix` in **Power BI Desktop** to explore the interactive dashboard.

---

## 📈 Dashboard Preview

<img width="1202" height="675" alt="image" src="https://github.com/user-attachments/assets/6316cc8f-b563-4a77-b389-0751942047a8" />


---

## 🔍 Key Insights

- Top-performing products and channels by revenue and margin
- Seasonal peaks/dips in monthly sales
- Which states/regions drive the most revenue vs. order volume
- How actual sales performed against 2017 budgeted targets

---

## 👤 Author

**[Sameer raj]**
[LinkedIn](https://www.linkedin.com/in/sameerrajj/) • [Gmail](sameer.raj3187@gmail.com)

---

## 📄 License

This project is for portfolio/educational purposes. Add a license (e.g. MIT) if you'd like others to freely reuse the code.
