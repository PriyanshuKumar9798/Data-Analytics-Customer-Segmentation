# Data Analytics Customer Segmentation

## Goal of the project
The purpose of this project is to conduct a Customer Segmentation Analysis for an Automobile bike Company. Customer segmentation is performed by developing a RFM Model. RFM (Recency, Frequency, Monetary) analysis is a behavior-based approach grouping customers into segments. It groups the customers on the basis of their previous purchase transactions. In this analysis the customer segment was divided into 11 groups. The analysis will help in determining which customers segments should be targeted in order to enhance sales revenue for the company. 

## Analysis Approach
### 1. Data Quality Assessment and Data Cleaning
The first step towards generating useful insights from the data was the data preparation, quality assessment and data cleaning step. After the cleaning process exploratory data analysis on the dataset and identification customer purchasing behaviours to generate insights can be performed.

In the data cleaning step the data quality of the following datasets were first assessed. After a data quality assessment the following data quality issues were observed and the necessary process to mitigate the issues was followed:

- **CustomerDemographics.xlsx**  
  - 1 irrelevant column was present and dropped.  
  - 5 columns had missing values. Based on volume, either records were dropped or values imputed.  
  - Gender column lacked standardisation. Values were standardised.  
  - Date of Birth column was transformed into new features: Age and Age Group. Outliers were removed.  
  - No duplicate records were found.  

- **NewCustomerList.xlsx**  
  - 5 irrelevant columns were dropped.  
  - 4 columns had missing values. Records were either dropped or imputed.  
  - Date of Birth column transformed into Age and Age Group.  
  - No inconsistencies or duplicates found.  

- **Transaction_data.xlsx**  
  - Product_first_sold_date column converted from int64 to datetime format.  
  - 7 columns had missing values. Records were dropped or imputed.  
  - New feature "Profit" created (difference between list price and standard price).  
  - No inconsistencies or duplicates found.  

- **CustomerAddress.xlsx**  
  - States column standardised for consistency.  
  - Some Customer IDs from demographics table did not match with address table.  

### 2. Exploratory Data Analysis on Customer Segments
Insights from the analysis include:  

- **New vs Old Customers Age Distribution**  
  - Most new and old customers are aged between 40–49.  
  - Lowest customer counts under 20 and above 80.  
  - New customers are concentrated in the 20–29 and 40–49 age groups.  
  - Sharp drop observed in 30–39 age group among new customers.  

- **Bike purchases over last 3 years by Gender**  
  - Females made ~51% of purchases, Males ~49%.  
  - Female purchases exceeded male purchases by about 10,000 units.  

- **New vs Old Customers Job Industry Distribution**  
  - Manufacturing and Financial Services sectors dominate (~20% each).  
  - Agriculture and Telecom sectors lowest (~3%).  
  - Similar trends in both new and old customers.  

- **Wealth Segmentation by Age Category**  
  - Across all ages, most customers are "Mass Customer" segment.  
  - Next largest group: "High Net Worth".  
  - For ages 40–49, "Affluent" segment surpasses "High Net Worth".  

- **Cars owned by States**  
  - New South Wales: largest number without a car.  
  - Victoria: proportions even.  
  - Queensland: more car owners than non-owners.  

### 3. RFM Analysis and Customer Segmentation
Customer segmentation was done with an RFM Model. Customers were divided into 11 groups:  
- Platinum Customers  
- Very Loyal Customers  
- Recent Customers  
- Potential Customers  
- Lost Customers  
- Losing Customers  
- Late Bloomer  
- High Risk Customers  
- Evasive Customers  
- Becoming Loyal  
- Almost Lost Customers  

### 4. RFM Analysis: Scatter Plots
- **Recency vs Monetary**  
  Recent customers generate more revenue compared to those inactive for a longer period.  

- **Frequency vs Monetary**  
  Platinum, Very Loyal, and Becoming Loyal customers purchase more frequently and generate higher revenue.  

## Datasets Used
The datasets used include:  

- **Raw_data.xlsx** (containing multiple sheets):  
  - **Transactions_data.xlsx** – customer transaction history across Australian states.  
  - **NewCustomerList.xlsx** – details of newly acquired customers.  
  - **CustomerDemographic.xlsx** – demographic information of customers.  
  - **CustomerAddress.xlsx** – customer address details.  

## Tools and Technologies used
- **Python** – for Data Quality Assessment and Cleaning.  
- Libraries: **pandas, matplotlib, seaborn** – for EDA and visualisation.  
