# Sales Data Analysis using Python and Pandas

## Project Overview
This project performs basic data analysis on a sales dataset using Python and the Pandas library. The objective is to understand how to load, explore, clean, and analyze real-world data.

The dataset contains information such as product name, quantity sold, and price. Using Pandas, the dataset is analyzed to calculate key metrics such as total revenue, highest sale, lowest sale, and best-selling product.

This project demonstrates how Python can be used for efficient data analysis similar to spreadsheet operations.

---

## Setup Instructions

### 1. Install Python
Download Python from the official website:

https://www.python.org/downloads/

Verify installation using:

python --version

### 2. Install Required Libraries

Install pandas using pip:

pip install pandas

(Optional for Jupyter Notebook)

pip install notebook

### 3. Open Project in VS Code
1. Open Visual Studio Code  
2. Click **File → Open Folder**  
3. Select the project folder  

### 4. Run the Notebook
Open the notebook file:

sales_analysis.ipynb

Run each cell using:

Shift + Enter

---

## Code Structure

week3-sales-analysis
│
├── sales_analysis.ipynb
├── sales_data.csv
├── analysis_report.md
├── README.md
└── requirements.txt


### File Description

sales_analysis.ipynb – Jupyter notebook containing the data analysis code  
sales_data.csv – Dataset used for performing analysis  
analysis_report.md – Detailed project documentation  
README.md – Project overview and instructions  
requirements.txt – List of required Python libraries  

---

## Analysis Steps and Findings

### Step 1: Import Libraries
The Pandas library is imported to perform data manipulation and analysis.

import pandas as pd

### Step 2: Load Dataset
The dataset is loaded from the CSV file using the read_csv() function.

df = pd.read_csv("sales_data.csv")

### Step 3: Explore the Dataset
Basic exploration is performed to understand the dataset structure.

df.head() – Displays first few rows  
df.shape – Shows number of rows and columns  
df.info() – Displays column names and data types  

### Step 4: Data Cleaning
Missing values are checked using:

df.isnull().sum()

Duplicates are removed using:

df.drop_duplicates()

### Step 5: Create Total Sales Column
A new column is created to calculate the sales value.

df["Total_Sales"] = df["Quantity"] * df["Price"]

### Step 6: Calculate Key Metrics

Total Revenue

total_revenue = df["Total_Sales"].sum()

Highest Sale

highest_sale = df["Total_Sales"].max()

Lowest Sale

lowest_sale = df["Total_Sales"].min()

Best Selling Product

best_product = df.groupby("Product")["Quantity"].sum().idxmax()

### Findings
The analysis helps identify:
- Total revenue generated from sales
- The product with the highest number of sales
- The highest and lowest sales values

These insights help understand product performance and sales trends.

---

## Visual Documentation
Screenshots were captured while running the notebook to demonstrate the functionality of the project. These include:

- Dataset preview using df.head()
- Dataset information using df.info()
- Missing value detection
- Final output showing calculated sales metrics

---

## Technical Details

Programming Language: Python

Library Used: Pandas

Data Structure Used: Pandas DataFrame

A DataFrame is a two-dimensional table-like data structure used to store and manipulate structured data efficiently.

Key functions used in this project include:
- read_csv()
- head()
- info()
- isnull()
- drop_duplicates()
- groupby()
- sum()
- max()
- min()

---

## Testing Evidence

Test Case 1 – Dataset Loading  
The dataset was loaded using read_csv().  
Result: Dataset loaded successfully.

Test Case 2 – Missing Value Detection  
Missing values were checked using isnull().  
Result: Missing values correctly identified.

Test Case 3 – Sales Calculation  
Total sales were calculated using Quantity × Price.  
Result: Accurate sales calculations produced.

Test Case 4 – Best Selling Product  
groupby() was used to identify the product with the highest quantity sold.  
Result: Best-selling product identified successfully.

---

## Conclusion
This project demonstrates how Python and the Pandas library can be used to analyze real-world datasets. The dataset was loaded, explored, cleaned, and analyzed to generate useful insights such as total revenue and best-selling product.

The project highlights how data analysis techniques can help businesses understand their sales performance and make better decisions.