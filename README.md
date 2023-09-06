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
The dataset consists of 29 columns and 119390 rows for the period 2017 - 2019.  

**Data Assessment**
Data assessment is carried out to ensure that the data used for further analysis is ready and in accordance with the needs of the analysis. Things to do:

  - Checking for null or missing values ​​in data
  - Check for duplication of data
  - Perform data type and value consistency
  - Check for outliers or unusual data


Table 1 - Assessment Data Results

| Data Assessment | Finding | Handling |
| -------- | -------- | -------- |
| Missing values | There are null values ​​for company, city, children, and agent | - company: filled with 0, indicating the guest is not from the company - agent: filled with 0, indicating the guest made a reservation independently or not through an agent - children: filled with 0, indicating the guest does not bring children - city: filled with 'Undefined', because the city is not known with certainty |
| Inappropriate or inconsistent values | Meaning of 'Undefined' in the meal column | Values ​​of the meal column can be categorized into 2, namely 'With Meal' (Breakfast, Full Board, Dinner) and 'No Meal' (No Meal, Undefined) |
| Anomaly data or unnecessary data |  - There are negative values ​​and outliers that are very far from the data distribution in the adr column - There are 180 data bookings that do not have guests. | Delete or drop these data rows |



# 📂 STAGE 2: Data Analysis 

**1. Monthly Hotel Booking Analysis Based on Hotel Type**

This analysis will be carried out to find out the trend of bookings for each type of hotel. This analysis can help companies better understand their market and customer needs, and enable them to improve operational efficiency and optimize revenue.



 <p align="center">
  <img src="![image](https://github.com/prathmeshjani/Investigate-Hotel-Business-using-DataVisualization/assets/69078331/a1fe3177-8717-43cf-8b8c-463547b4d75f)" alt="Your Image Description" width="200" height="200" />
</p>

<p align = 'center'>
Figure 1 — City Hotel and Resort Hotel Ratio Percentage Graph
</p>

From the above plot, it can be seen that City Hotels are more in demand by customers, with a percentage of bookings reaching 66.41%. These hotels are usually located in downtown or urban areas, close to attractions and businesses, so customers booking these hotels may have their main activity around where they are staying. On the other hand, Resort Hotels are only booked by 33.59% of customers. These hotels are usually located in beautiful places such as the seaside, mountains, or quiet rural areas and there are complete facilities. Customers who book this hotel allegedly have the goal of vacationing and relaxing in that place.

<p align="center">
  <img src="![download](https://github.com/prathmeshjani/Investigate-Hotel-Business-using-DataVisualization/assets/69078331/47948486-e45c-468b-97a2-822e0f2cf304)" alt="Your Image Description" width="200" height="200" />
</p>
<p align = 'center'>
Figure 2 — Graph of City Hotel and Resort Hotel Booking Numbers by Month
</p>

Hotel bookings tend to increase during the holiday season, especially in the period May - August. The two types of hotels, namely City Hotels and Resort Hotels, had the highest booking value in that period, with a significant increase in City Hotels. This is likely due to the large number of national holidays in 2017-2019, such as collective leave and religious events (Ramadan) which allow people to take vacations. In addition, with the majority of Indonesia's population being Muslim and the existence of a culture of going home and gathering during Eid al-Fitr, it is possible for people to travel far and need a place to stay in the middle of the trip, so they can make hotel reservations.

Meanwhile, during the holiday season, from October to December, hotel bookings also increased but tended to be lower than May - August. It is likely that many people prefer to celebrate holidays such as Christmas and New Year at home.

In the period January - March, the lowest hotel booking rate. This is likely due to the small number of national holidays, and this period is the start of a new school year for students and not a period of busy business travel activities because it is still the beginning of the year.


**2. Impact Analysis of Stay Duration on Hotel Bookings Cancellation Rates**

This analysis focuses on the relationship between the duration of stay and the cancellation rate of hotel bookings. Based on data, about 19% of hotel orders made online are canceled before the customer arrives [source]. These cancellations can lead to reduced room availability and an impact on hotel revenue because each vacant room can become a financial burden on that day. In addition, if the hotel uses an Online Travel Agency (OTA), this cancellation rate can affect the hotel's ranking in search [source].


Figure 3 — Hotel City Cancellation Percentage Graph


Figure 4 — Hotel Resort Cancellation Percentage Graph


City hotels also have a higher cancellation rate than resort hotels. This shows that many customers who book City Hotels tend to cancel their orders more often. City Hotels have a more centralized location in the city or urban area and are close to tourist and business spots, predictably many activities have to be arranged and perhaps due to other factors, many customers cancel their orders.

Figure 5 — Trends in Hotel Booking Cancellations Based on Duration of Stay


Based on the duration of stay, it can be seen that the cancellation rate for hotel orders will tend to be higher along with the longer the duration of the stay, both at City Hotels and Resort Hotels. At City Hotel the cancellation rate increased more significantly with a percentage value below 50% for a duration of one week. For a duration of stay of more than four weeks, this Resort Hotel also has a lower cancellation rate. In essence, both types of hotels have a positive trend, where the longer the duration of stay, the higher the possibility of the order being canceled.

Why the longer the duration of the stay causes the cancellation rate to increase, the company can carry out further evaluation and analysis. Several factors that may include customer dissatisfaction. Customers who stay in hotels for a long period of time may have higher expectations and demand better service. If customers are not satisfied with hotel services, they may decide to cancel their reservation and find a better hotel. In addition, higher costs can also be a factor. Costs may be greater than the customer expected or budgeted for, so they seek a more affordable alternative.



**3. Impact Analysis of Lead Time on Hotel Bookings Cancellation Rates**

Analysis was conducted to determine the correlation between order cancellation and lead time. Lead time is the waiting period or the time between hotel bookings and arrival times.


Figure 6 — Trend of Hotel Booking Cancellation Based on Lead Time


The lowest order cancellation for both types of hotels occurred at a lead time of less than one month. The highest cancellation rate of up to 60% occurs at City Hotels with a lead time of 10 months to 1 year. Meanwhile, the Resort Hotel trend has a fairly stagnant cancellation rate with an average value of 40%.

City Hotels which are located in the city center and are frequently used for events or business that are scheduled in advance, are prone to cancellation due to changes in customer schedules or plans. In addition, City Hotels may offer lower room rates than Resort Hotels, making it easier for customers to cancel their orders because they have found better deals elsewhere.

Resort hotels may be used more for vacations or recreation, so customers tend to stick more to their schedules and make fewer changes. Additionally, Resort Hotels that may target customers seeking a more exclusive experience, may be better able to maintain their order levels despite better offers elsewhere.


# STAGE 3: Summary and Recommendations

1. Overall City Hotel is the most booked by customers. In both types of hotels, a significant increase in customers occurred during the holiday seasons, namely May-July and October-December.
   Business recommendation:
     - Companies can optimize the facilities and services at Resort Hotels, because Resort Hotels have a lower booking rate than City Hotels so that customers are more interested in booking rooms there. For example by adding facilities        such as a spa, gym or swimming pool, as well as providing more personal and friendly service to customers.
     - The company can also maximize the City Hotel strategy, because it is in great demand by customers so it is more profitable. Companies can provide additional services for businesses, such as hall rooms or packages for meetings           such as seminars and so on.
     - Increasing promotions during the holiday season, for example by providing special discounts for guests who book a certain number of rooms or providing attractive holiday packages. Companies can also consider applying non-               refundable to avoid canceling orders.
     - For times of the off season, companies may combine flexible and non-refundable rates. Or can provide a special discount but non-refundable.


  2. The cancellation rate will be higher along with the length of stay booked at both types of hotels. Cancellation rates at City Hotels increased significantly with the lowest percentage less than one week in duration. Resort hotels also tend to experience an increase in cancellation rates but are more stagnant and for stays of less than 2 weeks and more than 1 month tend to have lower cancellation rates.
     Business recommendation:
     - The company can ensure that it has a solid order cancellation policy in place. This is to protect the company from the impacts, such as revenue loss. Companies can provide or explain terms and conditions before they place an order both in online and offline orders. This can include information about refunds, cancellation fees, etc. Tighter cancellation policies can have a big impact. In addition, it can also reduce fraudulent bookings.
     - Do a pricing strategy and limit the number of nights. Limiting the number of nights on a flexible rate over a one week span. In addition, it only provides non-refundable rates for longer stays. This is done to increase revenue and reduce the risk of unwanted cancellations.
     - For other cancellation prevention companies can improve services or provide good pre-stay services to increase customer satisfaction so that it will reduce their tendency to cancel their orders.
    
  3. The lowest order cancellation for both types of hotels occurred at a lead time of less than one month. City Hotel has the highest cancellation rate at 1 year lead time.

     - Both types of hotels can consider reducing lead times. By limiting available booking timeframes, hotels can ensure that customers only book when they are sure they will be staying at the hotel, thereby reducing the possibility of cancellation.
     - City Hotels may also consider increasing their room rates to improve their profit margins and lower cancellation rates. By increasing room rates, customers may be more likely to reconsider before canceling their order.
     - Sending reminders via email about their booking. This is done in order to stay connected and show the level of service the company provides. The company can inform you that the deadline is coming soon with its cancellation policy.
     - Instead of canceling orders, companies can offer to reschedule and sell rooms that still have long lead times.
    


**Source :**

Delgado, Pablo. "Cancellations on Booking.com: 104% More than on the Hotel Website. Expedia, 31% More." Mirai, https://www.mirai.com/blog/cancellations-on-booking-com-104-more-than-on-the-hotel-website-expedia-31-more/.

Delgado, Pablo. "Cancellations shooting up: implications, costs and how to reduce them". Mirai, https://www.mirai.com/blog/cancellations-shooting-up-implications-costs-and-how-to-reduce-them/

LOEB, Tony. "Where do Cancellations come from?". Experience Hotel Blog, https://blog.experience-hotel.com/where-do-cancellations-come-from/.

Travelline. "5 ways to decrease cancellation rate and retain customer loyalty". Travellin, https://www.travelline.pro/blog/5-ways-to-decrease-cancellation-rate-and-retain-customer-loyalty/

Verot, Benjamin. "Everything you Need to Know About Hotel Cancellations". HotelMinder. https://www.hotelminder.com/everything-you-need-to-know-about-hotel-cancellations.

Verot, Benjamin. "8 Tips to Reduce Last Minute Hotel Cancellations and No Shows". HotelMinder. https://www.hotelminder.com/8-tips-to-reduce-last-minute-hotel-cancellations-and-no-shows


