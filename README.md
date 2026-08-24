# Superstore Profitability Audit --- Python

## 📊 Project Overview

This project uses **Python, Pandas, NumPy, and Matplotlib** to perform a
profitability audit of the Superstore dataset.

The analysis focuses on understanding how discounting relates to
profitability and identifying major drivers of profit loss across
**categories, sub-categories, products, and regions**.

> **Business goal:** Increase **profitable sales**, not simply sales volume.

## 🎯 Business Questions

1.  Is the business profitable overall?
2.  How does discounting affect profitability?
3.  Which categories and sub-categories generate the highest losses?
4.  Which products contribute most to the losses?
5.  Which regions are most affected?
6.  What actions can improve profitability?

## 🛠️ Tools & Technologies

-   Python
-   Pandas --- data cleaning, grouping, aggregation, and analysis
-   NumPy --- numerical calculations
-   Matplotlib --- business visualization

## 🔍 Analysis Workflow

**Data Profiling → Data Preparation → Profitability Analysis → Discount
Analysis → Loss Analysis → Product/Region Drill-down → Pareto Analysis →
Business Recommendations**

### 1. Data Profiling & Preparation

The dataset was reviewed for dimensions, data types, missing values,
duplicates, and numerical statistics. `Order Date` was converted to
datetime and additional fields were created for **Order Year, Order
Month, and Order Quarter**.

### 2. Overall Profitability

Calculated KPIs include:

-   Total Sales
-   Total Profit
-   Total Orders
-   Total Customers
-   Profit Margin

**Profit Margin = Total Profit / Total Sales × 100**

### 3. Category & Sub-Category Profitability

Sales, profit, and profit margin were analyzed across categories and
sub-categories to identify where losses were concentrated.

### 4. Discount & Profitability Analysis

Discount levels were analyzed using orders, sales, profit, and profit
margin.

A key finding was that **profitability deteriorates as discount levels
increase**. Discounts of **40% and above** were particularly damaging to
profitability in this dataset.

This identifies an association between aggressive discounting and margin
erosion; it does not by itself establish causality.

### 5. Product-Level Loss Analysis

Products were analyzed using:

-   Orders
-   Sales
-   Profit
-   Average Discount
-   Profit Margin

The analysis identified the top loss-making products for further pricing
and discount review.

### 6. Discount-Related Loss Analysis

Loss-making records were isolated and `Loss_Contribution` was calculated
from the absolute value of negative profit.

Losses were then analyzed across:

-   Region
-   Category
-   Sub-Category
-   Product

### 7. Pareto Analysis

A Pareto-style analysis calculated:

-   Loss Contribution %
-   Cumulative Loss %

Approximately **179 product-level records were required to reach 80% of
the total discount-related loss**.

This indicates that the loss problem is broadly distributed across the
product portfolio rather than being caused by only a handful of
products.

### 8. Regional Profitability

Profitability was analyzed across regions to identify geographical
differences in performance and potential differences in discount policy
and product mix.

## 📈 Key Business Insights

### 1. Discounting is a major profitability driver

Profitability declines sharply as discount levels increase, with
aggressive discounts producing substantial losses.

### 2. High discounts require tighter controls

Discount levels of **40% and above** are associated with significant
negative profitability and should receive stronger pricing controls.

### 3. Losses are concentrated in specific product areas

Several products and sub-categories repeatedly generate negative profit
and should be reviewed for pricing and discount strategy.

### 4. Discount-related losses are broadly distributed

Approximately **179 product-level records account for 80% of
discount-related losses**, indicating a systemic rather than isolated
problem.

### 5. Regional performance differs

Profitability varies across regions, suggesting that discount policies
and product mix should also be evaluated geographically.

## 💡 Business Recommendations

1.  **Introduce discount thresholds** --- Require additional review for
    discounts above a defined threshold, particularly 40% or more.
2.  **Review loss-making products** --- Investigate products with
    consistently negative profit and high discount rates.
3.  **Optimize product-level pricing** --- Use historical margin
    performance to establish minimum profitable selling prices.
4.  **Review sub-category strategy** --- Focus corrective action on
    sub-categories with persistent negative profitability.
5.  **Monitor discount profitability regularly** --- Track discount,
    sales, profit, margin, and loss contribution.
6.  **Shift from revenue-focused to margin-focused decisions** --- High
    sales should not automatically be considered successful if they
    generate negative profit.

## 📂 Project Structure

``` text
superstore-profitability-audit-python/
├── Superstore Profitability Audit.py
└── README.md
```

## ▶️ How to Run

### 1. Install dependencies

``` bash
pip install pandas numpy matplotlib
```

### 2. Add the Superstore dataset

Place the Superstore CSV file in your local directory.

### 3. Update the dataset path

Update the `pd.read_csv()` path in the Python script to match your local
dataset location.

### 4. Run the script

The script generates KPI calculations, profitability analysis, discount
analysis, loss analysis, Pareto analysis, and Matplotlib visualizations.

## 📌 Portfolio Highlights

This project demonstrates:

-   Data profiling
-   Data preparation
-   Datetime manipulation
-   Pandas GroupBy and aggregation
-   KPI calculation
-   Profit margin analysis
-   Multi-dimensional analysis
-   Loss contribution analysis
-   Ranking and sorting
-   Cumulative percentage calculations
-   Pareto analysis
-   Business-focused visualization
-   Translating analytical findings into business recommendations

## 🧠 Analyst Takeaway

The key lesson is that **revenue alone is not enough to evaluate
business performance**.

A business can generate strong sales while simultaneously destroying
margin through aggressive discounting.

The analysis therefore shifts the focus from:

> **How can we increase sales?**

to:

> **How can we increase profitable sales?**

## 👩‍💻 Author

**Sheena Arora**

Data Analytics Portfolio Project

**Focus:** Python \| Pandas \| Business Analytics \| Profitability
Analysis
