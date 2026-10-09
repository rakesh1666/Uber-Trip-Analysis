# 📝 Problem Statement – Uber Trip Analysis (Dashboard 1: Overview Analysis)

## 1. Background
Uber operates thousands of trips every day across New York City. Every trip generates data such as pickup and drop-off time, distance, fare, surge fee, vehicle type, payment method and location. Without a proper analysis, this data does not help the business understand **when, where and how** customers book rides, or **which services generate the most revenue**.

## 2. Business Objective
Analyse Uber trip data of **June 2024** using Power BI to understand:
- booking trends and revenue generation,
- trip efficiency in terms of distance and duration,
- customer behaviour across payment methods, vehicle types and time of day,
- demand across locations,

so that stakeholders can make data-driven decisions on **pricing, driver availability and customer experience**.

## 3. Dataset
| Table | Rows | Key Columns |
|---|---|---|
| `Trip Details` | 103,728 | Trip ID, Pickup Time, Drop Off Time, passenger_count, trip_distance, PULocationID, DOLocationID, fare_amount, Surge Fee, Vehicle, Payment_type |
| `Location Table` | 265 | LocationID, Location, City |

Relationships: `Trip Details[PULocationID]` → `Location Table[LocationID]` (active, pickup) and `Trip Details[DOLocationID]` → `Location Table[LocationID]` (inactive, drop-off, used through DAX).

## 4. KPIs to Track
| KPI | Question it answers |
|---|---|
| Total Bookings | How many trips were booked in the selected period? |
| Total Booking Amount | How much revenue (fare + surge fee) was generated? |
| Average Booking Amount | What is the average revenue per trip? |
| Total Trip Distance | How many miles were covered in total? |
| Average Trip Distance | How far does a customer travel on average? |
| Average Trip Time | How long does an average trip take? |

## 5. Required Visuals
1. **Measure selector** (disconnected table) to switch visuals between *Total Bookings*, *Total Trip Distance* and *Total Booking Amount*, with a dynamic chart title.
2. **Bookings by Payment Type** – donut chart.
3. **Bookings by Trip Type (Day / Night)** – donut chart.
4. **Vehicle Type Analysis** – table with Total Bookings, Total Booking Amount, Average Booking Amount and Total Trip Distance for every vehicle type.
5. **Total Booking Amount by Day** – area chart to spot daily trends and peak days.
6. **Location Analysis**
   - Most frequent pickup point
   - Most frequent drop-off point (uses the inactive relationship)
   - Farthest trip (pickup, drop-off and distance)
7. **Top 5 Locations by Total Bookings.**
8. **Most Preferred Vehicle by Pickup Location.**
9. **Slicers** for Date and City.

## 6. Expected Outcomes
- Identify trends in bookings and revenue.
- Understand trip efficiency (distance vs. duration).
- Compare booking patterns across payment types, vehicle types and day/night.
- Find high-demand locations to improve driver availability and surge pricing.
- Provide insights to optimise pricing and improve customer satisfaction.

## 7. Scope
This project covers **Dashboard 1 – Overview Analysis**.

## 8. Tools
Power BI Desktop · DAX · Power Query · Microsoft Excel

---
*Project idea and dataset are based on a Power BI practice project problem statement; the analysis, data cleaning, dashboard and insights are done independently by the author.*
