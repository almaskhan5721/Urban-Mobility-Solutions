# Urban Mobility Solutions Bike-Sharing Program
## Table of Contents
   - [Project Description](#project-description)
   - [Business Introduction](#business-introduction)
   - [Aim of the project analysis](#aim-of-the-project-analysis)
   - [Processes](#processes)
   - [Insights](#insights)

## Project Description
The project is to analyse data from January 2025 to build a data model, clean the data, create a dashboard, and answer analytical questions to improve the program's efficiency and user experience.
<img width="1524" height="761" alt="Screenshot 2025-09-13 205724" src="https://github.com/user-attachments/assets/a1f6001a-94eb-481e-8af4-10cd479c84e1" />

### Business Introduction
Urban Mobility Solutions (UMS) operates a bike-sharing program in a large city, offering both standard and electric bikes for short-term rentals. The program aims to promote sustainable transportation, reduce traffic congestion, and improve urban mobility. UMS collects data on bike rentals, station usage, customer demographics, maintenance logs, and weather conditions to optimize operations.
### Aim of the project analysis
The primary objective of this project are as follows:
- Identify high- and low-usage stations and their neighborhood trends.
- Analyze how temperature and precipitation affect ride volume.
- Calculate the percentage of bikes in maintenance by type.
- Compare average ride duration by MembershipType and age group.
- Identify stations with low capacity utilization.
### Processes
- Step 1: Data Cleaning and Transformation
  Tools: PowerQuery
  * Missing EndTime values for some rides.
  * Inconsistent RideDuration_Minutes (e.g., negative values or mismatches with StartTime/EndTime).
  * Duplicate RideID entries. Inconsistent date formats (e.g., "12/20/2024" vs. "2024-12-20").
  * Missing LastMaintenanceDate for some bikes.
  * Invalid Status entries (e.g., typos like "Maintanance"). Missing or invalid Latitude/Longitude values (e.g., 0 or negative out-of-range).
  * Inconsistent Neighborhood names (e.g., "DownTown" vs. "Downtown").
  * Duplicate StationID entries.
  
- Step 2: Data Modeling
  Tools: PowerBI Data Model, DAX
  * Defined relationships between tables(Ride_Transactions, Rider_Demographics, Bike_Inventory, Station_Details, Weather_Data)
  * Created measures using DAX for key KPIs like Total rides, average ride duration, and active bikes.

- Step 3: Analysis and Dashboard Creation
  Tools: Power BI Visualization
  * Built interactive dashboards with filters, slicers and drill-through functionality.
  * Used Line Chart: Daily ridership trends (count of rides per day), Bar Chart: Top 5 stations by ride starts, Pie Chart: Distribution of rides by RideType (Standard vs. Electric), Map Visual: Station locations with bubble size based on ride volume, Table/Matrix: Maintenance status by bike type.
  * Created KPI Cards: Total rides, average ride duration, and active bikes.
    
### Insights
  - Identify high and low-usage stations and their neighborhood trends:
    According to top 5 stations by ride start bar chart, Station C and F has highest usage with 31 ride counts whereas Stations M has lowest usage with 14 ride counts. When you filter the bar chart by using neighbourhood slicer it shows in Downtown neighbourhood Station C has highest usage. So basically Station C in downtown and Station F in westside has highest usage, as population living in downtown prefer to use bikes over cars.
    <img width="395" height="258" alt="Screenshot 2025-09-13 211653" src="https://github.com/user-attachments/assets/86d9ea35-158f-45ec-a0af-354b601f31f1" />
    
  - Analyze how temperature and precipitation affect ride volume:
    According to dashboard if applied filter on weather condition, then it will show that only in rainy days we have ride data. Total rides in kpi is 489 but with slicers on rainy days total ride will decrease to 484.
    
  - Calculate the percentage of bikes in maintenance by type:
    According to dashboard if applied filter on weather condition, then it will show that only in rainy days we have ride data. Total rides in kpi is 489 but with slicers on rainy days total ride will decrease to 484
    <img width="400" height="165" alt="Screenshot 2025-09-13 211849" src="https://github.com/user-attachments/assets/4dc6dc41-2f27-42b5-9437-e26c7764c197" />

  - Compare average ride duration by MembershipType and age group:
    According to average ride duration kpi card if you filter by membership type it shows highest durations is 33 minutes with annual and monthly membership type. According to line chart age group 18-25 has highest average ride duration i.e. 38 for annual, 35 for monthly, and 34 for pay-per-ride membership type.
    <img width="407" height="268" alt="Screenshot 2025-09-13 211947" src="https://github.com/user-attachments/assets/bc3c9363-b264-4109-9c7d-4a9d025472fe" />

  - Identify stations with low capacity utilization:
    According to Station utilization table chart, all stations have utilization ration more than 1 which means none of station is empty or balance but are over utilized with maximum of 4.9 utilization ration of station C. May be increase docking facility in     overused stations can help to balance the capacity by total rides per station. Also may be making new station in high demand neighbourhoods can help in rebalancing.
    
    <img width="418" height="501" alt="Screenshot 2025-09-13 211405" src="https://github.com/user-attachments/assets/f759b2e1-a034-44f7-b332-111c8111480c" />

#### Note
    Check the files section for the Power BI file and datasets
