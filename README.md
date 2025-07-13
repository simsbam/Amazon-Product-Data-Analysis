# Amazon-Product-Data-Analysis

## Project Background
In this project, I analyzed an e-commerce dataset  product listings on Amazon. The goal was to perform data cleaning, business analysis, and dashboard reporting to answer executive-level questions and provide strategic insights.

The workflow followed the full data analysis pipeline:
- Data Cleaning (Excel)
- Data Analysis using Pivot Tables
- Dashboard Visualization
- Insight Extraction & Executive Reporting

This project demonstrates practical application of Excel for real-world data issues like:
- Cleaning inconsistent product names
- Extracting meaningful category information
- Handling text-based review IDs
- Generating KPI insights from messy data

## Data Structure & Initial Checks
### Dataset Overview
The dataset includes over 1465 Amazon product listings with the following key columns:
- product_name
- category
- actual_price
- discounted_price
- discount_percentage
- rating
- rating_count 
- rating_count
- review_id 

### Data Cleaning steps in Excel
1. Product Name Cleanup
   - Used formulas like =LEFT(A2,FIND(" ",A2)-1) to extract first word for clarity.
   - Removed extra text after special characters using:
     =TRIM(RIGHT(SUBSTITUTE(A2, "|", REPT(" ", 100)), 100))

2. Category Simplification
   - Extracted shorter category names using string formulas.
   - Created unique product-category pairings.

3. Blank Handling
   - Used Go To Special > Blanks to identify and clean blank cells.
   - Filled or removed rows based on completeness.

4. Review & Rating Fields
   - Converted review ID (text) to count using COUNTA.
   - Converted ratings and discounts to number format for math operations.

## Executive Summary
### Overview of Key Findings
Top-Rated Products: Identified 5 products with highest rating × review count.
High Discount Watch: 340+ products had discounts of 50% or more — flagged for margin review.
Average Discount: Overall average discount across all products was ~47%.
Category Leaders: Electronics & Apparel had the highest number of listed products and reviews.
Rating–Discount Relationship: No strong linear correlation, but products rated 4.0+ often had moderate discounts.
Price Segmentation: Products under ₹200 had fewer reviews; higher engagement started around ₹500+.

Below is the overview page from the Excel dashboard and more are included in the interactive dashboard can be downloaded 
![Dashboard overview](https://github.com/simsbam/Amazon-Product-Data-Analysis/blob/main/Dashboard%20Overview.png)

### Key Metrics Answered via Pivot Tables
1. Average discount % by category – Used AVERAGE on discount by category in pivot.
2. Products per category – Count of product names per category.
3. Total number of reviews per category – SUM of review count.
4. Highest average ratings – Sorted pivot by average rating.
5. Avg actual vs discounted price by category – Clustered chart comparison.
6. Top reviewed products – LARGE function or pivot sort by review count.
7. Products with 50%+ discounts – Used COUNTIF([discount], ">=50%").
8. Rating distribution – Bar chart showing frequency of 3.0, 4.0, 5.0 ratings.
9. Potential revenue – actual_price × rating_count summed per category.
10. Product count by price range – Bucketed using IF:
    =IF(price<200,"<₹200",IF(price<=500,"₹200–₹500",">₹500"))
11. Discount vs Rating Analysis – Scatter chart for visual correlation.
12. Products with <1,000 reviews – Used COUNTIF([rating_count], "<1000").
13. Categories with highest discounts – Max discount percentage grouped by category.
14. Top 5 Products (Rating × Reviews) – Created a new column for combined score, sorted pivot table.

Below is the overview page from the Pivot Table

### Dashboard Features
The dashboard was built using:
- Pivot Charts: Column, bar and pie chart.
- KPI Cards: Simulated using text boxes and formatted cells for:
  - Total Reviews
  - Avg. Discount
  - Total Products
  - Top Rated Product
- Slicers: Added for interactive filtering by category.
- Clean Layout: Executive-friendly color scheme, minimal clutter, and clear labeling.
  
### Tools Used
- Excel: Data cleaning, pivot tables, formulas, and dashboarding.

### Recommendations for Stakeholders
- Focus marketing on top 5 products with highest review × rating score.
- Reassess pricing on high-discount, low-rating products.
- Increase visibility for mid-range (₹200–₹500) products with high ratings.
- Encourage reviews for top-rated, low-engagement products via post-purchase email campaigns.



