# Myntra Product Web Scraping & EDA

## Project Overview

This project focuses on collecting product data from Myntra using web scraping and performing Exploratory Data Analysis (EDA) using Python.

The analysis explores product prices, ratings, reviews, brands, and categories to identify useful trends and relationships in the collected data.

## Business Problem

Myntra has a large number of products across different categories, making it difficult to compare products based on price, ratings, reviews, and brands.

This project analyzes the collected product data to understand:

- Product distribution across categories
- Brands with the highest number of products
- Price and rating distributions
- Relationship between price, ratings, and reviews
- Differences in average prices and ratings across categories

## Objectives

- Collect Myntra product data using web scraping
- Clean and prepare the collected data
- Perform basic statistical analysis
- Perform Exploratory Data Analysis (EDA)
- Create visualizations to identify trends and patterns
- Apply statistical hypothesis testing
- Extract meaningful business insights

## Dataset

The final dataset contains:

- **550 records**
- **7 columns**

### Columns

| Column | Description |
|---|---|
| Rating | Product rating |
| Reviews | Number of product reviews |
| Brand | Product brand |
| Product_Name | Name of the product |
| Price | Product price in INR |
| Size | Product size |
| Category | Product category |

## Web Scraping

The product data was collected using Python web scraping techniques.

### Tools Used

- Python
- Selenium
- WebDriver
- BeautifulSoup
- Regular Expressions (Regex)
- Pandas

Selenium was used to automate the browser and handle dynamically loaded product data.

BeautifulSoup was used to parse HTML and extract required product information.

Regular expressions were used to extract and clean values such as product prices and review counts.

## Data Cleaning & Preprocessing

The following preprocessing steps were performed:

- Checked missing values
- Identified missing values in `Rating` and `Reviews`
- Retained missing `Rating` and `Reviews` because some products did not have ratings or reviews
- Converted columns to appropriate data types
- Removed extra spaces from text columns
- Cleaned the `Size` column
- Checked duplicate records

The cleaned dataset was then used for further analysis.

## Exploratory Data Analysis

EDA was performed using statistical methods and visualizations.

### Basic Analysis

Used:

- `value_counts()` to analyze product counts by category and brand
- `describe()` to calculate descriptive statistics such as mean, median, minimum, and maximum

### Visualizations

The following visualizations were created:

- Price Distribution
- Rating Distribution
- Top 10 Categories by Number of Products
- Top 10 Brands by Number of Products
- Price vs Rating
- Average Price by Top 10 Categories
- Average Rating by Top 10 Categories
- Price vs Reviews
- Price Distribution by Rating
- Average Reviews by Rating
- Correlation Heatmap
- Top 5 Categories Distribution

## Statistical Analysis

### One-Way ANOVA

ANOVA was used to compare average prices and average ratings across different product categories.

#### Category vs Price

- **F-statistic:** 3.8193
- **p-value:** 4.726 × 10⁻¹⁴

The p-value was less than 0.05, so the null hypothesis was rejected.

This indicates a statistically significant difference in average prices across categories.

#### Category vs Rating

- **F-statistic:** 30.3272
- **p-value:** 3.669 × 10⁻⁶⁵

The p-value was less than 0.05, so the null hypothesis was rejected.

This indicates a statistically significant difference in average ratings across categories.

### Pearson Correlation

Pearson correlation was used to measure the linear relationship between Price and Rating.

- **Correlation:** 0.2569
- **p-value:** 1.891 × 10⁻⁶

The result indicates a weak positive linear relationship between Price and Rating, which was statistically significant.

## Key Insights

- **Face Wash and Cleanser** had the highest number of products, with **98 products**.
- **ZAROON PRODUCTION** had the highest number of products among the top brands, with **39 products**.
- Most products had ratings between approximately **4.3 and 4.6**.
- Most products were priced below **₹1,000**, with a few high-price values.
- **Skin Care Combo** had the highest average price among the top 10 categories.
- **Lipstick** had the lowest average price among the top 10 categories.
- Most top categories had average ratings above **4.0**.
- The correlation between Rating, Reviews, and Price was weak, indicating no strong linear relationships among these variables.

## Project Workflow

```text
Web Scraping
      ↓
Data Collection
      ↓
Data Cleaning & Preprocessing
      ↓
Basic Statistical Analysis
      ↓
Exploratory Data Analysis
      ↓
Data Visualization
      ↓
Hypothesis Testing
      ↓
Business Insights
