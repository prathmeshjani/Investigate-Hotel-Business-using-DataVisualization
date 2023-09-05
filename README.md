# 🏬 Investigate Hotel Business using DataVisualization

**Tool** : Jupyter Notebook  
**Programming Language** : Python  
**Libraries** : Pandas, NumPy  
**Visualization** : Matplotlib, Seaborn  
**Dataset** : Hotel_bookings_data.csv  


**Table of Contents**

 - STAGE 0: Problem Statement
      - Introduction
      - Business Questions
      - Objective
  - STAGE 1: Data Preprocessing
      - Data Overview
      - Data Assessment
  - STAGE 2: Data Analysis
      - Monthly Hotel Booking Analysis Based on Hotel Type
      - Impact Analysis of Stay Duration on Hotel Bookings Cancellation Rates
      - Impact Analysis of Lead Time on Hotel Bookings Cancellation Rates
  - STAGE 3: Summary and Recommendations


# 📂 STAGE 0: Problem Statement

**Introduction**

Business performance analysis is an important key for companies to achieve success in their business. Companies can carry out an analysis to identify their problems, weaknesses, and strengths. In the hospitality business, it is important to understand customer behavior. By understanding customer behavior, companies can find out what factors influence customers in making hotel reservations. In addition, companies can also identify which products or services are not selling well in the market. This is done to adjust the appropriate business strategy so that the company can improve customer experience and achieve long-term business goals.

**Business Questions**

  - What types of hotels are most frequently visited by customers?
  - Does the length of stay affect the cancellation rate of hotel bookings?
  - Does the time gap between a hotel reservation and the day a guest arrives affect the cancellation rate of 
    hotel bookings?


**objective**
Create data-based visualizations as insights for the hotel business

# STAGE 1: Data Preprocessing

**Data Overview**
The dataset consists of 29 columns and 119390 rows with the period 2017 - 2019.  

**Data Assessment**
Data assessment is carried out to ensure that the data used for further analysis is ready and in accordance with the needs of the analysis. Things to do:

  - Checking for null or missing values ​​in data
  - Check for duplication of data
  - Perform data type and value consistency
  - Check for outliers or unusual data


Table 1 - Assessment Data Results

| Data Assessment | Finding | Handling |
| -------- | -------- | -------- |
| Missing values | There are null values ​​for company, city, children, and agent | - company : filled with 0, indicating the guest is not from the company - agent : filled with 0, indicating the guest made a reservation independently or not through an agent - children : filled with 0, indicating the guest does not bring children - city : filled with 'Undefined', because the city is not known with certainty |
| Inappropriate or inconsistent values | Meaning of 'Undefined' in the meal column | Values ​​of the meal column can be categorized into 2, namely 'With Meal' (Breakfast, Full Board, Dinner) and 'No Meal' (No Meal, Undefined) |
| Anomaly data or unnecessary data |  - There are negative values ​​and outliers that are very far from the data distribution in the adr column - There are 180 data bookings that do not have guests. | Delete or drop these data rows |


