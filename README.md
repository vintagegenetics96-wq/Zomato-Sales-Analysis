# Zomato-Sales-Analysis

📊 Power BI Project: Zomato Sales Analysis
1️⃣ Project Overview
Project Title: Zomato Sales & Customer Insights Dashboard
Tool Used: Power BI
Domain: Food Delivery / E-commerce Analytics

Objective:
Analyze Zomato sales data to understand:

Revenue trends

Customer behavior

City-wise & restaurant-wise performance

Order patterns and ratings

2️⃣ Dataset Description
You can assume or create a dataset with the following tables:

📁 Table 1: Orders
Column Name	Description
Order_ID	Unique order ID
Order_Date	Date of order
Customer_ID	Unique customer
Restaurant_ID	Restaurant identifier
City	City name
Order_Amount	Total bill amount
Delivery_Time (min)	Delivery duration
Payment_Mode	Cash, UPI, Card
Order_Status	Delivered / Cancelled

📁 Table 2: Restaurants
Column Name	Description
Restaurant_ID	Unique ID
Restaurant_Name	Name
Cuisine	Food category
Rating	Customer rating
City	Location

📁 Table 3: Customers
Column Name	Description
Customer_ID	Unique ID
Customer_Name	Name
Gender	M/F
Age	Age
City	City

3️⃣ Data Cleaning (Power Query)
Removed null & duplicate values

Converted date format

Standardized city names

Removed cancelled orders for sales analysis

Created Year, Month, Day columns

4️⃣ Data Model
Orders ↔ Customers (Customer_ID)

Orders ↔ Restaurants (Restaurant_ID)

One-to-Many relationships

⭐ Star schema used for performance.

5️⃣ Key DAX Measures
Total Sales = SUM(Orders[Order_Amount])

Total Orders = COUNT(Orders[Order_ID])

Average Order Value = 
DIVIDE([Total Sales], [Total Orders])

Delivered Orders =
CALCULATE(
    COUNT(Orders[Order_ID]),
    Orders[Order_Status] = "Delivered"
)

Avg Delivery Time =
AVERAGE(Orders[Delivery_Time])

6️⃣ Dashboard Pages

📌 Page 1: Sales Overview
KPIs:

Total Sales

Total Orders

Average Order Value

Average Delivery Time

Visuals:

Line chart: Sales trend by month

Bar chart: Top 10 cities by sales

Donut chart: Payment mode distribution

📌 Page 2: Restaurant Performance
Visuals:

Top restaurants by revenue

Cuisine-wise sales

Ratings vs Sales (scatter chart)

📌 Page 3: Customer Insights
Visuals:

New vs repeat customers

Age group analysis

City-wise customer count

📌 Page 4: Order Analysis
Visuals:

Peak order time (hourly)

Order status distribution

Delivery time analysis


7️⃣ Key Insights (Sample)

📈 Metro cities contribute over 60% of total sales

🍕 Italian & North Indian cuisines generate highest revenue

⏰ Peak order time: 7 PM – 10 PM

⭐ Restaurants with rating >4.2 show higher repeat orders

8️⃣ Business Recommendations
Focus marketing campaigns during peak hours

Improve delivery time in low-performing cities

Promote high-rated restaurants
Offer discounts to repeat customers
