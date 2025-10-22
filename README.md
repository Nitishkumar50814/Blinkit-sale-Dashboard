# Blinkit-sale-Dashboard

# Blinkit Sales Dashboard

![Blinkit Dashboard](Blinkit%20Snapshot.png)

## Project Title
**Blinkit Sales Dashboard** — Customer & outlet performance analysis using Power BI.

## Short Description / Purpose
Yeh dashboard Blinkit ke sales data ko visualise karta hai taaki business decisions le sakte hain — jaise top-selling categories, outlet type performance, item-level trends, aur seasonal/yearly filters. Mukhya purpose: **quick business insights** for product managers, category leads, aur ops teams.

## Tech Stack
- **Visualization:** Power BI (Desktop / Service)  
- **Data Processing:** Power Query (in Power BI)  
- **Data Source / Storage:** Excel / CSV (local), agar chaha to SQL / BigQuery se bhi connect kar sakte hain  
- **Tools for analysis (optional):** Python (pandas) / Jupyter for preprocessing  
- **Repo & Docs:** GitHub (README + dashboard snapshot)

## Data Source
- Primary: `sales_data.csv` (example)  
- Typical columns:
  - `OrderID`, `OrderDate`, `Year`
  - `OutletID`, `OutletType`, `OutletSize`, `OutletLocationType`
  - `ItemID`, `ItemType`, `ItemFatContent`
  - `Quantity`, `ItemPrice`, `TotalSale` (Quantity * ItemPrice)
  - `Rating`

> Note: Agar aapka real dataset alag ho to column mapping README ya ETL step mein mention karein.

## Features / Highlights
- **Key metrics cards:** Average Rating, Total Sales, Total Quantity, Unique Items.
- **Filter panel:** Year-wise filter (2011–2016) for time-based analysis.
- **Bar charts:** Sum of Sales by Outlet Type, Outlet Size, Item Type.
- **Donut / Pie:** Outlet Location Type, Item Fat Content distribution.
- **Detailed insight:** Category-wise sales (Fruits & Veg, Snack Foods, Frozen Foods, etc.) with annotated values.
- **Design:** Dark theme with highlighted KPI cards for quick glance.

## Example Insights (from this snapshot)
- **Total Sales:** 122.22K  
- **Average Rating:** 3.93  
- **Top categories:** Fruits & Vegetables, Snack Foods  
- **Item Fat Content:** Low fat contributes ~65% of sales  
- **Outlet Contribution:** Tier 2 outlets here show 100% in this dataset (dataset-specific)

## How to reproduce key metrics (example code snippets)

### Using pandas (Python)
```python
import pandas as pd

df = pd.read_csv('sales_data.csv')
df['TotalSale'] = df['Quantity'] * df['ItemPrice']

# Total sales
total_sales = df['TotalSale'].sum()

# Average rating
avg_rating = df['Rating'].mean()

# Unique items
unique_items = df['ItemID'].nunique()

# Sum of sales by item type
sales_by_item_type = df.groupby('ItemType')['TotalSale'].sum().sort_values(ascending=False)
