# Web Traffic & Engagement Analytics
This project focuses on analyzing and forecasting web traffic, user engagement, and channel performance using historical web traffic data. The analysis provides insights into traffic trends, user behavior, and the effectiveness of various channels, ultimately enabling better decision-making for optimizing website performance.

## Project Overview:
The objective of this project is to analyze web traffic data, extract key insights, and forecast future traffic patterns using statistical techniques. This analysis can assist website administrators, marketers, and analysts in understanding user behavior and improving engagement strategies.

## Dataset Overview:
The [dataset](https://statso.io/website-performance-case-study/) we are working on is an open dataset sourced from [statso.io](statso.io). It contains the following columns:
- Session primary channel group: The marketing channel (e.g., Direct, Organic Social)
- Date + hour (YYYYMMDDHH): The specific date and hour of the session
- Users: Number of users in a given time period
- Sessions: Number of sessions in that period
- Engaged sessions: Number of sessions with significant user engagement
- Average engagement time per session: The average time a user is engaged per session
- Engaged sessions per user: Ratio of engaged sessions to total sessions per user
- Events per session: Average number of events (actions taken) per session
- Engagement rate: The proportion of sessions that were engaged
- Event count: Total number of events during the period

## Features:
1. Data Loading and Cleaning:
    - Loads and cleans web traffic data from a CSV file.
    - The first row is set as column headers, and any rows with invalid datetime entries are removed.
    - Converts numeric columns to their correct data types (e.g., "Users," "Sessions").
2. Time Series Analysis:
    - Aggregates user and session data by date and hour, enabling a time-based overview of website traffic.
    - Provides visualizations of user and session trends over time.
3. Engagement Metrics Analysis:
    - Analyzes key engagement metrics such as:
      - Average Engagement Time per Session
      - Engaged Sessions per User
      - Events per Session
      - Engagement Rate
    - These metrics provide insights into user interactions, session quality, and overall engagement with the website.
4. Correlation Analysis:
    - Identifies relationships between engagement metrics, helping to uncover patterns and dependencies (e.g., "Average Engagement Time vs. Events per Session").
    - Pearson correlation coefficients and scatter plots visualize these relationships.
5. Channel Performance Analysis:
    - Aggregates traffic and engagement data by marketing channel (e.g., organic search, paid search).
    - Compares performance across channels using normalized metrics, such as engagement rate and events per session.
6. Traffic Forecasting (SARIMA Model):
    - Forecasts website traffic (sessions) for the next 24 hours using the SARIMA (Seasonal AutoRegressive Integrated Moving Average) model.
    - Provides a prediction of future traffic trends, enabling proactive website performance management.
  
## Key Findings:
1. Traffic Trends:
   - Web traffic (users and sessions) fluctuates significantly over time, with noticeable peaks and valleys. These fluctuations could indicate periods of high user interest or marketing campaigns.
2. Engagement Insights:
   - Engagement metrics, such as Average Engagement Time per Session and Engaged Sessions per User, show that certain hours of the day (e.g., evenings) have higher engagement, suggesting peak user activity.
   - The Engagement Rate appears to correlate positively with Events per Session, indicating that more interactive sessions result in higher engagement.
3. Channel Performance:
   - Analysis of channel performance reveals that certain channels (e.g., organic search) tend to bring in more users and sessions, but channels like paid search or social media have higher engagement rates and events per session.
    - Normalized metrics indicate which channels are the most efficient in terms of user engagement.
4. Forecasting Insights:
   - The SARIMA model effectively predicts traffic trends, with the forecast showing expected session counts for the next 24 hours. This can help plan for server load, marketing activities, or content updates during peak periods.

## Requirements:
- pandas: For data manipulation and analysis.
- matplotlib: For generating visualizations.
- statsmodels: For time series analysis and SARIMA model.
- seaborn: For advanced plotting and visualization.
- scipy: For statistical operations such as correlation analysis.
- pmdarima: For building the SARIMA model.
