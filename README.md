

# HVAC Sensor Data Analysis

**By Nandha Kumar S**
**2nd Year, Mechanical Engineering**
**ARM College of Engineering & Technology**
**Course: Data Analysis in Mechanical Engineering**

---

## Introduction

This project is part of my coursework on data analysis and focuses on studying data collected from HVAC (Heating, Ventilation, and Air Conditioning) systems. The main goal is to examine how environmental and system parameters such as temperature, humidity, air flow, CO2 concentration, number of people in the room, and energy usage change over time and relate to each other.

The insights from this project can help in improving how HVAC systems are used, especially in terms of energy savings and maintaining comfortable indoor environments.

---

## Objectives

Through this analysis, I aim to:

* Discover patterns in HVAC operation over time.
* Spot situations that may be causing high energy use.
* Help inform better decisions for building maintenance and automation.

---

## About the Dataset

The dataset contains time-based measurements of different factors linked to HVAC operation. Below is a summary of the features:

| Feature Name              | Description                           |
| ------------------------- | ------------------------------------- |
| Date\_Logged              | Time when the data was recorded       |
| Temperature (C)           | Indoor temperature in degrees Celsius |
| Humidity (%)              | Indoor relative humidity              |
| Air\_Flow (CFM)           | Airflow in cubic feet per minute      |
| CO2\_Level (ppm)          | CO2 concentration inside the room     |
| Occupancy                 | Number of people present              |
| Energy\_Consumption (kWh) | Energy used by the HVAC system        |

---

## Data Preprocessing

To prepare the data for analysis, I followed these basic steps:

1. **Data Loading**
   Used Pandas to load and take a first look at the dataset.

2. **Datetime Conversion**
   Converted the `Date_Logged` column to datetime format for easier time-based analysis.

3. **Handling Missing Data**
   Filled in missing values using the average of each respective column, especially in `CO2_Level` and `Air_Flow`.

4. **Feature Creation**
   Added two new features from the datetime column:

   * **Hour**: Hour of the day.
   * **DayOfWeek**: Day of the week (0 = Monday, 6 = Sunday).

---

## Data Analysis

I performed several types of analysis to understand the relationships between different variables:

### Time Trends

* Energy usage clearly rises during working hours.
* CO2 levels and temperature often change with the number of people in the room.

### Correlation

* Energy usage is somewhat related to indoor temperature and airflow.
* Occupancy is strongly linked to CO2 levels.

### Data Distribution

* Some features, like energy use and airflow, show uneven distributions.
* Boxplots and histograms helped identify unusual values (possible outliers).

---

## Findings

Here are some of the main things I learned from the data:

* **More people ? higher CO2 levels**, which is expected in enclosed spaces.
* **Airflow increases when more people are present**, showing that the HVAC system adjusts automatically.
* **Energy use peaks during work hours**, especially from 9 AM to 6 PM on weekdays.
* **Temperature and humidity remain stable**, suggesting the HVAC system is functioning well in maintaining comfort.

---

## What�s Next

To take this project further, I plan to:

* Detect and remove outliers more accurately using methods like the IQR technique.
* Try basic predictive models for estimating future energy use or identifying when the system might be working unusually.

---

## Tools and Technologies

* **Python** with **Pandas** and **NumPy** for data cleaning and analysis
* **Matplotlib** and **Plotly** for charts and graphs
* **Jupyter Notebook** to build and document the entire project
