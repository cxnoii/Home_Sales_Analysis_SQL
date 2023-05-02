# home_sales

## Overview
The purpose of this project is to determine the average price of homes sold based on features of interest. This exploratory analysis of homes sales data will be utilizing SparkSQL. Additionally, the runtimes of SQL queries using uncached tables, cached tables and data read through parquet will be compared. 

## Dataset 
* _date_: date the home was sold
* _date_built_: date the home was built
* _price_: total price of home
* _bedrooms_: number of bedrooms
* _bathrooms_: number of bathrooms
* _sqft_living_: total square feet of the interior of the home
* _sqft_lot_: total square feet of land outside the home
* _floors_: number of floors
* _waterfront_: a value of 0 indicates that the home is not located on a waterfront, 1 indicates that is is a waterfront home
* _view_: a value that judges how nice the view is; higher values indicate nicer views

## SparkSQL Process
In order to being using SparkSQL, a spark session was created. The home_sales dataset is then read into a dataframe from an AWS S3 bucket, where a temporary view must be created in order to begin quering the data using SQL in the spark session.

![image](https://user-images.githubusercontent.com/114107454/235787818-0b623342-ddd3-49db-95f2-50f6c6052ae9.png)

## Results

### Query Results
These queries will all be focused on the average price of homes based on specific criteria:
1.  3bd, 3bath
    *
    
    
### Runtime Results
The runtimes of the query as shown below

![image](https://user-images.githubusercontent.com/114107454/235789219-e5fbefba-0567-4c84-bb34-8cb0cdce4197.png)

*Uncached Table: 
--- 1.0891053676605225 seconds ---

*Cached Table:
--- 0.5521900653839111 seconds ---

*Parquet:
--- 0.4563748836517334 seconds ---
