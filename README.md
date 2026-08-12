🎯 Project Objectives
Store and manage real estate datasets using cloud storage.
Integrate AWS S3 with Snowflake.
Create and manage analytical tables in Snowflake.
Perform SQL-based analysis on real estate data.
Analyze property prices, rental trends, mortgage rates, and district-level performance.
Calculate rental yields and other business metrics.
Create analytical output tables for visualization.
Build an interactive Power BI dashboard.
Understand an end-to-end cloud data analytics workflow.
🗂️ Datasets
The project uses three main datasets.

1. District Prices Monthly
Contains monthly aggregated real estate market trends by district.
Key attributes include:
Year/Month
District
Administrative region
Secondary market price per square meter
New-build price per square meter
Rental price per square meter
Month-over-month price changes
Number of listings
Central Bank key rate
Average mortgage rate

3. Rentals
Contains individual rental property listings.
Key attributes include:
Property ID
Listing date
District
Administrative region
Latitude / Longitude
Total area
Number of rooms
Floor information
Building year
Building type
Renovation
Furnished status
Pets allowed
Deposit months
Metro station
Metro distance
Distance from city center
Monthly rent
Rent per square meter

3. Secondary Market
Contains individual resale property listings.
Key attributes include:
Property ID
Listing date
District
Administrative region
Latitude / Longitude
Total area
Living area
Kitchen area
Number of rooms
Floor information
Building year
Building type
Renovation
Furnished status
Parking
Metro accessibility
Distance from city center
Property price
Price per square meter

☁️ Cloud Data Pipeline
Step 1 — Dataset Management
The datasets were maintained in GitHub and uploaded to Amazon S3 for cloud-based storage.

Step 2 — AWS S3
Amazon S3 was used as the cloud storage layer for the project datasets.
Dataset → AWS S3 Bucket

Step 3 — Snowflake Integration
Snowflake was connected to the AWS S3 bucket using an external stage.
The datasets were then loaded into Snowflake tables for analysis.

AWS S3
   ↓
Snowflake External Stage
   ↓
Snowflake Tables

Step 4 — SQL Analysis
Analytical queries were written in Snowflake SQL to generate insights from the datasets.
The analysis includes:
Price trends
Rental trends
District comparisons
Property type analysis
Mortgage rate analysis
Rental yield analysis
Property characteristics
Listing trends

Step 5 — Power BI
The analytical output tables were imported into Power BI to create an interactive dashboard.
🧮 SQL Analysis
Snowflake SQL was used extensively for data analysis.
Techniques used include:
CTEs
Aggregations
GROUP BY
JOIN
Window Functions
DENSE_RANK()
PARTITION BY
QUALIFY
Calculated metrics
Percentage calculations
Example Analysis

Rental yield was calculated using:
Rental Yield (%) =
(Annual Rental Income / Average Property Price) × 100

The analysis combines rental and secondary-market information to identify districts with comparatively higher rental yields.

📊 Power BI Dashboard
The analytical results were visualized using Power BI.
The dashboard includes:
KPI cards
Price trend analysis
Rental price analysis
Mortgage rate trends
District-level comparisons
Property type analysis
Building type analysis
Rental yield analysis
Interactive filters and slicers

The dashboard was designed to help users explore real estate market trends from different perspectives.

🔍 Key Business Questions
The project investigates questions such as:

How do property prices vary across districts?
How have secondary-market and new-build prices changed over time?
Which districts have higher rental prices?
Which districts provide higher rental yields?
How are mortgage rates related to property prices?
Which building types are more common?
How does property size influence price?
How does proximity to metro stations affect rental properties?
Which districts have higher property listing activity?
What are the major trends in the real estate market?

🛠️ Technology Stack
Programming & Analysis:
Python
Pandas
NumPy
Matplotlib
Seaborn
Cloud:
Amazon S3
Data Warehouse:
Snowflake
Database & Analytics:
SQL
Visualization:
Power BI
Version Control:
Git
GitHub

📁 Project Structure
real-estate-data-analytics/
│
├── data/
│   ├── district_prices_monthly.csv
│   ├── rentals.csv
│   └── secondary_market.csv
│
├── python/
│   ├── data_cleaning.ipynb
│   └── exploratory_data_analysis.ipynb
│
├── sql/
│   └── analysis_queries.sql
│
├── powerbi/
│   └── dashboard/
│
├── reports/
│   └── project-report.pdf
│
├── screenshots/
│   └── dashboard.png
│
└── README.md

Update the folder names above to match the actual structure of your GitHub repository.

📈 Project Outcome
The project demonstrates an end-to-end cloud analytics workflow:
Data Collection
      ↓
Cloud Storage
      ↓
Data Warehouse
      ↓
SQL Analytics
      ↓
Business Metrics
      ↓
Power BI Visualization
      ↓
Business Insights

The project provides practical experience with:

Cloud data storage
Data warehousing
SQL analytics
Data transformation
Business intelligence
Data visualization
Cloud-to-BI workflows

🚀 Future Improvements
The current workflow involves some manual steps. Future improvements could include:
Automated data ingestion
Scheduled data pipelines
Snowpipe-based ingestion
AWS Glue-based ETL
Automated Power BI refresh
Real-time or near-real-time data integration
Data quality monitoring
Pipeline orchestration
👨‍💻 Author

Ranit Karmakar

B.Tech — Computer Science & Engineering (Data Science)
