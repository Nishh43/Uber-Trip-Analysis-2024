
# 🚗 Uber Trip Analysis 2024

## 🔍 Project Overview
This project provides a detailed analysis of Uber trip data from 2024 using Python, Pandas, Seaborn, Plotly, and machine learning techniques.  
It covers end-to-end steps: data cleaning, exploratory data analysis (EDA), interactive visualizations, predictive modeling, and actionable business recommendations.  
Purpose: Help ride-sharing businesses optimize operations, reduce cancellations, and improve customer satisfaction.

## 📊 Dataset Overview
- **Dataset Size:** 150,000 records  
- **Features:** 21 columns, including Date, Time, Booking Status, Vehicle Type, Pickup & Drop Locations, Booking Value, Ride Distance, Ratings, Payment Method, etc.  
- **Date Range:** January 1, 2024 – December 30, 2024  
- **Unique Customers:** 148,788  
- **Unique Pickup Locations:** 176  
- **Unique Drop Locations:** 176  
- **Key Challenge:**  
 Large proportion of missing data in cancellation reasons, ratings, and booking value (~32%).

## ⚙️ Steps Performed

### 1️⃣ Data Cleaning & Preparation
- Converted Date and Time to datetime format.  
- Created features: Hour, DayOfWeek, Month, IsWeekend flag.  
- Created target flags: Is_Successful, Is_Cancelled_Customer, Is_Cancelled_Driver.  
- Encoded categorical variables.  
- Handled missing data by removing or imputing as necessary.

### 2️⃣ Exploratory Data Analysis (EDA)
- Success rate analysis by vehicle type, hour of day, day of week.  
- Revenue distribution by vehicle type, distance category, and hour.  
- Geographic insights: Top pickup & drop locations, most popular routes.  
- Time-based insights: Peak vs Quiet hours, Weekend vs Weekday performance.  
- Customer behavior: Repeat customers, top spenders, rating distributions.

### 3️⃣ Interactive Visualizations
- Success rate by vehicle type (interactive bar chart).  
- Hourly ride volume vs success rate (interactive dual-axis plot).  
- Revenue vs Distance (interactive scatter plot).

### 4️⃣ Predictive Modeling

#### ✅ Model 1: Ride Success Prediction (Random Forest Classifier)
- Accuracy: ~62%  
- Recall on True Class (Successful Rides): 1.00 → Very good.  
- Top Features: Pickup Location Encoded, Drop Location Encoded, Vehicle Type Encoded.  
- 🚀 Suitable for operational decisions (driver allocation, demand forecasting).

#### ⚠️ Model 2: Revenue Prediction (Random Forest Regressor)
- R² Score: ~-0.024 → Very poor, unreliable.  
- RMSE: ₹404.13  
- ➔ This model is not production-ready and is included for learning purposes only.

## 💡 Key Insights & Recommendations

### 📊 Executive Summary
- Total Rides: 150,000  
- Successful Rides: 93,000 (62.0% Success Rate)  
- Total Revenue: ₹47,260,574  
- Avg Ride Value: ₹508  
- Avg Distance: 26.0 km  
- Avg Driver Rating: 4.23/5  
- Avg Customer Rating: 4.40/5  
- Customer Cancellations: 10,500  
- Driver Cancellations: 27,000

### ⏰ Time-Based Insights
- Peak Hour: 18:00 (12,397 rides)  
- Quietest Hour: 4:00 (1,321 rides)  
- Weekend Success Rate: 62.3%  
- Weekday Success Rate: 61.9%

### 🗺 Geographic Insights
- Top Pickup Location: Khandsa (949 rides)  
- Top Drop Location: Ashram (936 rides)  
- Top Route: DLF City Court → Bhiwadi (17 rides)

### 🚀 Business Recommendations
- Optimize driver allocation during peak hours (18:00) to reduce cancellations.  
- Focus on high-performing pickup-drop combinations for resource allocation and promotions.  
- Improve data collection to reduce missing cancellation reasons and ratings.  
- Use success prediction model for improving operational decisions.

### ⚡ Strong Recommendations
- ✅ The Success Prediction Model is ready to showcase as a working component of the project.  
- ⚠️ The Revenue Prediction Model is not reliable and should NOT be used in production.  
 Instead, mention in README:  
  *"Attempted revenue prediction shows poor results (R² ~ 0.05). Future work needed: Advanced features, models (e.g., LightGBM, CatBoost), external data (weather, events).”*
