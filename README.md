# High-Performance In-Memory Data Wrangling on Large-Scale Arrays Using `data.table`

## Project Objective

The objective of this project is to understand how large-scale enterprise transaction datasets can be processed and analyzed efficiently using the `data.table` package in R.

This project demonstrates high-performance in-memory data manipulation using reference semantics and the `:=` operator. Unlike traditional `data.frame` operations that may create copies of data, `data.table` updates data directly in memory, improving execution speed and memory efficiency.

The project uses a synthetic sales transaction dataset containing **500,000 transaction records** and performs data generation, cleaning, indexing, filtering, grouping, aggregation, business analysis, report generation, and visualization.

---

## Software Used

* **R Programming Language**
* **RStudio**
* **data.table Package**
* **Git**
* **GitHub**

### Package Restriction

Only the `data.table` package is used for data manipulation.

The following packages are not used:

* `dplyr`
* `tidyverse`
* `sqldf`
* `dbplyr`
* Other data manipulation packages

Visualizations are created using **Base R**.

---

## Dataset Description

A synthetic enterprise sales transaction dataset was generated using R.

### Dataset Size

* **Number of Transactions:** 500,000
* **Number of Columns:** 17
* **File Name:** `sales_transactions.csv`

### Dataset Columns

| Column        | Description                  |
| ------------- | ---------------------------- |
| TransactionID | Unique transaction number    |
| CustomerID    | Customer identifier          |
| CustomerName  | Customer name                |
| Gender        | Customer gender              |
| Age           | Customer age                 |
| ProductID     | Product identifier           |
| ProductName   | Product purchased            |
| Category      | Product category             |
| Quantity      | Number of products purchased |
| UnitPrice     | Price per unit               |
| Discount      | Discount percentage          |
| GST           | GST percentage               |
| PaymentMethod | Payment method used          |
| City          | Customer city                |
| State         | Customer state               |
| OrderDate     | Date of purchase             |
| SalesPerson   | Sales executive              |

---

## Project Tasks

### Task 1 – Generate the Dataset

* Generate 500,000 synthetic sales transactions.
* Save the dataset as `sales_transactions.csv`.
* Display the first 10 observations.
* Display the last 10 observations.
* Display dataset dimensions.
* Display dataset structure.

### Task 2 – Load and Explore the Dataset

* Load the dataset using `fread()`.
* Display first and last observations.
* Display column names.
* Check data types.
* Display summary statistics.
* Find missing values.
* Find duplicate records.
* Count unique customers.
* Count unique products.
* Count unique cities.

### Task 3 – Data Cleaning and Preparation

* Check missing values.
* Remove duplicate records.
* Rename columns.
* Reorder columns.
* Remove unnecessary columns if required.
* Convert columns into appropriate data types.
* Display the cleaned dataset.

### Task 4 – High-Speed Data Manipulation

* Select single columns.
* Select multiple columns.
* Filter rows using one condition.
* Filter rows using multiple conditions.
* Sort data in ascending order.
* Sort data in descending order.
* Display the top 20 expensive products.
* Display the top 20 transactions with the highest quantity.

### Task 5 – In-Place Column Updates Using `:=`

The following calculated columns were created:

* `Revenue`
* `DiscountAmount`
* `GSTAmount`
* `NetRevenue`

The `:=` operator was used to update the dataset directly in memory.

### Task 6 – Index Keying Using `setkey()`

* Create indexes for efficient searching.
* Create a key on `CustomerID`.
* Create a key on `ProductID`.
* Search transactions belonging to a specific customer.
* Search purchases of a specific product.
* Compare search performance before and after indexing.

### Task 7 – Grouping and Aggregation

Business reports were generated for:

#### Customer-wise Summary

* Total Orders
* Total Revenue
* Average Revenue

#### Product-wise Summary

* Total Quantity Sold
* Total Revenue

#### City-wise Summary

* Number of Transactions
* Total Revenue

#### Category-wise Summary

* Total Revenue
* Average Revenue

### Task 8 – Business Analysis

The following business questions were answered:

1. Which city generated the highest revenue?
2. Which product generated maximum sales?
3. Which customer placed the highest number of orders?
4. Which payment method is used most frequently?
5. What is the average transaction value?
6. Which category generated maximum revenue?
7. Who are the top 20 customers by revenue?
8. Which are the top 20 products by quantity sold?

### Task 9 – Export Reports

The following reports were exported as CSV files:

* `customer_summary.csv`
* `product_summary.csv`
* `city_summary.csv`
* `category_summary.csv`

### Task 10 – Visualization

The following plots were created using Base R:

* Transactions by City
* Revenue by Product Category
* Top 20 Customers
* Payment Method Distribution

All plots were saved in the `Output` folder.

---

## Steps to Run the Program

### Step 1: Install R and RStudio

Install:

* R
* RStudio

### Step 2: Install the `data.table` Package

Run the following command in RStudio:

```r
install.packages("data.table")
```

### Step 3: Clone the Repository

Clone the GitHub repository:

```bash
git clone <your-github-repository-url>
```

### Step 4: Open the Project

Open the project folder in RStudio.

### Step 5: Run the R Program

Run the R scripts in the following order:

```text
1. Task1_Generate_Dataset.R
2. Task2_Load_Explore.R
3. Task3_Data_Cleaning.R
4. Task4_Data_Manipulation.R
5. Task5_In_Place_Updates.R
6. Task6_Index_Keying.R
7. Task7_Grouping_Aggregation.R
8. Task8_Business_Analysis.R
9. Task9_Export_Reports.R
10. Task10_Visualization.R
```

### Step 6: Check the Output Files

After execution, the following files will be generated:

```text
sales_transactions.csv
customer_summary.csv
product_summary.csv
city_summary.csv
category_summary.csv
```

The visualization files will be saved inside the `Output` folder.

---

## GitHub Repository Structure

```text
Week2-data.table-project/
│
├── README.md
│
├── R/
│   ├── Task1_Generate_Dataset.R
│   ├── Task2_Load_Explore.R
│   ├── Task3_Data_Cleaning.R
│   ├── Task4_Data_Manipulation.R
│   ├── Task5_In_Place_Updates.R
│   ├── Task6_Index_Keying.R
│   ├── Task7_Grouping_Aggregation.R
│   ├── Task8_Business_Analysis.R
│   ├── Task9_Export_Reports.R
│   └── Task10_Visualization.R
│
├── Data/
│   └── sales_transactions.csv
│
├── Reports/
│   ├── customer_summary.csv
│   ├── product_summary.csv
│   ├── city_summary.csv
│   └── category_summary.csv
│
└── Output/
    ├── transactions_by_city.png
    ├── revenue_by_category.png
    ├── top_20_customers.png
    └── payment_method_distribution.png
```

---

## Output Screenshots

Add screenshots of the following outputs to the repository:

### Dataset Generation

* First 10 records
* Last 10 records
* Dataset dimensions
* Dataset structure

### Data Exploration

* Summary statistics
* Missing value results
* Duplicate record results

### Data Manipulation

* Filtered records
* Top 20 expensive products
* Top 20 highest-quantity transactions

### Business Reports

* Customer summary
* Product summary
* City summary
* Category summary

### Visualizations

Add screenshots of:

* Transactions by City
  <img width="100" height="100" alt="transactions_by_city" src="https://github.com/user-attachments/assets/06db37ad-cfa8-4417-95a3-acccc5ae977b" />

* Revenue by Product Category
  <img width="1000" height="700" alt="revenue_by_category" src="https://github.com/user-attachments/assets/668fa694-dd28-4128-aa44-f8f13070c027" />

* Top 20 Customers
  <img width="1200" height="800" alt="top_20_customers" src="https://github.com/user-attachments/assets/4b1b96d8-f000-4f6c-92a8-98a885ad79b5" />

* Payment Method Distribution
  <img width="1000" height="700" alt="payment_method_distribution" src="https://github.com/user-attachments/assets/f0fd01fc-421b-4054-8480-e56857d30474" />


Example:

```text
screenshots/
│
├── dataset_structure.png
├── customer_summary.png
├── product_summary.png
├── transactions_by_city.png
├── revenue_by_category.png
├── top_20_customers.png
└── payment_distribution.png
```

---

## Business Questions Solved

This project answers important business questions such as:

* Which city generates the highest revenue?
* Which products have the highest sales volume?
* Which customers generate the most revenue?
* Which customers place the highest number of orders?
* Which payment method is most frequently used?
* What is the average transaction value?
* Which product category generates the highest revenue?
* Which products have the highest quantity sold?

These insights can help organizations make better decisions related to:

* Customer targeting
* Product planning
* Sales performance
* Revenue optimization
* Regional performance
* Payment method strategy

---

## Learning Outcomes

After completing this project, the following concepts were learned:

* Generating large synthetic datasets in R.
* Importing large datasets using `fread()`.
* Exporting large datasets using `fwrite()`.
* Using `data.table` for high-performance data manipulation.
* Understanding reference semantics and in-memory updates.
* Using the `:=` operator to create and update columns efficiently.
* Filtering and sorting large datasets.
* Creating keys using `setkey()`.
* Performing fast indexed searches.
* Grouping and aggregating large datasets.
* Generating business reports.
* Performing business-oriented data analysis.
* Exporting reports to CSV format.
* Creating visualizations using Base R.
* Organizing and managing projects using Git and GitHub.

---

## Conclusion

This project demonstrates how the `data.table` package can be used to perform high-performance data wrangling and business analysis on large-scale transactional datasets.

By using in-memory processing, reference semantics, efficient indexing, grouping, aggregation, and fast file operations, `data.table` provides an efficient approach for analyzing hundreds of thousands or millions of records.

The project successfully demonstrates the complete data analytics workflow:

**Data Generation → Data Loading → Data Cleaning → Data Manipulation → In-Place Updates → Indexing → Aggregation → Business Analysis → Report Export → Visualization**
