# Data Analyst - Bidur
# Project Description: Data Wrangling for Rental Standards Analytics in Downtown Vancouver
# Project Title: Data Wrangling for Enhanced Rental Standards Analytics in Downtown Vancouver
# Objective: 
The primary goal of this project is to clean, transform, and consolidate rental property data to enable accurate analysis of by-law compliance issues in Downtown Vancouver. By preparing a structured and reliable dataset, this project aims to facilitate data-driven decision-making for policymakers and city planners.
# Background: 
The dataset, "Rental Standards - Current Issues," is sourced from the City of Vancouver’s Open Data Portal (2025). It includes information on licensed rental properties, by-law violations, and property locations. However, raw data often contains missing values, inconsistencies, and redundant records, necessitating a rigorous data wrangling process.
# Dataset Description: 
The dataset “Rental standards - current issues” utilize the following data attributes for data analysis.
-	businessoperator: Landlord or owner of the rental property.
-	detailurl: Webpage address for additional information on current by-law issues.
-	streetnumber: Number for street where the business is located.
-	street: Name of street where the business is located.
-	totaloutstanding: The number of unresolved by-law violations.
-	totalunits: The total number of rental units in a building.
-	geom: Spatial data indicating the property’s location.
-	geo_local_area: The planning area where the property is located.
-	geo_point_2d: Location in 2D. 

# Methodology:
## 1.	Data Collection:
-	Acquired dataset from the City of Vancouver Open Data Portal.
- Stored the dataset in an AWS S3 bucket for further processing.
## 2.	Data Assessment:
-	Identified missing values in key attributes such as business operator names and geographical coordinates.
-	Detected duplicate records and inconsistent formatting in location fields.
-	Documented column data types and necessary transformations.
## 3.	Data Cleaning:
-	Removed rows where business operator names were missing, as these entries lacked essential identifying information.
-	Replaced missing values in geographical columns (Geom, Local Area, Geo-point-2d) with null values.
-	Standardized column naming conventions to camel case for consistency.
## 4.	Data Transformation:
-	Converted relevant columns to appropriate data types (e.g., converting date fields and numerical attributes for analysis).
-	Derived new attributes, such as total outstanding issues per property and categorized property types for segmentation.
-	Filtered records to retain only properties located in Downtown Vancouver.
## 5.	Data Integration & Storage:
-	Processed data using AWS Glue ETL pipeline for efficient transformation.
-	Created a Glue Data Catalog to store metadata for optimized querying.
-	Summarized key metrics using AWS Athena and stored the processed data in an S3 curated bucket.
## 6.	Validation & Quality Assurance:
-	Performed exploratory data analysis (EDA) to verify data integrity.
-	Cross-checked aggregated results against raw records to ensure consistency.
-	Generated summary statistics to confirm successful cleaning and transformation.
# Tools & Technologies:
- AWS Services: S3 (storage), Glue (ETL processing), Athena (querying), Glue Data Catalog (metadata management), AWS EC2 (virtual computing), AWS Beanstalk (app deployment).
- Tableau: Data visualization and dashboard creation for rental compliance insights.
- SQL: Aggregation and querying of structured data.
# Deliverables:
-	A cleaned and structured dataset with improved consistency and accuracy.
-	A data wrangling report documenting processing steps, challenges, and transformations applied.
-	Summary tables and visualizations to illustrate key data quality improvements.
# Timeline:
-	Week 1: Data collection and initial assessment.
-	Week 2-3: Data cleaning and transformation.
-	Week 4: Data integration and validation.
-	Week 5: Final reporting and visualization.

This data wrangling project provides a high-quality dataset that supports an in-depth analysis of rental property by-law compliance in Downtown Vancouver. The cleaned and structured data enables policymakers to address regulatory gaps, strengthen enforcement strategies, and improve rental housing standards effectively. Future enhancements may include integrating historical datasets to analyze trends over time and developing predictive models to identify high-risk non-compliant properties.
