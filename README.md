# Hotel_Industry_Analysis

### Dashboard Link : https://app.powerbi.com/groups/me/reports/384d017e-e935-44dc-9e7d-1626c1a36de1/ReportSection

## Problem Statement


The dashboard provides valuable insights into hotel operations, helping to understand and improve customer satisfaction. By analyzing factors such as booking platforms, customer reviews, room rates, and room utilization, the hotel can optimize services and increase revenue. The analysis shows that 57% of customers are neutral or dissatisfied, indicating the need for improvements in service quality. Additionally, the average delay in check-in and check-out is 15 minutes, which signals an operational bottleneck.

## Key Highlights:

#### KPIs Included:

📌 Booking Percentage by Platform: Analyzes which platforms (e.g., MakeMyTrip, LogTrip) contribute most to bookings, allowing for targeted marketing and optimization.

📌 Average Daily Rate (ADR): Measures the average revenue earned per room per day, helping hotels understand their pricing effectiveness.

📌 Revenue Per Available Room (RevPAR): Tracks overall revenue performance by measuring how much revenue is generated from each available room, regardless of occupancy.

📌 Daily Booked Room Nights (DBRN): Shows how many rooms are being booked each day on average.

📌 Daily Utilized Room Nights (DURN): Tracks how many rooms are being actively utilized by guests each day.

Project Overview:
📍 Objective: To analyze daily room occupancy, customer satisfaction, and revenue metrics in the hotel industry.
📍 Data Sources: SQL databases, Excel files, CSV files, and cloud services.
📍 Tech Stack: Power BI.

Outcomes:
This project provided a deeper understanding of how analytics can be used to improve hotel operations. The insights gained can lead to enhanced decision-making, better customer service, and increased profitability.

Steps Followed:
#### Data Loading:
Imported the dataset from a CSV file into Power BI.

#### Data Cleaning:
Ensured the data was complete and accurate using Power Query's column profiling tools.

#### Handling Missing Values: 
Addressed missing data in important fields like customer reviews and delays.

#### Data Visualization:
Created visual representations of key metrics, including customer ratings, room utilization, and booking platforms.

#### Filters and Slicers:
Added slicers for easy segmentation by factors like room class, customer type, and travel type.

#### Delay Calculation: 
Used card visuals to display average delays in check-in and check-out times.

#### Customer Satisfaction by Gender: 
Segmented satisfaction data by gender to analyze trends.

#### Rating Visualization:
 Showed average customer ratings for various service aspects, including cleanliness, food, and room service.

#### Custom Columns and Measures: 
Created calculated columns for customer age groups and dynamic measures for KPIs like total bookings and room revenue.

#### Publishing: 
Published the completed report to Power BI Service for stakeholders.
Insights
#### 1) Total Customers Analyzed: 129,880
Satisfied Customers (Male): 21.68%

Satisfied Customers (Female): 21.76%

Neutral/Unsatisfied Customers (Male): 27.58%

Neutral/Unsatisfied Customers (Female): 28.97%

This reveals that a majority of customers are either neutral or dissatisfied, indicating a need for improvement in service quality.

#### 2) Average Service Ratings (Out of 5):

Room Service: 3.64

Cleanliness: 3.29

Food and Drink: 3.21

Online Booking Convenience: 2.88

Wifi Service: 2.81

Baggage Handling: 3.63

Check-in Process: 3.31

Overall Comfort: 3.44

#### 3) Delays in Service:

Average Check-in Delay: 15.09 minutes

Average Check-out Delay: 14.71 minutes

The delays in check-in and check-out are notable pain points, with over 15 minutes of average delay, suggesting the need for improved efficiency in these areas.

#### 4) Room Class Preferences:
Business Class: 47.87% of customers

Economy Class: 44.89%

Economy Plus: 7.25%

#### 5) Customer Age Distribution:
0-25 years: 21.69%

25-50 years: 52.44%

50-75 years: 25.57%

75-100 years: 0.31%

#### 6) Customer Type:
First-time customers: 18.31%

Returning customers: 81.69%

The high percentage of returning customers suggests customer loyalty, but improvements are needed to maintain satisfaction levels.

#### 7) Type of Travel:
Business Travelers: 69.06%

Leisure Travelers: 30.94%

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

        
- Step 15 : New measure was created to find total count of customers.

Following DAX expression was written for the same,
        
        Count of Customers = COUNT(airline_passenger_satisfaction[ID])
        
A card visual was used to represent count of customers.

![Snap_Count](https://user-images.githubusercontent.com/102996550/174090154-424dc1a4-3ff7-41f8-9617-17a2fb205825.jpg)

        
 - Step 16 : New measure was created to find  % of customers,
 
 Following DAX expression was written to find % of customers,
 
         % Customers = (DIVIDE(airline_passenger_satisfaction[Count of Customers], 129880)*100)
 
 A card visual was used to represent this perecntage.
 
 Snap of % of customers who preferred business class
 
 ![Snap_Percentage](https://user-images.githubusercontent.com/102996550/174090653-da02feb4-4775-4a95-affb-a211ca985d07.jpg)

 
 - Step 17 : New measure was created to calculate total distance travelled by flights & a card visual was used to represent total distance.
 
 Following DAX expression was written to find total distance,
 
         Total Distance Travelled = SUM(airline_passenger_satisfaction[Flight Distance])
    
 A card visual was used to represent this total distance.
 
 
 ![Snap_3](https://user-images.githubusercontent.com/102996550/174091618-bf770d6c-34c6-44d4-9f5e-49583a6d5f68.jpg)
 
 - Step 18 : The report was then published to Power BI Service.
 
 
![Publish_Message](https://user-images.githubusercontent.com/102996550/174094520-3a845196-97e6-4d44-8760-34a64abc3e77.jpg)

# Snapshot of Dashboard (Power BI Service)

![dashboard_snapo](https://user-images.githubusercontent.com/102996550/174096257-11f1aae5-203d-44fc-bfca-25d37faf3237.jpg)

 
 # Report Snapshot (Power BI DESKTOP)

 
![Dashboard_upload](https://user-images.githubusercontent.com/102996550/174074051-4f08287a-0568-4fdf-8ac9-6762e0d8fa94.jpg)

# Insights

A single page report was created on Power BI Desktop & it was then published to Power BI Service.

Following inferences can be drawn from the dashboard;

### [1] Total Number of Customers = 129880

   Number of satisfied Customers (Male) = 28159 (21.68 %)

   Number of satisfied Customers (Female) = 28269 (21.76 %)

   Number of neutral/unsatisfied customers (Male) = 35822 (27.58 %)

   Number of neutral/unsatisfied customers (Female) = 37630 (28.97 %)


           thus, higher number of customers are neutral/unsatisfied.
           
### [2] Average Ratings

    a) Baggage Handling - 3.63/5
    b) Check-in Service - 3.31/5
    c) Cleanliness - 3.29/5
    d) Ease of online booking - 2.88/5
    e) Food & Drink - 3.21/5
    f) In-flight Entertainment - 3.36/5
    g) In-flight service - 3.64/5
    h) In-flight Wifi service - 2.81/5
    i) Leg room service - 3.37/5
    j) On-board service - 3.38/5
    k) Online boarding - 3.33/5
    l) Seat comfort - 3.44/5
    m) Departure & arrival convenience - 3.22/5
  
  while calculating average rating, null values have been ignored as they were not relevant for some customers. 
  
  These ratings will change if different visual filters will be applied.  
  
  ### [3] Average Delay 
  
      a) Average delay in arrival(minutes) - 15.09
      b) Average delay in departure(minutes) - 14.71
Average delay will change if different visual filters will be applied.

 ### [4] Some other insights
 
 ### Class
 
 1.1) 47.87 % customers travelled by Business class.
 
 1.2) 44.89 % customers travelled by Economy class.
 
 1.3) 7.25 % customers travelled by Economy plus class.
 
         thus, maximum customers travelled by Business class.
 
 ### Age Group
 
 2.1)  21.69 % customers belong to '0-25' age group.
 
 2.2)  52.44 % customers belong to '25-50' age group.
 
 2.3)  25.57 % customers belong to '50-75' age group.
 
 2.4)  0.31 % customers belong to '75-100' age group.
 
         thus, maximum customers belong to '25-50' age group.
         
### Customer Type

3.1) 18.31 % customers have customer type 'First time'.

3.2) 81.69 % customers have customer type 'returning'.
       
       thus, more customers have customer type 'returning'.

### Type of travel

4.1) 69.06 % customers have travel type 'Business'.

4.2) 30.94 % customers have travel type 'Personal'.

        thus, more customers have travel type 'Business'.


