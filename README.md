# DecodeLabs-Internship 
Data Analysis Project 2

### PROJECT TITLE: Data Cleaning, Analysis, Querying and Visualization using Microsoft Excel and PowerBI Query

[Status](https://img.shields.io/badge/Status-Complete-success)

[Project Overview](#project-overview)

[Data Sources](#data-sources)

[Tools Used](#tools-used)

[Data Cleaning & Transformation](#data-Cleaning-and-transformation)
 
[Data Virtualization](#data-virtualization)

[Exploratory Data Analysis](#exploratory-data-analysis)

[Contact](#contact)


### Project Overview
---
This repository contains the data, analysis, and key findings for Project 2: Exploratory Data Analysis (EDA) as part of the DecodeLabs Industrial Training Program.

Key Objectives:

•	The objective of this project is to transition from raw transactional metrics into structured business intelligence.

•	By interrogating an e-commerce transactional dataset, this analysis uncovers underlying purchasing patterns, monitors fulfillment efficiencies, evaluates coupon marketing performance, and identifies critical customer behavior trends.


### Data Sources
---
The data set was given by our tutors


### Tools Used
---
Power BI: Data Modeling, DAX (Time Intelligence), and Visualization.

Excel Office: Initial data exploration and cleaning.


### Data Cleaning & Transformation
---
Before analysis, the raw dataset underwent a rigorous cleaning process in Excel and Power BI (Power Query) to ensure "one version of the truth."

1. Handling Date Inconsistencies

The raw data contained three different date formats (DD/MM/YYYY, DD-MMM-YYYY, and YYYY-MM-DD).

•	Action: Standardized all entries to a unified Date format to enable Time Intelligence functions.

•	Tool: Excel "Text-to-Columns" and Power Query "Locale-based Transformation."

2. Text Normalization

The Region, Category, and Product columns had inconsistent casing and hidden characters (e.g., "North\t", "EAST", "computers").

•	Action: Applied TRIM, CLEAN, and UPPER (Proper Case) functions to ensure categories grouped correctly in charts.

•	Result: Prevented duplicate categories like "Mobile" and "mobile" from appearing separately.

3. Feature Engineering (New Columns)

To meet the case study requirements, I created several calculated columns:

•	Total Sales: [Units Sold] * [Unit Price]

•	Total Profit: [Total Sales] * 0.2 (Applying the 20% margin requirement).

•	Date Table: Created a separate Calendar Table in Power BI with columns for Year, Quarter, Month, and Fiscal Period to support YTD and YoY analysis.

4. Data Validation

•	Duplicate Removal: Scanned for and removed duplicate transaction IDs to avoid overstating revenue.

•	Outlier Check: Verified that the 2.5 Million unit price for Laptops was correct and not a typing error (confirmed via product catalog).

Data Modelling

I implemented a Star Schema to optimize performance and simplify the DAX calculations.

•	Fact Table: Sales (Cleaned transactions).

•	Dimension Tables: Pivot


### Data Virtualization
---
The final stage of this project involved creating an interactive Power BI Dashboard designed to provide executive-level insights at a glance.

1. The Visual Hierarchy

I designed the dashboard using a "top-down" approach:

•	KPI Cards (The "What"): Placed at the very top to show Total Sales, Total Profit, and Units Sold instantly.

•	Time Intelligence Trends (The "When"): A line chart showing Sales performance over months, allowing stakeholders to see the February peak.

•	Categorical & Regional Breakdowns (The "Where" & "Who"): Using Bar Charts and Treemaps to compare how Categories (Computers vs. Mobile) and Regions (West vs. North) are performing.

2. Key Dashboard Features

•	Interactive Slicers: Added slicers for Region, Category, and Sales Rep, allowing users to filter the entire report by specific segments.

•	Dynamic Tooltips: Implemented tooltips that show the Profit Margin % when hovering over any product category.

•	Drill-Through Capabilities: Enabled users to click on a specific Region to see a detailed breakdown of the Sales Reps and Customers within that zone.

3. Design Principles Applied

•	Color Theory: Used a consistent color palette where Sales are represented in one primary color and Profit in another, reducing cognitive load.

•	Data-to-Ink Ratio: Removed unnecessary gridlines and borders to keep the focus entirely on the data insights.

•	Accessibility: Ensured high contrast between text and backgrounds for better readability.
Visual Insights Derived

•	Strategic Gap: The dashboard clearly visualized that while Computers have high value, Mobile devices drive store traffic (highest Units Sold).

•	Performance Tracking: By using YoY Growth indicators, I highlighted that the West Region isn't just the biggest, but also the fastest-growing.


### Exploratory Data Analysis
---
This phase involved a deep dive into the dataset to understand the underlying distributions and relationships between variables.

1. Data Profiling & Quality Audit

•	Volume Check: Analyzed 100 rows of transactions with 10 variables (Date, Region, Product, etc.).

•	Data Integrity: Identified inconsistencies in the Date column where formats varied between DD/MM/YYYY, DD-MMM-YYYY, and YYYY-MM-DD.

•	Missing Values: Audited the Profit and Sales columns to ensure no null values would skew the final KPIs.

2. Descriptive Statistics

I calculated the "Big Three" for the key numerical columns (Sales, Units Sold, Unit Price):

•	Mean (Average): To understand the typical transaction value.

•	Median: To identify if high-end "Computers" were skewing the average.

•	Range: Identifying the cheapest item vs. the most expensive (e.g., $65,000 Peripherals vs. $2,500,000 Laptops).

3. Distribution & Relationship Analysis

•	Category Breadth: Verified that the business sells across 6 distinct categories, with Computers being the highest value.

•	Regional Spread: Confirmed that sales are distributed across North, South, East, and West, ensuring the Time Intelligence comparisons would be statistically valid for all zones.

•	Sales vs. Profit Correlation: Verified a consistent 20% margin across the dataset, confirming that profit scales linearly with sales volume.

4. Outlier Detection

•	Identified that February 2025 contained an unusually high volume of sales compared to other months. During EDA, I investigated if this was a data entry error or a legitimate sales peak (it was confirmed as a peak).

Tools Used for EDA

•	Excel/Calc: Used for initial filtering, pivot tables to check column totals, and conditional formatting to highlight duplicates.

•	Power BI Power Query: Used for "Column Quality" and "Column Distribution" profiling to visualize data health.

During the Exploratory Data Analysis phase in Excel, I utilized:

•	Histograms to analyse the distribution of Unit Price, identifying a wide variance between high-end hardware and peripherals.

•	Scatter Plots to validate the correlation between Sales and Profit, confirming a standardized 20% margin across all categories.

•	Pivot Tables to identify the West Region as the primary revenue driver before moving to Power BI for advanced modelling


### Contact
---
•	LinkedIn: https://www.linkedin.com/in/hezekiah-stephanie-11061422a/

•	Email: stephaniehezekiel@gmail.com

•	Portfolio: https://github.com/Stephanie-hezekiah


