# Sales-Data-Analysis-Project
Dashboard report for the sales data using powerbi

## Problem Statement

The goal of this project is to analyze sales data and create an interactive dashboard using Power BI. The dashboard will focus on understanding shipment patterns and shipment delays, helping the organization optimize logistics operations and improve customer satisfaction.

### Data sources:

The data for this Power BI dashboard is sourced from CSV file containing sales data of a global super store for five years, from 2011 to 2015.

### Tools:

- **Power BI**: Utilized to design and develop an interactive dashboard, allowing for dynamic data visualization and real-time analysis of sales and shipment data.
- **Power Query**: Responsible for cleaning, transforming, and preparing raw data for analysis, ensuring that the data is accurate, consistent, and ready for visualization.
- **SQL**: Applied to extract, manipulate, and analyze data from the database, facilitating efficient querying and complex data transformations needed for deeper analysis.

###Data Cleaning:
1:Handling Missing Data:
Checking for missing Order Date, Ship Date, and Ship Mode values.
Removing or imputing missing values if necessary (e.g., replace missing dates with averages, or flag them for exclusion).
2:Correcting Data Formatting:
Ensuring Order Date and Ship Date fields are in the correct date format.
Validating that the Ship Mode field only contains valid categories.
3:Removing Duplicates:
Ensuring that there are no duplicate rows, particularly for Order ID.

###Data Analyzing:
1:Analyzing the Shipment Count by Ship Mode:
Using the COUNTROWS function to count the number of shipments for each ship mode.
Creating a DAX measure:
DAX
CountofShipMode= = COUNTROWS(GlobalSuperstores)
Creating a simple table chart to visualize the number of shipments per ship mode.

2:Calculating Date Difference (Order Date vs. Shipment Date):
Calculate the number of days between the Order Date and Shipment Date.
Use the DATEDIFF DAX function:
DAX
DATEDIFFERENCE = DATEDIFF(FIRSTDATE(GlobalSuperstores[OrderDate]),LASTDATE(GlobalSuperstores[ShipDate]),DAY)
Use this field to analyze delivery delays and performance.

3:Creating Visuals:
Creating more visuals including sum of sales, profit, sales over countries in various charts for better understanding.

###Final Report Summary
In the Power BI dashboard:

Shipment Count by Ship Mode: Provides a breakdown of how many shipments were made using each ship mode.
Average Delivery Time: Displays the average time it takes from order to shipment, highlighting any trends or anomalies.



Conclusion: The dashboard effectively visualizes shipment counts and delivery times, offering valuable insights into shipping performance and efficiency. This can drive strategic decisions related to logistics, cost management, and customer satisfaction.






  
 

 

