# Mobile-Sales-Dashboard
This Power BI project provides a complete analytical view of Mobile Sales Performance across multiple brands, models, cities, and payment methods.
The dashboard includes interactive KPIs, trend analysis, geospatial visuals, MTD reporting, and YoY comparisons, giving stakeholders actionable insights into business performance.

This repository contains the Power BI report file (.pbix), dataset, and documentation.

📂 Dashboard Pages

The report consists of 3 interactive pages:

1️⃣ Main Dashboard

Total Sales, Total Quantity, Transactions, and Average Selling Price

City-wise Sales Map

Monthly Trends

Customer Rating Analysis

Payment Method Distribution

Sales by Mobile Brand & Model

Sales by Day of Week

2️⃣ MTD (Month-To-Date) Report

MTD Sales, Quantity, Transactions, and Average Price

MTD Trend by Year, Quarter, Month & Day

Dynamic performance patterns visible for each month

3️⃣ Same Period Last Year Comparison

Current Year vs Same Period Last Year

Breakdown by Year, Quarter, and Month

YoY growth and seasonality trends

🛠️ Tools & Technologies Used
Tool	Purpose
Power BI Desktop	Visualization & DAX modeling
Power Query	Data cleaning & transformation
DAX	Time intelligence, KPIs & advanced calculations
Excel	Data source
Custom Calendar Table	Accurate YTD/MTD/YoY calculations
📐 Data Model (Star Schema)

The report uses a clean Star Schema structure:

Fact Table

Mobile_Sales_Data (Sales, Quantity, Transactions, Dates, Model, Brand)

Dimension Tables

Date (Custom Calendar)

Brand

City

Mobile Model

Payment Method

This ensures optimized performance and accurate time intelligence.

🧮 Key DAX Measures
Total Sales = SUM(Mobile_Sales_Data[Sales])

Total Quantity = SUM(Mobile_Sales_Data[Quantity])

Average Price = DIVIDE([Total Sales], [Total Quantity], 0)

MTD Sales = TOTALMTD([Total Sales], 'Date'[Date])

Sales LY = CALCULATE([Total Sales], SAMEPERIODLASTYEAR('Date'[Date]))

YoY Growth % =
DIVIDE([Total Sales] - [Sales LY], [Sales LY], 0)

📊 Key Insights

✔ Apple & Samsung are top-performing brands
✔ UPI & Debit Card dominate payment methods
✔ Sales peak on weekends (higher demand)
✔ MTD trend shows monthly seasonality
✔ YoY comparison highlights strong growth in later months
✔ City-level sales gaps offer targeted business opportunities

📦 Project Deliverables

📁 Mobile Sales Power BI Dashboard (.pbix)

📊 Fully automated KPIs & time intelligence

🔍 Interactive slicers & drillthrough

🗺️ City-based geospatial insights

📈 MTD & YoY performance comparison

🧠 Actionable business insights

🧑‍💻 How to Use

Download the .pbix file from this repository

Open in Power BI Desktop

Refresh the data source (Excel/CSV if provided)

Explore all 3 report pages & interactive visuals

🌟 Conclusion

This Power BI project provides a powerful analytics solution enabling better decision-making, real-time performance tracking, and strategic planning. The dashboard is designed with clean visuals, optimized DAX measures, and a user-friendly layout ready for business use.
