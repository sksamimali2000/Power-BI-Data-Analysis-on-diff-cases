### 🔹 Data Model (Star Schema)  
![Data Model](images/model.png)

### 🔹 Currency-wise Sales Breakdown  
![Currency Report](images/currency_report.png)

### 🔹 Monthly Sales Trend  
![Monthly Trend](images/monthly_trend.png)

### 🔹 Customer-Level Revenue Contribution  
![Customer Breakdown](images/customer_breakdown.png)

📊 Power BI Sales Analysis Dashboard

🚀 End-to-end Power BI Analytics Project built from scratch – from raw data preprocessing → DAX modeling → stunning dashboards.
This project analyzes global sales data across multiple currencies, customers, and timelines to deliver actionable business insights.

🔑 Key Features

✨ Data Preprocessing & Modeling

Integrated multiple tables: fact_InternetSales, dim_Customer, dim_Currency, dim_Date, dim_Product.

Designed a Star Schema Model for efficient querying and reporting.

Cleaned and transformed large datasets for analysis-ready format.

✨ Dynamic Date Dimension with DAX

dim_Date = ADDCOLUMNS( 
    CALENDAR(MIN(fact_InternetSales[ShipDate]), MAX(fact_InternetSales[ShipDate])),
    "Year", YEAR([Date]),
    "Month", MONTH([Date]),
    "Month Name", FORMAT([Date], "MMM"),
    "Day of Week", FORMAT([Date], "DDDD"),
    "Quarter", FORMAT([Date], "Q"),
    "YearQuarter", FORMAT([Date], "YYYY") & "/Q" & FORMAT([Date], "Q")
)


✨ Visual Dashboards

🌍 Currency-wise Sales – Comparison of sales volume across USD, AUD, CAD, DEM, FRF, GBP.

📅 Monthly Sales Trend – Seasonal insights across 12 months with strong Q4 performance.

👥 Customer-Level Analysis – Revenue contribution broken down by individual customers.

📊 KPI Highlights – Total Sales, Currency distribution, and Month-over-Month growth.

📸 Project Snapshots
🔹 Data Model (Star Schema)

Efficient schema connecting Fact & Dimension tables.


🔹 Currency-wise Sales Breakdown

USD leads globally, followed by AUD – showing heavy reliance on US-based markets.


🔹 Monthly Sales Trend

Sales peak in November & December (Q4) 📈, highlighting strong year-end demand.


🔹 Customer-Level Revenue Contribution

Top customers drive over 13K+ each in sales, helping identify key accounts.


💡 Best Insights

🔥 Top Findings from Analysis

💵 USD dominates sales with over 146M+, followed by AUD.

📈 Q4 (Nov–Dec) contributes the highest sales, showing seasonal spikes in demand.

👥 Few customers contribute 13K+ individually, highlighting high-value accounts.

🌍 Sales are spread across 6 currencies, but USD and AUD account for ~90% of revenue.

📊 Yearly trends show consistent growth with clear seasonal peaks, supporting targeted promotions.

🛠 Tools & Technologies

Power BI Desktop – Data modeling & dashboarding

Excel / CSV – Data preprocessing

DAX – Calculations for Date table & KPIs

Star Schema Design – Optimized data model

📂 Project Structure
📦 PowerBI-Sales-Analysis
 ┣ 📊 Dashboard.pbix       # Power BI dashboard file
 ┣ 📑 README.md            # Project documentation
 ┣ 📁 Data                 # Processed datasets
 ┗ 📸 Snapshots            # Dashboard images

🚀 How to Use

Clone the repository

git clone https://github.com/yourusername/PowerBI-Sales-Analysis.git


Open Dashboard.pbix in Power BI Desktop

Refresh the data connections

Explore reports & dashboards 🎉

🌟 Key Learnings

Built a full-stack Power BI pipeline (ETL → Modeling → Dashboarding).

Mastered DAX for dynamic calculations (custom date table, KPIs).

Delivered business-ready insights on currency performance, seasonal trends, and customer contributions.

✨ If you found this project insightful, please ⭐ star the repo and share!
