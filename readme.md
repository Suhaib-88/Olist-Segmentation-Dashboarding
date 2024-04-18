# Seller Segmentation of Brazilian eCommerce, Visualization and Reporting 

## Problem Statement

In this project, we will analyze customer orders placed between 2016-2018 from sellers on the Brazilian eCommerce platform Olist Store. From this data, we will first determine the number of customers by geographic region (looking at zip code prefix, city, and state), most popular products, number of repeat customers and purchases, and total purchases by date. After data cleaning and initial analysis, we will use machine learning to make predictions on customer behavior, providing sellers on Olist the opportunity to increase sales and customer base.

## Description of the of dataset:

The Brazilian-eCommerce dataset from Kaggle is used in our analysis:
- This dataset contains approximately 100,000 customer orders, along with corresponding files on product information and English translations of product categories originally in Portuguese. 
- Seller names in this dataset were anonymized and replaced with Game of Thrones House names. 
- Nine files from the original Kaggle dataset were chosen for further analysis: *olist_geolocation_dataset, olist_customers_dataset, olist_sellers_dataset, olist_product_dataset, olist_order_items_dataset, olist_orders_dataset, olist_order_payments_dataset, olist_order_reviews_dataset and product_category_name_translation*.

- Data Source: https://www.kaggle.com/olistbr/brazilian-ecommerce

### Questions we hope to answer with our data:

With this data, we hope to answer...

What are business trends like for Olist, in general?
What data features impact review scores the most?
Can we predict review scores using machine learning?

## Database
We used SQL Server to create data tables in SQL. The Entity Relationship Diagram(ERD) below shows the connectivity between the 11 data tables used in our analysis.
![Sql Schema](https://raw.githubusercontent.com/Suhaib-88/Olist-Segmentation-Dashboarding/master/static/sql_schema.png)


## Transformation
Deliverable: Documentation of any cleaning or manipulation of data.

For data processing I worked with both PowerBI and Excel.

Before starting with the analysis data needs to be cleaned. The cleaning process:

- Removed unnecessary records.
- Removed trailing spaces from all the Queries.
- Removed columns with inconsistencies.
- Changed the mismatched data types.
- Split date-time columns into two separate columns: date, time.
- Derived columns such as duration_delivery_delayed, weekday_vs_weekend_delivery, duration(in days), duration(in hours)etc.
- Changed the dates format consistently throughout the dataset.
- Renamed the columns in a meaningful, user friendly way
- Mapped product categories from portuguese to english
- Translated review comments from portuguese to english: in order to make rating-score wise analysis of negative vs positive sentiment words 

## Dashboarding
### Data Modelling in PowerBI
![Data modelling](https://raw.githubusercontent.com/Suhaib-88/Olist-Segmentation-Dashboarding/master/static/datamodel-olist.jpg)

### Overview Page
![Overview Page](https://raw.githubusercontent.com/Suhaib-88/Olist-Segmentation-Dashboarding/master/static/home.jpg)

### Marketing Leads Page
![Marketing Page](https://raw.githubusercontent.com/Suhaib-88/Olist-Segmentation-Dashboarding/master/static/marketing-leads.jpg)

### Revenue Page
![Revenue Page](https://raw.githubusercontent.com/Suhaib-88/Olist-Segmentation-Dashboarding/master/static/revenue-.jpg)

### Customer Analysis Page
![Customer Page](https://raw.githubusercontent.com/Suhaib-88/Olist-Segmentation-Dashboarding/master/static/customer.jpg)

### Delivery Analysis Page
![Delivery Page](https://raw.githubusercontent.com/Suhaib-88/Olist-Segmentation-Dashboarding/master/static/delivery.jpg)

### Late Delivery Investigation Page
![Late-Delivery Page](https://raw.githubusercontent.com/Suhaib-88/Olist-Segmentation-Dashboarding/master/static/late-delivery.jpg)

### User Seniment Analysis Page
![Seniment Page](https://raw.githubusercontent.com/Suhaib-88/Olist-Segmentation-Dashboarding/master/static/sentiment.jpg)

### Detailed Sentiment Analysis Page
![Detailed Page](https://raw.githubusercontent.com/Suhaib-88/Olist-Segmentation-Dashboarding/master/static/sentiment_detail.jpg)

## Clustering

For clustering analysis, I worked on Pyspark notebooks-databricks due to the computational speed and to evaluate clustering analysis using both sparkML and scikit-learn libraries. Check out the notebooks section in the repo.
![cluster selection Page](https://raw.githubusercontent.com/Suhaib-88/Olist-Segmentation-Dashboarding/master/static/final_clustering_selection.jpeg)

## Final model Selection
https://databricks-prod-cloudfront.cloud.databricks.com/public/4027ec902e239c93eaaa8714f173bcfc/8667267216737444/981413217912682/6052381717536981/latest.html

## Result Takeaways
![cluster selection Page](https://raw.githubusercontent.com/Suhaib-88/Olist-Segmentation-Dashboarding/master/static/results_takeaway.jpeg)

## Recommendation 
Checkout the final report for a detailed report and recommendation:
![final Page](https://raw.githubusercontent.com/Suhaib-88/Olist-Segmentation-Dashboarding/master/Final%20Marketplace%20Report.pdf)
