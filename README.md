# 🐼 Python Pandas Data Analysis Projects

> **Data Technician Bootcamp | Python | pandas | Data Cleaning, Analysis & Visualisation**

![Python](https://img.shields.io/badge/Python-Data%20Analysis-blue?style=flat-square&logo=python&logoColor=white)
![pandas](https://img.shields.io/badge/pandas-Data%20Manipulation-150458?style=flat-square&logo=pandas&logoColor=white)
![Google Colab](https://img.shields.io/badge/Google-Colab-orange?style=flat-square&logo=googlecolab&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualisation-green?style=flat-square)

---

## 🔎 Overview

This repository contains **Python data analysis projects and exercises** completed during my Data Technician Bootcamp.

The work focuses on using **pandas** to explore, clean, filter and analyse datasets in Google Colab, alongside visualisation techniques using pandas plotting and **Matplotlib**.

Retail and sales-style datasets were used to practise turning raw data into structured information and useful analytical insights.

---

## 📂 Projects & Exercises

| Area | Focus |
|---|---|
| 🐼 **Pandas DataFrames** | Creating, loading and exploring tabular data |
| 🔍 **Filtering & Slicing** | Selecting rows and columns using conditions, `.loc[]` and `.iloc[]` |
| 🧹 **Data Cleaning** | Identifying and handling missing or incomplete values |
| 📊 **Data Analysis** | Grouping, aggregating and sorting data |
| 📈 **Data Visualisation** | Creating charts to identify patterns and trends |
| 🛍️ **Retail & Sales Analysis** | Exploring products, categories, sales and performance |

---

## 🐼 Working with pandas

pandas was used to load and work with structured datasets using **DataFrames**.

```python
import pandas as pd

df = pd.read_csv("sales_data.csv")

df.head()
```

Initial exploration included methods such as:

```python
df.head()
df.tail()
df.info()
df.describe()
df.shape
df.columns
```

These helped understand the structure, data types and contents of a dataset before further analysis.

---

## 🔍 Filtering Data

Conditional filtering was used to focus on records relevant to a particular question.

```python
high_sales = df[df["Sales"] > 500]
```

Multiple conditions could also be combined:

```python
filtered_data = df[
    (df["Category"] == "Technology") &
    (df["Sales"] > 500)
]
```

This allowed larger datasets to be narrowed down to specific products, categories, transactions or performance levels.

---

## ✂️ Selecting Data with `.loc[]` and `.iloc[]`

### `.loc[]`

`.loc[]` was used to select data using row and column labels.

```python
df.loc[:, ["Product", "Category", "Sales"]]
```

It can also be combined with conditions:

```python
df.loc[df["Sales"] > 500, ["Product", "Sales"]]
```

### `.iloc[]`

`.iloc[]` was used to select data based on numerical row and column positions.

```python
df.iloc[0:5, 0:4]
```

These techniques provided more control over which sections of a DataFrame were selected for analysis.

---

## 🧹 Data Cleaning

pandas methods were used to identify and manage missing values.

```python
df.isna().sum()
```

### Removing Missing Values

```python
df.dropna()
```

### Replacing Missing Values

```python
df["Sales"] = df["Sales"].fillna(0)
```

Cleaning data before analysis helps prevent incomplete records from affecting calculations and results.

---

## ↕️ Sorting Data

`sort_values()` was used to rank and organise records.

```python
df.sort_values("Sales", ascending=False)
```

This can be used to identify:

- Highest-selling products
- Lowest-performing products
- Largest transactions
- Top-performing categories

---

## 📊 Grouping & Aggregation

`groupby()` was used to summarise data across categories.

```python
category_sales = df.groupby("Category")["Sales"].sum()
```

Multiple metrics can also be calculated:

```python
df.groupby("Category")["Sales"].agg(["sum", "mean", "count"])
```

This makes it possible to move from individual transaction-level records to useful business summaries.

---

## 🛍️ Retail & Sales Analysis

pandas techniques were applied to explore business-style datasets and answer questions such as:

✅ Which products generate the highest sales?  
✅ Which categories perform best?  
✅ What is the average sales value?  
✅ Which transactions meet specific conditions?  
✅ How many records exist within each category?  
✅ Where are missing values present?  
✅ How can products or categories be ranked by performance?  

This demonstrated how Python can be used to transform raw sales data into useful analytical information.

---

## 📈 Data Visualisation

Charts were used to make patterns and comparisons easier to interpret.

### Bar Chart

```python
category_sales.plot(kind="bar")
```

### Line Chart

```python
df.plot(x="Month", y="Sales", kind="line")
```

### Matplotlib

```python
import matplotlib.pyplot as plt

category_sales.plot(kind="bar")

plt.title("Sales by Category")
plt.xlabel("Category")
plt.ylabel("Sales")
plt.show()
```

Visualisation helped communicate findings such as category performance, sales trends and differences between groups.

---

## 🛠️ Key pandas Methods

| Method | Purpose |
|---|---|
| `head()` | Preview the first rows |
| `info()` | Inspect columns and data types |
| `describe()` | Generate summary statistics |
| `.loc[]` | Select data using labels |
| `.iloc[]` | Select data using positions |
| `sort_values()` | Sort records |
| `groupby()` | Group and summarise data |
| `dropna()` | Remove missing values |
| `fillna()` | Replace missing values |
| `isna()` | Identify missing values |
| `value_counts()` | Count unique values |
| `mean()` | Calculate averages |
| `sum()` | Calculate totals |

---

## 💡 What I Practised

Through these projects, I developed practical experience in:

✅ Importing datasets into pandas  
✅ Working with DataFrames  
✅ Exploring dataset structure and statistics  
✅ Filtering records using conditions  
✅ Slicing data with `.loc[]` and `.iloc[]`  
✅ Sorting data with `sort_values()`  
✅ Grouping and aggregating with `groupby()`  
✅ Identifying and handling missing values  
✅ Analysing retail and sales data  
✅ Creating charts with pandas and Matplotlib  
✅ Using Python to answer data-driven business questions  

---

## 🎯 Key Skills

`Python` • `pandas` • `DataFrames` • `.loc[]` • `.iloc[]` • `Filtering` • `groupby()` • `sort_values()` • `dropna()` • `fillna()` • `Data Cleaning` • `Data Manipulation` • `Data Analysis` • `Matplotlib` • `Data Visualisation` • `Google Colab`

---

## 📚 Project Context

These projects were completed as part of my **Data Technician Bootcamp** and form part of my developing data analytics portfolio.

The work builds on my Python fundamentals and applies Python to practical **data cleaning, manipulation, analysis and visualisation tasks** relevant to Data Technician and entry-level Data Analyst roles.
