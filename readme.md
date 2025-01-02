# Project – K-Means Clustering

## Introduction
The aim of this workshop is to perform clustering using the K-Means Algorithm and visualize the results on a map. The dataset used for this workshop contains COVID-19 statistics. The objective is to determine whether the K-Means algorithm is a suitable choice for this task by comparing the accuracy of the results with real-world news reports.

## Data Preparation
The dataset was prepared by selecting data from **1st February 2022 to 31st March 2022**. The downloaded files contain information such as confirmed cases, deaths, and incidence rates from different countries and regions at various timeslots. 

## Data Points
A new dataset was created focusing on the total number of confirmed COVID-19 cases and deaths. This data was stored in the file `MameFasseSALL-2441202_4.csv`. The key data points include:
- **Confirmed Cases**: Calculated as the difference between values on two dates.
- **Deaths**: Calculated as the difference between values on two dates.

These data points were chosen because they provide a clear understanding of how COVID-19 progressed over time.

## Data Processing
Preprocessing steps were performed to ensure accurate and reliable results:
1. **Renaming Columns**: Column names were standardized to ensure consistency across different files.
2. **Geolocation Verification**: Longitude and latitude of regions were retrieved and cross-checked with the provided data.

## Data Transformation
The data was transformed to ensure uniformity:
- **Standard Scaling**: The `StandardScaler` function was used to bring all features to the same scale, which is essential for distance-based algorithms like K-Means.
- **Outlier Removal**: Outliers were removed to improve the quality of clustering.

## K-Means Algorithm
The K-Means algorithm was chosen for this workshop because:
- It performs well with large datasets.
- It creates clusters of approximately equal size.
- It minimizes within-cluster variations, making it suitable for identifying regions with similar COVID-19 trends.

### Model Parameters
- **Number of Clusters**: 4 (selected using the elbow method).
- **Random State**: 10 (ensures reproducible results).


## Results and Discussion
The analysis resulted in **4 clusters**, with most values lying in the first cluster. The clusters were mapped geographically, and the results were coherent:
- Regions within the same cluster were geographically close and shared similar COVID-19 trends.
- The characteristics of each cluster aligned with expected COVID-19 progression patterns.

To validate the results, real-world news articles were reviewed, and the trends reported in the news matched the clustering results.

## Conclusion
The K-Means clustering algorithm provided valuable insights into regional COVID-19 trends. The clusters were geographically coherent and supported by real-world evidence. Key steps such as geolocation verification and data standardization were crucial for achieving accurate results. While there is room for improvement, the findings are robust and align with external sources, demonstrating the effectiveness of the K-Means algorithm for this analysis.

---

### Repository Structure
- `MameFasseSALL-2441202_4.csv`: Dataset containing COVID-19 confirmed cases and deaths.
- `kmeans_clustering.ipynb`: Jupyter Notebook containing the code for data processing, clustering, and visualization.
- `README.md`: This file.

### Requirements
- Python 3.x
- Libraries: Pandas, NumPy, Scikit-learn, Matplotlib, Geopy

### How to Run
1. Clone the repository.
2. Install the required libraries using `pip install -r requirements.txt`.
3. Open the Jupyter Notebook `kmeans_clustering.ipynb` and run the cells to perform clustering and visualize the results.

---

**Note**: Ensure you have the necessary dataset and dependencies installed before running the code.