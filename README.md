# Sales Data Analysis using Python and Pandas

## Project Overview
This project performs basic data analysis on a sales dataset using Python and the Pandas library. The main objective is to understand how to work with real-world data by loading, exploring, cleaning, and analyzing a dataset.

The dataset contains information such as product name, quantity sold, and price. Using Pandas, the data is processed to calculate important metrics like total revenue, highest sale, lowest sale, and best-selling product.

This project demonstrates how Python can be used for data analysis similar to spreadsheet tools like Excel but with more flexibility and automation.

---

## Tools and Technologies
- Python
- Pandas Library
- Jupyter Notebook
- Visual Studio Code
- GitHub

---

## Project Structure

```
week3-sales-analysis
│
├── sales_analysis.ipynb
├── sales_data.csv
├── analysis_report.md
├── README.md
└── requirements.txt
```

### File Description

**sales_analysis.ipynb**  
Jupyter Notebook that contains the Python code used for loading, cleaning, and analyzing the dataset.

**sales_data.csv**  
The dataset used for performing the sales data analysis.

**analysis_report.md**  
Detailed explanation of the project, analysis steps, and findings.

**requirements.txt**  
List of required Python libraries needed to run the project.

**README.md**  
Overview and instructions for the project.

---

## Setup Instructions

### 1. Install Python
Download Python from the official website:

https://www.python.org/downloads/

Check installation using:

python --version

### 2. Install Required Libraries

Install pandas using pip:

pip install pandas

(Optional if using Jupyter Notebook)

pip install notebook

### 3. Open the Project
1. Open **Visual Studio Code**
2. Click **File → Open Folder**
3. Select the project folder.

### 4. Run the Notebook

Open the notebook file:

sales_analysis.ipynb

Run each cell using:

Shift + Enter

---

## Data Analysis Steps

### 1. Import Libraries
The Pandas library is imported to perform data manipulation and analysis.

import pandas as pd

### 2. Load Dataset
The dataset is loaded using the `read_csv()` function.

df = pd.read_csv("sales_data.csv")

This converts the dataset into a Pandas DataFrame.

### 3. Explore the Dataset
Basic exploration is done to understand the dataset.

- df.head() – Shows first few rows  
- df.shape – Shows number of rows and columns  
- df.info() – Shows column names and data types  

### 4. Data Cleaning
The dataset is checked for missing values and duplicate records.

df.isnull().sum()

df.drop_duplicates()

Cleaning ensures that the dataset is accurate and ready for analysis.

### 5. Create Total Sales Column
A new column is created to calculate the total sales value.

df["Total_Sales"] = df["Quantity"] * df["Price"]

### 6. Calculate Key Metrics

Total Revenue

total_revenue = df["Total_Sales"].sum()

Highest Sale

highest_sale = df["Total_Sales"].max()

Lowest Sale

lowest_sale = df["Total_Sales"].min()

Best Selling Product

best_product = df.groupby("Product")["Quantity"].sum().idxmax()

---

## Key Findings

From the analysis, the following insights were obtained:

- The **total revenue** shows the overall sales generated from the dataset.
- The **best-selling product** indicates the product with the highest quantity sold.
- The **highest sale value** represents the most profitable transaction.
- The **lowest sale value** shows the smallest sale recorded.

These insights help understand sales performance and product demand.

---

## Technical Details

Programming Language: **Python**

Library Used: **Pandas**

Data Structure Used: **Pandas DataFrame**

A DataFrame is a two-dimensional table-like data structure used for storing and analyzing structured data efficiently.

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

## Conclusion
This project demonstrates how Python and the Pandas library can be used for analyzing real-world datasets. The dataset was successfully loaded, explored, cleaned, and analyzed to generate meaningful insights such as total revenue and best-selling product.

The project highlights the importance of data analysis in understanding business performance and supporting better decision-making.