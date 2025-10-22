# 1. Blinkit Sales Dashboard
![Blinkit-sale-Dashboard](Blinkit%20Sales%20Snapshot.png)
# Blinkit Sales Dashboard

# Project Title

## Blinkit Sales Dashboard — Customer and outlet performance analysis using Power BI.

# Short Description / Purpose

This dashboard visualizes Blinkit’s sales data to support better business decision-making — such as identifying top-selling categories, outlet performance, item-level trends, and yearly variations.
The main goal is to provide quick business insights for product managers, category leads, and operations teams.

# Tech Stack

### Visualization: Power BI (Desktop / Service)

### Data Processing: Power Query (inside Power BI)

### Data Source / Storage: Excel / CSV (local); optionally can connect with SQL or BigQuery

### Tools for Analysis (Optional): Python (Pandas) 

### Documentation: GitHub (README + Dashboard Snapshot)

# Data Source

#### Primary Dataset: sales_data.csv (example)

Typical Columns:

OrderID, OrderDate, Year

OutletID, OutletType, OutletSize, OutletLocationType

ItemID, ItemType, ItemFatContent

Quantity, ItemPrice, TotalSale (calculated as Quantity × ItemPrice)

Rating


# Features / Highlights

 KPI Cards: Average Rating, Total Sales, Total Quantity, Unique Items

Filter Panel: Year-wise filter (2011–2016) for time-based analysis

Bar Charts: Sum of Sales by Outlet Type, Outlet Size, and Item Type

Donut / Pie Charts: Outlet Location Type and Item Fat Content distribution

Detailed Insights: Category-wise sales (Fruits & Vegetables, Snack Foods, Frozen Foods, etc.) with annotated values

# Design: Dark theme with highlighted KPI cards for quick visual understanding

Insights (From This Dashboard)

Total Sales: 936.53K

Average Rating: 3.92

Top Categories: Fruits & Vegetables, Snack Foods

Item Fat Content: Low Fat items contribute approximately 65% of total sales

Outlet Contribution: Tier 2 outlets contribute 100% of total sales (dataset-specific insight)
