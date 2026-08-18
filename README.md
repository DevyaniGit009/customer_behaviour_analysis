# customer_behaviour_analysis
# Customer Shopping Behavior Analysis

## Overview

This project analyzes customer shopping behavior using a dataset of **3,900 transactions**. The goal is to understand customer spending patterns, product preferences, discounts, subscriptions, shipping behavior, and customer segments.

## Tools & Technologies

* Python
* Pandas
* PostgreSQL
* SQLAlchemy
* SQL
* Power BI

## Project Workflow

### 1. Data Loading & Exploration

The dataset is loaded using Pandas and explored using:

* `df.head()`
* `df.info()`
* `df.describe()`
* Missing-value analysis

### 2. Data Cleaning

The project includes:

* Handling missing values in the **Review Rating** column using the median rating within each product category.
* Converting column names to **snake_case**.
* Standardizing the `purchase_amount` column.
* Checking redundant columns and removing `promo_code_used`.

### 3. Feature Engineering

Two new features were created:

* **age_group** – Customers are divided into four age groups.
* **purchase_frequency_days** – Purchase frequency is converted into numerical days for analysis.

### 4. PostgreSQL Integration

The cleaned Pandas DataFrame is connected to PostgreSQL using **SQLAlchemy** and loaded into the `customer_analysis` database for further SQL-based analysis.

### 5. SQL Analysis

SQL analysis is used to answer business questions such as:

* Revenue by gender
* Subscribers vs. non-subscribers
* Top-rated products
* Shipping type comparison
* Customer segmentation
* Discount-dependent products
* Repeat buyers and subscriptions
* Revenue by age group

### 6. Power BI Dashboard

An interactive Power BI dashboard was created to visualize the customer shopping behavior and communicate key business insights.

## Key Insights

The analysis focuses on:

* Customer spending behavior
* Product performance
* Subscription behavior
* Discount usage
* Customer loyalty
* Revenue by age group
* Shipping preferences

## Business Recommendations

* Increase subscription adoption through exclusive benefits.
* Develop loyalty programs for repeat customers.
* Review discount strategies to balance sales and margins.
* Promote top-rated and best-selling products.
* Target high-revenue customer groups.

## Project Structure

```text
Customer-Shopping-Behavior-Analysis/
│
├── DA_project.ipynb
├── customer_shopping_behavior.csv
├── README.md
└── PowerBI_Dashboard/
```

## How to Run

1. Clone this repository.
2. Install the required Python libraries.
3. Open `DA_project.ipynb` in Jupyter Notebook or Google Colab.
4. Update the dataset path in the notebook.
5. Run the data cleaning and feature engineering cells.
6. Configure your local PostgreSQL database.
7. Run the PostgreSQL connection and data-loading section.
8. Open the Power BI dashboard to explore the results.
