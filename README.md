# Power BI Sales & Profitability Performance Dashboard
This repository contains an end-to-end Power BI performance reporting project designed to deliver dynamic insights into Sales, Gross Profit, and Quantity metrics.
The dashboard uses advanced DAX, switch measures, conditional formatting, and a well-structured data model to identify performance trends, pain points, and growth opportunities
## Data Overview
The dataset is a mock Excel-based model consisting of three interconnected tables

🔹 Sales (Fact Table) -  Contains transactional sales data

🔹 Account (Dimension Table) - Includes account-level attributes

🔹 Product (Dimension Table) - Describes product hierarchy

## Data Preparation
### Power Query (Cleaning & ETL)

- Renamed tables and columns

- Fixed incorrect data types

- Removed duplicate rows in dimension tables

### Data Modeling

- Built a virtual date table

- Added an in_past column to mark months before the latest sales date

- Created base measures for Sales, Quantity, COGS, Gross Profit, and GP%

- Built YTD and PYTD measures for time-intelligence

- Added switch measures to dynamically toggle between Sales, GP, and Quantity

- Added YTD_vs_PYTD comparison

## Treemap - Bottom 10 Countries (YTD vs PYTD):
#### Purpose: To pinpoint underperforming geographical areas.
#### Visual Choice: A Treemap was selected as it's excellent for visualizing hierarchical data and relative proportions, making it easy to see which countries are contributing most to the decline. 
#### Key Insight: Filtered to show the bottom 10 countries by the YTD_vs_PYTD comparison, this chart quickly identifies regions with significant sales or gross profit declines, enabling targeted investigation. 
## Waterfall Chart - Contribution to Variance:
#### Purpose: To break down the YTD_vs_PYTD difference by contributing factors.
#### Visual Choice: A Waterfall Chart is ideal for showing how an initial value is affected by positive or negative changes, leading to a final value. It vividly illustrates the drivers of the year-over-year change. 
#### Key Insight: Users can drill down by country and product type to understand specific products or regions driving the variance. 
## Line and Stacked Column Chart - Monthly Performance:
#### Purpose: To visualize monthly/quarterly trends and compare current year performance against the prior year.
#### Visual Choice: This combination chart effectively displays two different types of data (column for YTD values by product type, line for PYTD) on a single visual, allowing for direct comparison and trend analysis over time. 
#### Key Insight: It helps in identifying months or quarters where current year performance deviates from the prior year, broken down by product type. Markers and distinct colors enhance readability. 
## Scatter Chart with Zoom Slider - Account Profitability & Quantity:
#### Purpose: To segment accounts based on their profitability and sales/quantity performance.
#### Visual Choice: A Scatter Chart is perfect for identifying relationships between two numerical variables (GP_percent and Switch_YTD (Sales/Quantity)) and spotting outliers or clusters. The zoom slider feature is crucial for navigating dense data points.
#### Key Insight: This chart allows for the identification of:
Accounts with high sales/quantity but low gross profit percentage (potential profitability issues).
Accounts with low sales/quantity but high gross profit percentage (potential for growth initiatives).
The addition of average lines for GP% and Sales/Quantity provides benchmarks for easy segmentation.
## Conclusion & Key Findings
This Power BI dashboard offers dynamic insights into business performance. It successfully identifies underperforming regions, reveals specific drivers of year-over-year variance, and enables segmentation of accounts by profitability and sales volume. This comprehensive analysis provides actionable intelligence for strategic decision-making.
