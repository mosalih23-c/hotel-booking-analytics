# 🏨 Hotel Booking Analytics Dashboard

## 📊 Overview

This project is an end-to-end **Hotel Booking Analytics** project built using **Power BI, Power Query, and DAX**.

The goal of the project is to analyze hotel booking data and transform raw booking records into an interactive dashboard that provides insights into:

- Booking performance
- Revenue
- Customer behavior
- Cancellation patterns
- Hotel performance
- Booking channels
- Market segments
- Lead time
- Length of stay

The project demonstrates the complete data analytics workflow, from data cleaning and transformation to business analysis and interactive dashboard development.

---

## 🛠️ Tools & Technologies

- **Power BI**
- **Power Query**
- **DAX**
- **Data Cleaning**
- **Data Transformation**
- **Data Modeling**
- **Business Intelligence**
- **Interactive Dashboard Design**

---

## 🔄 Project Workflow

```text
Raw Hotel Booking Data
        ↓
Power Query
        ↓
Data Cleaning & Transformation
        ↓
Feature Engineering
        ↓
DAX Measures
        ↓
Interactive Power BI Dashboard
        ↓
Business Insights

🧹 Data Preparation with Power Query
Power Query was used to clean and transform the dataset before building the dashboard.
Main transformations included:
- Data type correction
- Handling invalid records
- Removing unnecessary records
- Creating a complete arrival date
- Calculating total nights
- Calculating total guests
- Calculating estimated booking revenue
- Creating arrival month number
- Creating arrival quarter
- Creating cancellation status
- Creating hotel type
- Creating lead time groups
Key Calculated Columns
Total Nights
Total Nights =
Weekend Nights + Week Nights

Total Guests
Total Guests =
Adults + Children + Babies

Booking Revenue
Booking Revenue =
ADR × Total Nights

Lead Time Groups
Bookings were categorized into:
- 0–7 Days
- 8–30 Days
- 31–90 Days
- 91–180 Days
- 181+ Days
📐 DAX Measures
Several DAX measures were created to support the dashboard.
Total Bookings
Total Bookings =
COUNTROWS(Hotel_Bookings_Cleaned)

Cancelled Bookings
Cancelled Bookings =
CALCULATE(
    [Total Bookings],
    Hotel_Bookings_Cleaned[is_canceled] = 1
)

Cancellation Rate
Cancellation Rate =
DIVIDE(
    [Cancelled Bookings],
    [Total Bookings]
)

Total Booking Revenue
Total Booking Revenue =
SUM(Hotel_Bookings_Cleaned[booking_revenue])

Average ADR
Average ADR =
AVERAGE(Hotel_Bookings_Cleaned[adr])

Average Length of Stay
Average Length of Stay =
AVERAGE(Hotel_Bookings_Cleaned[total_nights])

Total Guests
Total Guests =
SUM(Hotel_Bookings_Cleaned[total_guests])

📊 Dashboard
The Power BI report contains three analytical pages plus a cover page.
🏠 Cover
The cover page provides:
- Project title
- Hotel analytics branding
- Project author
- Navigation buttons
- Access to all dashboard pages
📈 1. Hotel Booking Overview
This page provides an executive overview of hotel booking performance.
KPIs
- Total Bookings
- Cancelled Bookings
- Cancellation Rate
- Total Booking Revenue
Visualizations
- Bookings by Hotel Type
- Booking Trend
- Cancellation Status
- Booking Revenue by Hotel Type
- Average ADR Trend
Filters
- Hotel Type
- Cancellation Status
- Customer Type
- Market Segment
👥 2. Customer & Booking Analysis
This page focuses on customer behavior and booking patterns.
KPIs
- Average Length of Stay
- Total Guests
- Average ADR
Visualizations
- Bookings by Customer Type
- Bookings by Market Segment
- Bookings by Distribution Channel
- Bookings by Lead Time Group
- Average Length of Stay by Customer Type
Filters
- Hotel Type
- Customer Type
- Market Segment
- Lead Time Group
🏨 3. Hotel Performance & Cancellation Analysis
This page focuses on hotel performance and cancellation behavior.
KPIs
- Total Bookings
- Cancellation Rate
- Average ADR
- Total Booking Revenue
Analysis
- Revenue by Hotel Type
- Cancellation Rate by Hotel Type
- Cancellation Rate by Deposit Type
- Cancellation Rate by Lead Time
- Hotel performance comparison
Filters
- Hotel Type
- Deposit Type
- Lead Time Group
💡 Business Questions
The dashboard was designed to answer questions such as:
- Which hotel type generates more booking revenue?
- Which hotel type has a higher cancellation rate?
- Which customer segments generate the most bookings?
- Which market segments are most important?
- How do booking channels differ in performance?
- Does longer lead time relate to higher cancellation rates?
- Which deposit types are associated with higher cancellation?
- How does ADR change over time?
- How long do different customer types typically stay?
🎯 Project Objectives
The main objectives of this project were to:
1. Clean and prepare hotel booking data.
2. Perform data transformation using Power Query.
3. Create meaningful analytical features.
4. Build reusable DAX measures.
5. Develop an interactive Power BI dashboard.
6. Analyze booking, customer, revenue, and cancellation patterns.
7. Convert raw data into actionable business insights.
📁 Project Structure
hotel-booking-analytics/
│
├── README.md
├── Hotel-Booking-Analytics.pbix
│
├── screenshots/
│   ├── cover.png
│   ├── hotel_booking_overview.png
│   ├── customer_booking_analysis.png
│   └── hotel_performance.png
│
└── .gitignore

The original dataset is not included in this repository.

📸 Dashboard Preview
Cover

Hotel Booking Overview

Customer & Booking Analysis

Hotel Performance & Cancellation Analysis

👨‍💻 Author
Mohamed Salih
Data Analyst | Business Intelligence | Data Science
This project was developed as part of my Data Analytics & Business Intelligence portfolio to demonstrate practical skills in data preparation, Power Query, DAX, and Power BI dashboard development.
⭐ Key Skills Demonstrated
- Power BI
- Power Query
- DAX
- Data Cleaning
- Data Transformation
- Feature Engineering
- KPI Development
- Business Analysis
- Interactive Dashboard Design
- Data Visualization
- Business Intelligence