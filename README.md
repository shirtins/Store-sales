# Store sales-Dashboard

### Dashboard Link : https://app.powerbi.com/groups/me/reports/c6b6ae6e-2c34-4459-a5cf-3b4e2c9c110e/ReportSection?experience=power-bi

## Problem Statement

Super store wants to know how well their company have been doing for the past 3 years in business and will want to know key insights to focus on for the next year. They also want to build up their customer service by knowing and having a better relationship with their top customers.
This dashboard helps the Store understand the trend of their revenue and also know their customers better. It helps the airlines know if their customers are satisfied with their services. Through different areas, they get to know their improvement area, & thus they can improve their services by identifying these area. It also helps them to knwo key products and their category that affect revenue

#
Below is the dashboard for the Store sales and attached in this path is the data used for the Dashboard

![Store sales report_page-0001](https://github.com/user-attachments/assets/2a073091-c40a-4036-9b28-75b45be799d9)
## Steps followed 

- Step 1 : Load data into Power BI Desktop, dataset is a csv file.
- Step 2 : Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.
- Step 3 : Also since by default, profile will be opened only for 1000 rows so you need to select "column profiling based on entire dataset".
- Step 4 : It was observed that in none of the columns errors & empty values were present.
- Step 5 : In the report view, under the view tab, theme was selected.
- Step 7 : Since the data contains various ratings, thus in order to represent ratings, a new visual was added using the three ellipses in the visualizations pane in report view. 
- Step 8 : Visual filters (Slicers) were added for 2 fields named "Goods Category" and "Order date". This enables the store understand how sales have been for specific dates and the good category that were of noticeable help to the revenue.
- Step 9 : A card visual was used to represent the *most sold product* which changes with respect to the given filter, thus it is dynamic. DAX function was used;
        
        Most sold product = 
        CALCULATE(
            MAX(sales[Product_Name]),
            FILTER(
                sales,
                sales[Total Order] = MAX(sales[Total Order])))


- Step 10 : Five card visuals joined together shows the necessary KPIs for the store sales: "Total Revenue", "Avg order value", Total goods sold", "Total Orders", and "Avg goods per order". These were made using the necessary measures.
Below is a snipshot of the KPIs.

![Screenshot 2024-10-12 151010](https://github.com/user-attachments/assets/a667f878-6693-4404-9037-ad09fb3d4c5a)


- Step 11 : In focusing on out top buyers a Treemap was used to show the top 3 buyers.

Step 12 : A bar chart was created to show the daily trend of Total orders and a line chart was used to show the monthly trend of total orders. This was done separately to enable one see for a particular month which days have more orders.

- Step 13 : Knowing that their customers are from different states in the USA, a shape map was used to show the different states where their customers order from, The intensity of the below map is based on the total revenue with a tooltip also showing the total orders and goods sold.
Below is the snip shot.
![Screenshot 2024-10-12 152348](https://github.com/user-attachments/assets/52ba7c21-41de-400e-b948-553720f61e8c)

- Step 14 : The Store divides their products into segments: "Consumer", "Corporate" and " Home Office". A funnel chart was created to show the profict made from each segment.



# Insights

A single page report was created on Power BI Desktop & it was then published to Power BI Service.

Following inferences can be drawn from the dashboard;

### [1] Most sold product of all time: Xerox 1908 (A colour printer).

   Based on different Goods category:


          1. Furniture: Executive Impressions 13" Clairmont Wall Clock.
          2. Office Supplies: Xerox 1908
          3. Technology: Logitech P710e Mobile Speakerphone 
           
### [2] The company wants to know their top 3 buyers for each category:
   Furniture:

    a) Seth Vernon
    b) Joel Easton
    c) Justin Deggeller
  
  This can also be seen for the other two categories.

  
  ### [3] Month and daily trend of sales.
  
      a) Beginning months of the year experienced the least sales 
         while the last 4 months had the highest sales with November being the month with highest sales.
      b) Saturdays and Sundays were the days of least sales while Friday was day of highest sales followed by monday

 ### [4] Some other insights

 ### PRODUCTS
 - The Technology proudcts generate more revenue than the other 2 product category even as it has the least number of orders
 - Furniture products given the least profit though with high revenue
  
 ### SEGMENT
 
 1.1) Consumer products made more profit out of the three segments
 
 1.2) Technology products made highest sales out of the consumer segment

 ### STATE
 *California* stands as the state of highest sales order, followed by *New York*, these two states should serve as best options for establishment of stores for easier delivery.
 



