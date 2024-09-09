# Hotel_Industry_Analysis

### Dashboard Link : https://app.powerbi.com/groups/me/reports/384d017e-e935-44dc-9e7d-1626c1a36de1/ReportSect

#### Dashboard Visual:

![Screenshot 2024-06-13 145024](https://github.com/user-attachments/assets/02dbe053-9afe-4f76-a513-e134f6adefb2)

## Problem Statement


The dashboard provides valuable insights into hotel operations, helping to understand and improve customer satisfaction. By analyzing factors such as booking platforms, customer reviews, room rates, and room utilization, the hotel can optimize services and increase revenue. The analysis shows that 57% of customers are neutral or dissatisfied, indicating the need for improvements in service quality. Additionally, the average delay in check-in and check-out is 15 minutes, which signals an operational bottleneck.

## Key Highlights:

#### KPIs Included:

📌 Booking Percentage by Platform: Analyzes which platforms (e.g., MakeMyTrip, LogTrip) contribute most to bookings, allowing for targeted marketing and optimization.

📌 Average Daily Rate (ADR): Measures the average revenue earned per room per day, helping hotels understand their pricing effectiveness.

📌 Revenue Per Available Room (RevPAR): Tracks overall revenue performance by measuring how much revenue is generated from each available room, regardless of occupancy.

📌 Daily Booked Room Nights (DBRN): Shows how many rooms are being booked each day on average.

📌 Daily Utilized Room Nights (DURN): Tracks how many rooms are being actively utilized by guests each day.

#### Project Overview:
📍 Objective:
To analyze daily room occupancy, customer satisfaction, and revenue metrics in the hotel industry.

📍 Data Sources:
 SQL databases, Excel files, CSV files, and cloud services.

📍 Tech Stack: Power BI.

#### Outcomes:
This project provided a deeper understanding of how analytics can be used to improve hotel operations. The insights gained can lead to enhanced decision-making, better customer service, and increased profitability.

#### Data Model used:
![Data Model for Hotel Analysis](https://github.com/user-attachments/assets/c947a65b-2b96-498d-8066-5b2fc7c242d8)

### Steps Followed:
#### 1.) Data Loading:
Imported the dataset from a CSV file into Power BI.

#### 2.) Data Cleaning:
Ensured the data was complete and accurate using Power Query's column profiling tools.

#### 3.) Handling Missing Values: 
Addressed missing data in important fields like customer reviews and delays.

#### 4.) Data Visualization:
Created visual representations of key metrics, including customer ratings, room utilization, and booking platforms.

#### 5.) Filters and Slicers:
Slicers were added for easy segmentation based on factors like room class, customer type, and travel type.

#### 6.) Delay Calculation: 
Used card visuals to display average delays in check-in and check-out times.

#### 7.) Customer Satisfaction by Gender: 
Segmented satisfaction data by gender to analyze trends.

#### 8.) Rating Visualization:
 Showed average customer ratings for various service aspects, including cleanliness, food, and room service.

#### 9.) Custom Columns and Measures: 
Created calculated columns for customer age groups and dynamic measures for KPIs like total bookings and room revenue.

#### 10.) Publishing: 
Published the completed report to Power BI Service for stakeholders.

### Insights
#### 1) Total Customers Analyzed: 129,880
📍Satisfied Customers (Male): 21.68%

📍Satisfied Customers (Female): 21.76%

📍Neutral/Unsatisfied Customers (Male): 27.58%

📍Neutral/Unsatisfied Customers (Female): 28.97%

This reveals that a majority of customers are either neutral or dissatisfied, indicating a need for improvement in service quality.

#### 2) Average Service Ratings (Out of 5):

📍Room Service: 3.64

📍Cleanliness: 3.29

📍Food and Drink: 3.21

📍Online Booking Convenience: 2.88

📍Wifi Service: 2.81

📍Baggage Handling: 3.63

📍Check-in Process: 3.31

📍Overall Comfort: 3.44

#### 3) Delays in Service:

📍Average Check-in Delay: 15.09 minutes

📍Average Check-out Delay: 14.71 minutes

The delays in check-in and check-out are notable pain points, with over 15 minutes of average delay, suggesting the need for improved efficiency in these areas.

#### 4) Room Class Preferences:
📍Business Class: 47.87% of customers

📍Economy Class: 44.89%

📍Economy Plus: 7.25%

#### 5) Customer Age Distribution:
📍0-25 years: 21.69%

📍25-50 years: 52.44%

📍50-75 years: 25.57%

📍75-100 years: 0.31%

#### 6) Customer Type:
📍First-time customers: 18.31%

📍Returning customers: 81.69%

📍The high percentage of returning customers suggests customer loyalty, but improvements are needed to maintain satisfaction levels.

#### 7) Type of Travel:
📍Business Travelers: 69.06%

📍Leisure Travelers: 30.94%

#### Summary 
This breakdown highlights that the majority of hotel guests are business travelers, offering opportunities to tailor services and pricing strategies accordingly.

This dashboard helps the Hotel industry understand their customers better. It helps the Hotel industry know if their customers are satisfied with their services. Through different ratings, they get to know their improvement area, & thus they can improve their services by identifying these area. It also lets them know the customer reviews, Hotel ratings, food thus since by using this dashboard they have identified this problem, they can further work on factors responsible for these unwanted delays.

Since, number of neutral/dissatisfied customers (almost 57 %) are more than satisfied customers (around 43 %), thus in all they must work on improving their services. 

Also since average delay in arrival & departure both is 15 minutes, thus they must try to reduce it.
Key Highlights:

for creating new column following DAX expression was written;
       
        Age Group = 
        
        if(Customer_satisfaction[Age]<=25, "0-25 (25 included)",
        
        if(Customer_satisfaction[Age]<=50, "25-50 (50 included)",
        
        if(Customer_satisfaction[Age]<=75, "50-75 (75 included)",
        
        "75-100 (100 included)")))
        
Snap of new calculated column ,

![Snap_1](https://user-images.githubusercontent.com/102996550/174089602-ab834a6b-62ce-4b62-8922-a1d241ec240e.jpg)

        
New measure was created to find total occupancy of customers.

Following DAX expression was written for the same,
        
        Count of Customers = COUNT(customer_id[ID])
        
#### Trends per week 
📌 Daily Utilized Room Nights (DURN): Tracks how many rooms are being actively utilized by guests each day.

![Occupancy Trend by week and Day](https://github.com/user-attachments/assets/0a4fbe6f-9cb5-46f4-8e1a-06d293e7cdbb)


 #### Rooms booked per night
 📌 Revenue Per Available Room (RevPAR): Tracks overall revenue performance by measuring how much revenue is generated from each available room, regardless of occupancy.
 
 A visual used to represent this: 
 Revenue per room by week number and day type:

![Revenue Trend by Day and Week](https://github.com/user-attachments/assets/e0f9a8eb-24a4-4718-b5bd-97c6f37b3930)
 
 #### Revenue trend per week
 
![Revenue Trend Per Week](https://github.com/user-attachments/assets/42991634-d2b7-42c4-8075-b3e3b77d25b8)

 
