# Getting Started with Snowflake Cortex ML-Based Functions for Wanderlust Voyages

## Overview

For "Wanderlust Voyages," a premier travel company, leveraging data insights is key to staying competitive and enhancing customer experiences. Data/Business Analysts play a crucial role in producing recommendations based on these insights. This often involves building models to: make forecasts for travel demand, identify long-running trends in travel preferences, and detect abnormalities in booking patterns or operational data. However, the statistical and machine learning knowledge required can be a hurdle.

Snowflake Cortex ML-Based Functions provide a SQL-friendly approach to implement these models. As of your current Snowflake version, functions for time-series based data include:

1.  **Forecasting**: Predict future metrics like passenger numbers for specific destinations or package types. This helps Wanderlust Voyages in resource planning, staffing, and inventory management for travel packages.
2.  **Anomaly Detection**: Identify unusual data points, such as unexpected spikes or drops in bookings for a particular region, which could indicate emerging trends, operational issues, or the impact of external factors.
3.  **Contribution Explorer**: (Not the focus of this lab, but useful for) determining the most significant drivers for metrics like booking value or customer satisfaction.

This lab will also demonstrate how Wanderlust Voyages can use **Sentiment Analysis** and **Text Classification** to understand customer feedback and the nature of external events, enriching the forecasting and anomaly detection processes.

For further details on ML Functions, please refer to the [snowflake documentation](https://docs.snowflake.com/guides-overview-analysis).

### Prerequisites
* Working knowledge of SQL
* A Snowflake account login with appropriate roles to create databases, schemas, tables, stages, tasks, and use Cortex functions.

### What You’ll Learn
* How to use Anomaly Detection & Forecasting ML Functions to create models and predict passenger numbers for Wanderlust Voyages.
* How to perform Sentiment Analysis on customer feedback and external event descriptions using `SNOWFLAKE.CORTEX.SENTIMENT`.
* How to classify customer feedback using `SNOWFLAKE.CORTEX.CLASSIFY_TEXT`.
* How to incorporate external event data (with sentiment) into forecasting models.
* How to use Tasks to retrain models on a regular cadence.
* How to use email notification integration to send reports.

### What You’ll Build
This Quickstart will guide you through using Forecasting and Anomaly Detection ML Functions within the context of "Wanderlust Voyages."
We will:
* Create a forecasting model to predict the number of passengers for specific travel offerings, aiding in operational planning.
* Analyze customer feedback to understand sentiment and categorize comments, helping Wanderlust Voyages identify areas for service improvement.
* Analyze external events and their sentiment to understand their potential impact on travel.
* Build an anomaly detection model to identify unusual patterns in passenger numbers for different travel packages/destinations, which can highlight trending offers or issues needing attention.
* **(Optional)** Scale the forecasting model to multiple travel offerings and incorporate sentiment-analyzed external event data to potentially improve forecast accuracy.
* **(Optional)** Showcase how to schedule model retraining and reporting using Tasks and email notifications.

By the end of this lab, you'll have practical experience applying these functions to solve real-world travel analytics problems, empowering you to bring ML insights into your daily work.

Let's get started!


### Resources:
For further details on the functions used:
* [Snowflake Cortex ML Functions Overview](https://docs.snowflake.com/en/user-guide/snowflake-cortex/ml-functions)
* [SNOWFLAKE.ML.FORECAST](https://docs.snowflake.com/en/user-guide/ml-powered-forecasting)
* [SNOWFLAKE.ML.ANOMALY_DETECTION](https://docs.snowflake.com/en/user-guide/ml-powered-anomaly-detection)
* [SNOWFLAKE.CORTEX.SENTIMENT](https://docs.snowflake.com/en/sql-reference/functions/sentiment)
* [SNOWFLAKE.CORTEX.CLASSIFY_TEXT](https://docs.snowflake.com/en/sql-reference/functions/classify)
* [Tasks](https://docs.snowflake.com/en/user-guide/tasks-intro)
* [Stored Procedures](https://docs.snowflake.com/en/developer-guide/stored-procedure/stored-procedures-overview)
