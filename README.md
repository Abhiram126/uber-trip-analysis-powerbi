# 🚖 Uber Trip Data Analysis | Power BI

## 📊 Project Overview

Uber Trip Data Analysis is an interactive Power BI dashboard built to analyze Uber trip data and generate insights into bookings, booking value, trip distance, trip duration, payment methods, vehicle types, locations, and time-based demand patterns.

The project turns raw Uber trip data into an interactive business intelligence dashboard that supports data-driven decisions on demand, driver allocation, pricing, and operational efficiency.

---

## 🎯 Business Requirement

The objective of this project is to analyze Uber trip data using Power BI to understand:

- Booking trends and revenue generation
- Trip efficiency based on distance and duration
- Demand variation across time and day
- Location-based booking patterns
- Customer payment preferences
- Vehicle performance and preferences
- High-demand pickup and drop-off locations

---

## 🛠️ Tools & Technologies

- Power BI
- Power Query
- DAX
- Data Modeling
- Data Visualization
- Microsoft Excel

---

## 📁 Dataset

The project uses the following datasets:

- `Uber Trip Details.xlsx`
- `uber Location Table.xlsx`

The trip data contains:

- Trip ID
- Pickup Date
- Pickup Time
- Vehicle Type
- Payment Type
- Passenger Count
- Pickup Location
- Drop-off Location
- Trip Distance
- Booking Value

---

## 🧹 Data Preparation

Power Query was used to prepare the raw data for analysis:

- Removed duplicate records
- Handled null and missing values
- Corrected date and time formats
- Replaced missing payment types
- Prepared the data for analysis and visualization

---

## 🗂️ Data Model

A star-schema approach was used to organize the data model:

| Table | Purpose |
|-------|---------|
| **Trip Details** | Main trip (fact) data |
| **Location Table** | Pickup and drop-off location information |
| **Calendar Table** | Date and day analysis |
| **Dynamic Measure Table** | Dynamic metric selection |

![Data Model](screenshots/Screenshot%20(1).png)

---

## 📐 DAX Measures

Key DAX measures used in the dashboard:

```DAX
Total Bookings = COUNTROWS(TripDetails)

Total Revenue = SUM(TripDetails[BookingValue])

Avg Trip Distance = AVERAGE(TripDetails[Distance])

Avg Trip Duration = AVERAGE(TripDetails[Duration])
```

A dynamic measure selector was also implemented for:

- Total Bookings
- Total Booking Value
- Total Trip Distance

This lets dashboard visuals change dynamically based on the selected metric.

---

## 📊 Dashboard

### 1. Overview Analysis

The Overview Analysis page gives a high-level view of Uber's operational and financial performance.

**Key Performance Indicators**

| KPI | Value |
|-----|-------|
| Total Bookings | 103.7K |
| Total Booking Value | $1.6M |
| Average Booking Value | $15 |
| Total Trip Distance | 349K miles |
| Average Trip Distance | 3 miles |
| Average Trip Time | 16 minutes |

**Visualizations**

- Payment Type Analysis
- Day/Night Trip Analysis
- Total Bookings by Day
- Vehicle Type Analysis
- Total Bookings by Location
- Preferred Vehicle by Pickup Location
- Most Frequent Pickup Point
- Most Frequent Drop-off Point
- Farthest Trip

![Overview Dashboard](screenshots/Screenshot%20(2).png)

### 2. Time Analysis

The Time Analysis page focuses on booking patterns across different times and days.

**Visualizations**

- Total Bookings by Pickup Time
- Total Bookings by Day Name
- Hour vs Day Heatmap
- Dynamic KPI Selection

This analysis helps identify peak and off-peak demand periods and supports better driver scheduling and operational planning.

![Time Analysis Dashboard](screenshots/Screenshot%20(3).png)

### 3. Details

The Details page provides a granular view of individual trip records.

**Table columns**

- Trip ID
- Pickup Date
- Vehicle
- Payment Type
- Number of Passengers
- Location
- Trip Distance
- Booking Value
- Pickup Hour

![Details Dashboard](screenshots/Screenshot%20(4).png)

---

## 🔍 Key Insights

- Uber Pay accounts for approximately **67%** of recorded payments.
- Day trips account for approximately **73%** of bookings.
- **UberX** generates the highest booking value among the vehicle types shown.
- Booking demand is concentrated during daytime and evening hours.
- **Penn Station / Madison Sq. West** is a top pickup location.
- **Upper East Side North** is a frequent drop-off location.
- The farthest trip is from **Lower East Side to Crown Heights North**, covering approximately **144.1 miles**.

---

## 💼 Business Impact

The dashboard can support decisions in areas such as:

- Demand forecasting
- Driver allocation
- Fleet planning
- Pricing decisions
- Location-based promotions
- Peak and off-peak demand planning
- Understanding customer payment preferences
- Understanding vehicle preferences by location

---

## 📈 Decision Support & Recommendations

Based on the analysis, stakeholders can:

- Increase driver availability in high-demand areas
- Optimize driver scheduling during peak hours
- Analyze demand patterns to inform pricing
- Promote preferred digital payment methods
- Run targeted promotions during low-demand periods
- Optimize vehicle availability based on location demand

---

## 🚀 Future Scope

- AI-based demand prediction
- Real-time trip monitoring
- Multi-city performance analysis
- Weather and holiday data integration
- Event-based demand analysis
- Driver behavior analysis
- Customer behavior analysis

---

## 📂 Project Structure

```
uber-trip-analysis-powerbi/
│
├── README.md
├── Uber_Analysis_25.pbix
├── Uber Trip Details.xlsx
├── uber Location Table.xlsx
├── uber Problem Statement.docx
├── Uber Trip Data Analysis CASE STUDY PPT 2.pptx
│
└── screenshots/
    ├── Screenshot (1).png
    ├── Screenshot (2).png
    ├── Screenshot (3).png
    └── Screenshot (4).png
```

---

## 👨‍💻 Author

**Nallamothu Abhiram**
B.Tech – Computer Science (AI/ML)

**Connect with me**

- [GitHub](https://github.com/Abhiram126)
- [LinkedIn](https://www.linkedin.com/in/nallamothu-abhiram-chowdary-12714629b)

---

## ⭐ Project Summary

This project demonstrates the use of Power BI, Power Query, DAX, data modeling, and data visualization to transform raw Uber trip data into an interactive analytical dashboard that generates insights to support data-driven business decisions.
