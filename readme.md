# Regional Sales Performance Analysis (2014–2018)

A comprehensive Exploratory Data Analysis (EDA) project focused on understanding multi-year regional sales performance, revenue drivers, profit dynamics, and budget adherence across the United States. The dataset spans 2014 to 2018 and includes multi-sheet information on sales orders, customer segmentation, products, regions, and budget allocations.

# Project Overview

This project investigates:

Revenue concentration and product performance

Margin behavior and pricing strategy patterns

Regional growth and budget vs. actual performance

Seasonal/monthly sales patterns

Customer & product segmentation insights

The analysis is structured to deliver market-intelligence-ready insights, aligning closely with expectations for roles in Business Analytics, Market Intelligence, and Strategy.

# Key Business Questions Addressed

1. What are the key drivers of revenue, and which products/regions adhere to the 80/20 (Pareto) Principle?

2. How do profit margins correlate with unit price, and is there evidence of tiered pricing strategies?

3. Are there recurring seasonal or monthly trends in sales volume that should inform inventory and marketing strategy?

4. Which regions and product lines represent the highest and lowest ROI (Budget vs. Actual Performance)?

# Data Engineering & Preparation Workflow

## Technical Stack

1. Language: Python

2. Libraries: Pandas (for data cleaning and manipulation), NumPy (for numerical operations), Matplotlib & Seaborn (for visualization).

## Data Preprocessing Steps

The workflow involved several critical steps to ensure data integrity and feature engineering:

1. Multi-Sheet Loading: All sheets (Sales Orders, Customers, Products, Regions, Budget) were loaded simultaneously using pd.read_excel(..., sheet_name=None).

2. Column Selection & Renaming: Selected core analytical features (e.g., Order No, Unit Price, Date, Quantity) and renamed them to a standard, lowercase format.

3. Feature Engineering: Created new time-series and financial features:

    revenue = Unit Price * Quantity

    order_month, order_month_name, and month_period from the Order Date column.

4. Data Validation & Merging: Handled missing budget values and ensured correct data types before merging all five dataframes using primary keys (Customer ID, Product ID, Region ID) to construct the Master Sales Dataset.

# Core Findings & Strategic Recommendations

The project yielded several high-impact insights for strategic adjustment:

## 1. Revenue Concentration (Pareto Principle):
1. Finding: Revenue exhibits strong adherence to the Pareto Principle. The top 5 products generate approximately 80% of the total revenue.

2. Recommendation: Increase production and marketing focus on these top-tier SKUs and evaluate the financial viability of discontinuing extremely low-performing products to optimize the product portfolio.

## Profitability Analysis

1. Finding: Profit margins range broadly (18% to 60%). The visual analysis (scatter plot of Profit Margin vs. Unit Price) revealed dense horizontal bands, strongly suggesting the company utilizes a standardized, tiered pricing model based on product category rather than unit cost variance.

2. Recommendation: Conduct a detailed review of the pricing tiers. Apply successful pricing levers from high-margin products to mid-tier products, aiming for margin uplift across the board.

## Regional Imbalance & Budget Adherence

1. Finding: The California region leads the market, contributing over 20% of total revenue. Furthermore, analysis of Budget vs. Actual revealed significant budget misalignment, with some regions consistently exceeding their targets while others consistently underperform.

2. Recommendation: Implement a strategy to diversify risk by investing targeted marketing and strategic resources into "medium-potential" states. Align annual budgets with actual historical performance patterns to ensure realistic target setting and KPI adherence.

## Seasonal and Trend Analysis

1. Finding: While no extreme monthly seasonality exists, a minor but recurring volume uptick is consistently observed in the May–June period. A notable anomaly was identified: a sharp revenue dip (approx. $21.2M) in early 2017.

2. Recommendation: Reallocate promotional spending to capitalize on the natural May–June peak. Conduct an urgent post-mortem analysis on the 2017 anomaly to prevent recurrence.
