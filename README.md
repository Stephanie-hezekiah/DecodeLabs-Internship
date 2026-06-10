# DecodeLabs-Internship 
Data Analysis Project 2

### PROJECT TITLE: Data Cleaning, Analysis, Querying and Visualization using Microsoft Excel and PowerBI Query

[Status](https://img.shields.io/badge/Status-Complete-success)

[Project Overview](#project-overview)

[Data Sources](#data-sources)

[Tools Used](#tools-used)

[Data Cleaning and Transformation](#data-cleaning-and-transformation)
 
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


### Data Cleaning and Transformation
---
Before analysis, the raw dataset underwent a rigorous cleaning process in Excel and Power BI (Power Query) to ensure "one version of the truth."

1. Handling Date Inconsistencies

The raw data contained empty cells on the coupon code column.

•	Action: Remove all empty cells to avoid getting errors.

•	Tool: Excel "Text-to-Columns" and Power Query "Locale-based Transformation."

2.Data Validation

•	Duplicate Removal: Scanned for and removed duplicate transaction IDs to avoid overstating revenue.

•	Outlier Check: Verified that the 2.5 Million unit price for Laptops was correct and not a typing error (confirmed via product catalog).

3. Descriptive Statistical Profiling:

I implemented core statistical distributions to establish baseline metrics (Mean, Median, Mode and Count distributions) for purchase volumes and pricing models.

4. Multi-Dimensional Pivot Aggregations:

i. I developed dynamic Pivot Tables to segment variables across cross-sections of the business.

ii. I aggregated revenue metrics to isolate top performing product categories (identifying Chairs and Printers as leading gross earners at over $195,600 each).

iii. I also grouped transaction velocities by payment funnels to identify volume density (e.g., establishing that Online Payments and Credit Cards capture the highest financial shares with 731 and 712 items ordered respectively).

5. Data Modelling

I implemented a Star Schema to optimize performance, this design decouples transactional metrics (numerical facts) from the contextual attributes (dimensions) that describe them.

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

1. Data Integrity Auditing & Forensic Profiling: The primary step of the EDA process involved assessing the structural completeness and accuracy of the dataset.

i. Schema Consistency Validation: Evaluated the data types across all rows to verify that numeric keys, transaction tracking integers, alpha-numeric order strings, and localized address lines conformed to explicit column rules.

ii. Duplicate and Null Verification: Profiled primary identifier fields (OrderID, TrackingNumber) to ensure unique constraints were maintained, preventing data inflation or fragmented analytics downstream.

iii. Mathematical Integrity Check: Implemented formula audits across the derived metric field (TotalPrice). By cross-calculating $(\text{Quantity} \times \text{UnitPrice})$ programmatically against the recorded totals, the data model was verified to be free from rounding drifts, truncations, or corrupted baseline metrics.

2. Descriptive Statistical Analysis: Descriptive metrics were compiled to profile center-tendencies and spatial spreads across core transactional vectors.

i. Financial Performance Bounds: Grouping total transaction outputs yielded a definitive gross revenue capture of $1,264,761.96 across a footprint of 3,535 physical units shipped.

ii. Order Distribution Mechanics: Analyzed purchasing volume densities via unit counts per transaction line (Quantity). This process mapped the standard inventory depletion cycles, exposing heavy cluster segments around retail buyers while mapping corporate supply lines characterized by bulk individual orders.

iii. Pricing Architecture Ranges: Segmented product unit costs (UnitPrice) to evaluate the pricing distribution spectrum—ranging from everyday workspace assets to premium enterprise infrastructure equipment.

3. Categorical Variables & Transaction Descriptors: With foundational numeric distributions anchored, variables were cross-examined across distinct transactional fields:

i. Product Segmentation Velocity: Aggregations isolated product demand profiles. Chairs ($195,620.11) and Printers ($195,612.61) emerged as the primary gross revenue drivers, while high-velocity categories like Laptops ($192,126.55) and Tablets ($186,568.95) demonstrated sustained market volume.

ii. Payment Gateway Share: Evaluating checkout channels revealed a balanced distribution of consumer financial preferences. Credit Cards paced revenue collection at $263,847.63, followed closely by Online Payments at $262,442.94 and Cash checkouts at $259,786.29.

4. Operational & Marketing Attribution Cross-Examination: The final phase of EDA involved analyzing multi-variable relationships to map how customer acquisition efforts translated into operational outcomes.

i. Funnel-to-Promo Conversions: By plotting ReferralSource paths against dynamic CouponCode identifiers, the analysis illuminated specific conversion trends. Top-of-funnel networks like Instagram and Facebook heavily utilized instant-incentive triggers (such as SAVE10 and FREESHIP), while Email campaigns sustained consumer baskets through focused seasonal offers like WINTER15.

ii. Fulfillment Pipeline Health: Analyzing distribution vectors by tracking OrderStatus across payment paths and geographical points isolated potential leakage points. Quantifying systemic status spreads (Delivered, Shipped, Pending, Cancelled, Returned) allowed the business to identify exactly where logistic delays or payment processing friction were occurring.

Tools Used for EDA
---

•	Excel/Calc: Used for initial filtering, pivot tables to check column totals, and conditional formatting to highlight duplicates.

•	Power BI Power Query: Used for "Column Quality" and "Column Distribution" profiling to visualize data health.

During the Exploratory Data Analysis phase in Excel, I utilized:

•	Histograms to analyse the distribution of Unit Price, identifying a wide variance between high-end hardware and peripherals.

•	Scatter Plots to validate the correlation between Sales and Profit, confirming a standardized 20% margin across all categories.

•	Pivot Tables to identify the West Region as the primary revenue driver before moving to Power BI for advanced modelling


### Key Core Analytics & Findings
---

1. Product Segment Performance: Aggregate revenue analysis shows remarkably balanced demand across major categories, with high-ticket electronics and foundational workspace furniture driving gross revenue:

i. Top Revenue Drivers: Chairs ($195,620.11) and Printers ($195,612.61) lead the product categories in total gross earnings.

ii. Volume Analysis: Laptops ($192,126.56) and Tablets ($186,568.95) maintain high demand density, validating a strong consumer tech market share.

2. Payment Gateway Optimization: An evaluation of financial checkout funnels reveals a highly diversified preference structure among consumers:

i. Credit Cards stand as the primary value vehicle, capturing $263,847.63 across 712 items.

ii. Online Payments exhibit the highest transaction volume, moving 731 items for a total gross value of $262,442.94.

iii. Cash Checkouts retain competitive transaction velocity with 753 items fulfilled ($259,786.29), indicating that alternative or localized settlement methods remain vital.

3. Marketing Acquisition & Promo Tracking: By evaluating the intersection of ReferralSource and CouponCode, the analysis maps exactly how marketing touchpoints convert:

i. Social channels (Instagram and Facebook) drive high top-of-funnel engagement, converting heavily via immediate-incentive codes like SAVE10 and FREESHIP.

ii. Email Marketing serves as a reliable retention mechanism, demonstrating strong average basket values through targeted seasonal codes (WINTER15).


### Contact
---
•	LinkedIn: https://www.linkedin.com/in/hezekiah-stephanie-11061422a/

•	Email: stephaniehezekiel@gmail.com

•	Portfolio: https://github.com/Stephanie-hezekiah


