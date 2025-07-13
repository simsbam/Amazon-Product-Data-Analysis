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
