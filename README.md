**#Smart Last-Mile Delivery Optimization (Zepto Delivery Analytics)**

This project presents an end-to-end real-world analytics solution for optimizing last-mile delivery performance for Zepto-like hyperlocal delivery operations. The goal is to identify delivery inefficiencies, optimize driver performance, reduce delays, and improve customer satisfaction by leveraging MySQL for data storage and Power BI for interactive dashboards.
**Project Objective**

Last-mile delivery is the most expensive and time-sensitive part of the logistics chain. This project simulates a real corporate analytics workflow:

✔ Identify high-delay zones
✔ Track distance, delivery time, and fuel consumption
✔ Measure on-time delivery % by location
✔ Analyze delay reasons (Traffic, Weather, Breakdown, Address Issues)
✔ Optimize driver-level performance & fuel efficiency
✔ Provide data-backed recommendations for operational efficiency
**Tech Stack**
🔹 Database Layer

MySQL for storing delivery logs, fuel usage, locations, status & driver records.

SQL used for:

Data cleaning

Calculating KPI metrics

Data modeling for analytics

🔹 Analytics & Visualization Layer

Power BI

Interactive dashboards

DAX measures for KPI calculations

Drill-down analysis (Location → Driver → Delay Reason)

Custom visualizations such as:

Fuel vs Distance Scatter

On-time Delivery Trends

Delay Reason Pie Charts

Quarter-wise Delivery Time Line Charts

Treemaps for Location-wise Metrics
**Key KPIs Developed**
KPI	Description
12.9K Orders	Total deliveries analyzed
97.63% On-time Delivery	Measures delivery efficiency
1961 Delayed Orders	Total failures
165K km Distance	Total distance covered
44.49 min Avg Delivery Time	Service speed benchmark
Fuel Optimization Metrics	Fuel usage per location & driver
**Major Insights & Findings**
🔹 1. On-time Delivery Performance by Location

Some locations achieve 98%+ on-time, while others show higher delay counts (ex: Begumpet, Banjara Hills).

🔹 2. High Delay Reasons Identified

Traffic

Wrong Address

Weather

Vehicle Breakdown

Each reason is quantified and compared across different zones.

🔹 3. Fuel Usage Optimization

Scatter plots show:

Drivers/locations using more fuel for shorter distances

Opportunities to optimize routes

🔹 4. Quarter-wise Delivery Time Trends

Improvement opportunity spotted by studying seasonal patterns in delivery time.

🔹 5. Driver-Level Performance Monitoring

Helps identify high-performing and underperforming drivers.
**DAX Measures Used**:
OnTime Delivery % =
DIVIDE(
    CALCULATE(COUNT(delivery[id]), delivery[status] = "Ontime"),
    COUNT(delivery[id])
)

Average Delivery Time =
AVERAGE(delivery[delivery_minutes])

Delay Count = 
CALCULATE(COUNT(delivery[id]), delivery[status] = "Late")
**Transformations**
The project initially used a MySQL database connected in DirectQuery mode 
to test real-time query execution directly from the SQL source.

For the final model build and performance improvement:
- I converted the connection from DirectQuery to Import mode.
- This reduced refresh dependency on the SQL server.
- Improved Power BI responsiveness during visuals and DAX calculation.
- Allowed for complex transformations using Power Query and DAX.

**Project Conclusion**

This end-to-end Last-Mile Delivery Optimization project showcases how real-time delivery data can be transformed into actionable business insights using SQL, Power BI, and DAX. Through detailed KPI tracking, operational analysis, and performance measurement, the solution provides a complete analytical framework used by companies like Zepto, Swiggy Instamart, Blinkit, Dunzo, and other hyperlocal delivery platforms.

The insights developed from the dashboard help in:

✔ Improving On-Time Delivery Performance
✔ Identifying high-delay locations and root causes
✔ Enhancing fuel efficiency and route performance
✔ Monitoring driver-level productivity
✔ Predicting workload and delivery patterns
✔ Reducing operational costs and optimizing fleet usage
