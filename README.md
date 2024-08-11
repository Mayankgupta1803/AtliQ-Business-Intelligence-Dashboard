

# 🏨 # AtliQ-Hospitality-Business-Intelligence-Dashboard

![Hospitality Dashboard](https://github.com/Mayankgupta1803/AtliQ-Business-Intelligence-Dashboard/blob/9629a8886dbb1fd4b3400b4bdc4e7d362e3000ec/BG.png) <!-- Replace with your own image link -->

## 📊 Overview

This repository contains a comprehensive Power BI dashboard designed to analyze and visualize hospitality revenue data. The dashboard provides insights into key metrics such as revenue, bookings, occupancy rates, and guest ratings across various hotels, cities, and booking channels. The goal is to enable data-driven decision-making for hospitality management by presenting trends, comparisons, and profitability analysis.

## 🎯 Objectives

- **High-Level Overview**: Get a quick summary of key performance indicators (KPIs) like Total Revenue, Total Bookings, Occupancy Rate, ADR, and RevPAR.
- **Channel and City Analysis**: Evaluate performance across different booking channels and cities to identify trends and areas for improvement.
- **Property and Room Category Performance**: Compare revenue, occupancy, and guest ratings across different properties and room categories.
- **Temporal Analysis**: Track booking trends, revenue generation, and occupancy rates over time.
- **Profitability Analysis**: Analyze profitability metrics to optimize operations and increase revenue.

## 📁 Data Sources

The dashboard is built using the following datasets:

1. **date_table.csv**: Contains date-related information such as week number, day type, and month.
2. **dim_hotels.csv**: Details of hotels including property ID, name, category, and city.
3. **dim_rooms.csv**: Information about room types and their classifications.
4. **fact_aggregated_bookings.csv**: Aggregated booking data by property and room category.
5. **fact_bookings.csv**: Detailed booking data including booking dates, check-in/check-out dates, booking platforms, and revenue details.

## 🛠️ Features

- **Interactive Navigation**: Use the Navigation page to easily switch between different analytical sections of the dashboard.
- **Key Metrics Visualization**: Get insights into Total Revenue, Bookings, ADR, RevPAR, and other important metrics.
- **Channel and City Analysis**: Breakdown of revenue and bookings by channel and city.
- **Property and Room Performance**: Compare the performance of different properties and room categories.
- **Temporal Trends**: Analyze booking trends and profitability over time.

## 🔍 Pages

1. **Navigation**: Easy access to different parts of the dashboard.
2. **Overview**: High-level summary of key metrics.
3. **Channel and City Level Analysis**: Performance analysis by booking channel and city.
4. **Property and Room Category Performance**: Detailed performance insights by property and room category.
5. **Temporal Analysis and Profitability**: Time-based analysis and profitability metrics.

## 🧑‍💻 How to Use

1. **Clone the repository**:
    ```bash
    git clone (git_repository_link)
    ```

2. **Open Power BI Desktop** and load the `.pbix` file from the cloned repository.

3. **Explore the Dashboard**:
   - Use the Navigation page to move between different analysis sections.
   - Hover over charts to see detailed insights and use slicers to filter data.

## 📈 Key Calculations

- **MoM Booking Growth**: `MOM_booking = ([MTD_booking]-[PMTD_booking])/[PMTD_booking]`
- **WoW Revenue Growth**: `WoW_Revenue_Growth = ([Total_Revenue_Current_Week] - [Total_Revenue_Previous_Week]) / [Total_Revenue_Previous_Week] * 100`
- **Total Revenue Percentage by City**:
    ```DAX
    Total_Revenue_Percentage_By_City = 
    DIVIDE(
        [Total_Revenue_By_City],
        CALCULATE([Total_Revenue], ALL(dim_hotels[city]))
    ) * 100
    ```

## 🚀 Deployment

You can share this dashboard within your organization by publishing it to Power BI Service, allowing others to access it via a web link or embed it into your website.

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 📬 Contact

For any questions or feedback, please reach out:

- **Email**: your.email@example.com
- **LinkedIn**: [Mayank Gupta](https://www.linkedin.com/in/mayankgupta18/)
- **GitHub**: [@mayankgupta](https://github.com/Mayankgupta1803)

---

### 📎 Additional Notes

- Consider adding a section for **Future Enhancements** if you plan to expand the dashboard.
- Include screenshots or a video demo in the README to make it more engaging.
