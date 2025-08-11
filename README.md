E-Commerce Sales Dashboard

📌 Overview
This project is an interactive Power BI dashboard built from an open-source Kaggle dataset. The dashboard analyzes e-commerce sales data, providing insights into revenue trends, customer behavior, and product performance from 2016 to 2018.

🗂 Dataset
Source: Kaggle E-Commerce Dataset

Tables Used:

Orders → Order details and timestamps

Order Items → Product-level sales details

Products → Product category and subcategory info

Customers → Customer demographic/location data

Sellers → Seller location and details

Date Table: Custom date table marked as a date table in Power BI for accurate time intelligence.

⚙️ Data Preparation
Loaded and cleaned the dataset in Power BI.

Created relationships between fact and dimension tables:

Orders[order_id] → Order Items[order_id] (One-to-Many)

Products[product_id] → Order Items[product_id]

Customers[customer_id] → Orders[customer_id]

Date[date] → Orders[order_purchase_timestamp]

Created calculated columns/measures for:

Total Revenue = SUM(Order Items[price]) + SUM(Order Items[freight_value])

Total Orders = DISTINCTCOUNT(Orders[order_id])

Average Order Value (AOV) = DIVIDE([Total Revenue], [Total Orders])

📊 Dashboard Features
Revenue Trends Over Time – Tracks monthly revenue from 2016 to 2018.

Top Product Categories – Highlights best-performing categories.

Geographic Distribution – Sales by customer state.

Order Status Breakdown – Shows delivered, canceled, and other order statuses.

Key Metrics Cards – Total Revenue, Total Orders, and Average Order Value.

🔍 Key Insights
Steady Growth: Orders and revenue increased steadily from 2016 to 2018, peaking in late 2017.

Top Categories: Electronics and furniture generated the highest total revenue.

Regional Concentration: Most sales originated from major urban states.

Customer Behavior: Average order value remained stable, suggesting consistent spending patterns.

🛠 Tools & Technologies
Power BI for dashboard creation and data modeling.

DAX for calculated measures and KPIs.

Kaggle for the raw dataset.
