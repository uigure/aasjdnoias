# SC4002 Data Analytics & Mining 

## A Python implementation of the Generalized Sequential Patterns (GSP) algorithm for sequential pattern mining

This project implements the Generalized Sequential Patterns (GSP) algorithm to find frequent sequences within a given
dataset. The dataset comprises human mobility data from four metropolitan areas in Japan, anonymized to ensure individual privacy. 
This data includes spatial and temporal information for human activities over 75 days at a resolution of 500-meter grid cells.

## Contributors:
- Lim Kian Yew
- Bryan Chia Song Nian
- Shawn Yap Zheng Yi
- Wong Wei Kai
---

## Requirements

Libraries used:
```
- pandas
- numpy
- apriori
- trackintel
- matplotlib
- seaborn
- scikit-learn
- keras
- tensorflow
- other libraries as needed
```

### Data Integrity:
- Datasets B, C, and D are missing data for the last 15 days (from day 61 to 75), marked with coordinates as `-999`.

## Task Description

### Task 2.1: Analysis of Co-occurrence Patterns of Points of Interest (POI)
#### Objective:
- [Add the objective here]

#### Method:
- [Add the method here]

#### Approach:
- [Describe the approach here]

### Task 2.2: Mining Sequential Patterns
#### Objective:
- [Add the objective here]

#### Steps:
1. **Data Preprocessing**: [Describe the data preprocessing steps here]
2. **Data Analysis**: [Describe the data analysis steps here]

#### Approach:
- [Describe the approach here]

### Task 3: Advanced Tasks (Optional)
#### Objective:
Define an application based on the provided datasets, identifying locations with significant fluctuations in visit frequency throughout the week. This will provide insights into dynamic usage patterns, which can help with resource allocation, urban planning, and business strategies.

#### Methodology:
This task involves analyzing the variability in visit frequencies for locations over a week, with the goal of identifying locations and clusters with significant weekly fluctuations. The analysis is based on visit frequency data aggregated over the week, highlighting areas with high variability driven by events, peak hours, or weekend activities.

##### Steps:

1. **Dataset Loading**:
   The dataset is loaded from a pre-processed JSON file generated in Task 2, which contains the visit frequency data for each location across multiple cities.

2. **Analysis of Weekly Visit Trends**:
   - **Aggregation by Day**: Compute the total visit frequency for each day of the week across all locations.
     - Visualize this with a **bar plot** to show the total visits per day, identifying patterns such as peaks during weekdays and weekends.
     
   - **Standard Deviation Calculation**: For each location, calculate the standard deviation in visit frequency to measure variability.
     - Select the top 15 locations with the highest standard deviation to highlight areas with the most significant fluctuations.

3. **Clustering Analysis with K-Means**:
   - Perform **K-Means clustering** on the locations based on their spatial coordinates (latitude and longitude). The number of clusters is set to `k=50`, but this can be adjusted for finer granularity or based on predefined cluster centers indicating areas of interest.
   - Select the **top 5 clusters** that exhibit the highest variability in visit frequency based on their standard deviation.
   - **Visualize** the clusters on a **cluster map** and create a **line plot** for each cluster to show the variability in visit frequency across the days of the week.

#### Visualization:
The methodology helps identify locations with high weekly fluctuations and visualizes these patterns effectively through plots and maps.
