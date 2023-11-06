# Sales Analysis of Electronics on Amazon

## Introduction
In the realm of online sales and e-commerce, maximizing throughput to align with customer needs is pivotal for boosting sales opportunities.
![image](https://github.com/itzdeepp/product_sales_analysis_python/assets/145162410/f74a6b4d-f992-4217-8d66-3d727e763f41)


### What is Sales Analysis?

Sales analysis involves examining the profit contribution of different products sold by your business, providing insights into market performance.


### How Often Should Sales Analysis Be Done?

Performing regular product sales analysis is crucial for gaining a competitive edge, and this documentation will guide you through the essentials.


## Purpose of Analysis

A product analysis report is essential for:

1. **Internal Analysis**: Improving and marketing your product.
2. **External Analysis**: Understanding and convincing potential customers.
3. **Cost Analysis**: Analyzing the costs involved from manufacturing to sale.


## Things To Consider Before Doing a Sales Analysis

### i. Understanding the Business Model
![image](https://github.com/itzdeepp/product_sales_analysis_python/assets/145162410/537bfe9d-6681-414b-b917-43b2d02704e4)


Your company's plan for profitability through the sale of products or services.

### ii. Problem Analysis

Understanding real-world problems and proposing solutions to meet user needs.

Suggestions for creating problem trees include:

- Involving stakeholders for diverse insights.
- Simplifying complex issues into a robust problem tree diagram.


### iii. Consumption by the Consumer

Know how the consumer will use your model to tailor features accordingly.

### iv. The Economic Impact

Illustrate the economic benefits or the consequences of discontinuing a product.


### v. Data-Driven Decisions

Use data to inform the decision-making process and validate actions before committing.

### vi. Targeting Success Quantification

Measure success with both objective and subjective criteria post-completion.



## Overview
![image](https://github.com/itzdeepp/product_sales_analysis_python/assets/145162410/0d74b0a0-ffd7-4c76-9a63-e4ae063f2920)

![image](https://github.com/itzdeepp/product_sales_analysis_python/assets/145162410/67548351-9742-449c-be61-ea6254ddf13c)

![image](https://github.com/itzdeepp/product_sales_analysis_python/assets/145162410/419009b3-3dcc-44ab-8842-a1a4f3013ae4)

![image](https://github.com/itzdeepp/product_sales_analysis_python/assets/145162410/83f10ac3-bb3a-4d8d-95fb-b2017daa6aa0)

![image](https://github.com/itzdeepp/product_sales_analysis_python/assets/145162410/92ed0b72-5829-449f-b0ba-42743a403c64)

![image](https://github.com/itzdeepp/product_sales_analysis_python/assets/145162410/d4e0d1c9-2d76-47e9-b378-a58be59fcfd6)

![image](https://github.com/itzdeepp/product_sales_analysis_python/assets/145162410/33f7ed68-a67f-46f2-b544-eafd5c736ab4)

![image](https://github.com/itzdeepp/product_sales_analysis_python/assets/145162410/3b391d72-7455-4687-ae46-89fa4ca3a468)






The dataset provides sales data for electronics on Amazon, including user ratings, categories, and sale time. [Link to Data Set](here)

## Step 1: Exploratory Data Analysis (EDA)

EDA helps to understand data through patterns, anomalies, hypothesis testing, and assumptions via summary statistics and graphical representations.


### Initial Setup

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

# Load the dataset
dataset = pd.read_csv('path_to_dataset.csv')

# First five rows
print(dataset.head())

# Last five rows
print(dataset.tail())

# Dataset shape
print(dataset.shape)

# Dataset information
print(dataset.info())

# Convert Timestamp to datetime
dataset['Timestamp'] = pd.to_datetime(dataset['Timestamp'], unit='s')

# Convert IDs and categories to strings
dataset['User ID'] = dataset['User ID'].astype(str)
dataset['Product ID'] = dataset['Product ID'].astype(str)
dataset['Category'] = dataset['Category'].astype(str)

# Summary statistics
print(dataset.describe())


# Dealing With Missing Values
Understanding the reasons for missing data is key to determining the approach for handling them.

# Finding Answers with Visualizations
Using matplotlib and seaborn for graphical representations.

# Questions and Insights
Best Year of Sales: 2015 had the highest sales.
Best Month for Sales: January saw the highest sales.
Top Selling Brands: Mpow and Bose led in 2015.
Most Sold Products: Bose consistently led over the past three years.
Top Categories: Headphones, followed by Computers & Accessories.
Least Sold Categories: Security & Surveillance.
Least Sold Brands: Koolertron and DURAGADGET.
Ratings Distribution: Most products were rated 5.
![image](https://github.com/itzdeepp/product_sales_analysis_python/assets/145162410/dd825e9d-ad56-4a2b-882d-577028107d9c)

Best Rated Brands: Plemo and Savage.
![image](https://github.com/itzdeepp/product_sales_analysis_python/assets/145162410/e0e91fc5-5b61-41d3-9d88-248d16de9b22)


#Conclusion
2015 was the peak year for sales.
The 'Headphones' category dominated sales.
A sharp decline in sales was observed from 2016 to 2018.
Bose and Logitech were the top-selling brands.
Koolertron and DURAGADGET had the least sales.
Plemo was the best-rated brand.
