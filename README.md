# Swiggy-Food-Delivery-Analytics-Delivery-Time-Prediction

## Project Overview
This project focuses on analyzing food delivery data to understand customer behavior, restaurant performance, and delivery efficiency.
Along with analytics and visualization, a machine learning model is built to predict delivery time, helping improve operational planning and customer satisfaction.
The project follows a complete data workflow:
SQL → Python → Machine Learning → Tableau → Business Insights

## Business Objectives
-Identify top-performing restaurants and loyal customers
-Understand delivery time patterns and influencing factors
-Analyze food demand (Veg vs Non-Veg, popular dishes)
-Predict delivery time using machine learning
-Present insights through an interactive Tableau dashboard

## Tools & Technologies Used
-**SQL** – Data extraction, joins, KPIs, business queries
-**Python (Pandas, NumPy)** – Data cleaning & feature engineering
-**Machine Learning (Scikit-learn)** – Delivery time prediction
-**Tableau Public** – Dashboard & storytelling
-**GitHub** – Version control & project documentation

## Data Description
The dataset consists of multiple relational tables representing different parts of a food delivery system.
**1. Customers**
Contains customer-level information.
  -user_id – Unique customer identifier
  -name – Customer name
  -email – Customer email
Used to analyze customer behavior and loyalty.
**2. Orders**
Stores transaction-level order details.
  -order_id – Unique order identifier
  -user_id – Customer who placed the order
  -r_id – Restaurant identifier
  -amount – Total order value
  -date – Order date
  -delivery_time – Delivery duration (target variable for ML)
  -delivery_rating, restaurant_rating – Customer feedback
This table acts as the central fact table for analysis.
**3. Restaurants (Cuisine)**
Contains restaurant details.
  -r_id – Restaurant identifier
  -r_name – Restaurant name
  -cuisine – Cuisine type
  -city, state – Location details
Used to analyze restaurant performance and cuisine demand.
**4. Dishes**
Contains dish-level information.
  -f_id – Food item identifier
  -f_name – Dish name
  -type – Veg / Non-Veg
Helps in understanding food preferences and popularity.
**5. Order Details**
Maps orders to dishes (many-to-many relationship).
  -order_id – Order identifier
  -f_id – Dish identifier
Used to calculate items per order and popular dishes.
**6. Menu & Pricing (Card)**
Stores restaurant menu pricing.
  -r_id – Restaurant identifier
  -f_id – Dish identifier  
  -price – Price of dish
Used for price-based analysis and feature engineering.

## Data Integration
All tables were joined using:
**SQL** for data extraction, joins, and KPI creation
**Python (Pandas)** for final merging, cleaning, and feature engineering
This resulted in a single analytical dataset used for:
  -Business insights
  -Tableau dashboard
  -Machine learning model

## SQL Analysis
SQL was used to:
-Join multiple tables (orders, customers, restaurants, dishes)
-Calculate KPIs:
   -Total revenue per restaurant
   -Most loyal customers
   -Average delivery time
   -Most popular dishes
-Prepare clean datasets for analytics and ML
SQL queries are available in the /sql folder.

## Machine Learning (Delivery Time Prediction)
-Target Variable: Delivery Time (minutes)
-Models Used:
    -Linear Regression
    -Random Forest Regressor
-Final Model Selected: 
    -Linear Regression (better performance)

## Key Features Used:
-Order amount
-Day, month, weekend flag
-Customer order behavior
-Restaurant ratings & historical delivery time
-Item-level pricing
Feature importance analysis was performed to explain business impact.

## Tableau Dashboard
An interactive dashboard was created to visualize:
  -KPI cards (Fastest delivery, Top revenue, Loyal customer, Popular dish)
  -Restaurant-wise revenue
  -Customer loyalty
  -Delivery time vs rating
  -Monthly revenue trend
  -Veg vs Non-Veg demand
  -Cuisine-wise demand
 Tableau Public link: [(add your link here)](https://public.tableau.com/views/swiggy_17667065175410/Dashboard1?:language=en-GB&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

 ## Key Business Insights
  -Higher-rated restaurants do not always deliver faster
  -Delivery time varies significantly by restaurant and day
  -Certain dishes drive repeat orders and loyalty
  -Veg items dominate overall demand in this dataset
  -Order amount has limited impact on delivery speed

  ## Conclusion
  This project demonstrates an end-to-end data analytics pipeline with real-world business relevance.
  It combines SQL, machine learning, and visualization to support operational decision-making in food delivery platforms.
