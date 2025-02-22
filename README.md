# 
# Crime Dynamics: Integrating Textual, Spatial, and Temporal Perspectives

## Project Overview

This reserach project explores the analysis of crime dynamics in Los Angeles using machine learning, with a focus on classifying crime types, identifying crime hotspots, analyzing crime descriptions using text mining, and forecasting crime trends over time. By leveraging a combination of spatial, temporal, and textual data, this study provides insights that can aid in understanding crime patterns, improving public safety strategies, and forecasting crime occurrences.

![image](https://github.com/user-attachments/assets/cbaec49f-c80f-4af1-bb3e-62e29c646641)

### Project Objectives
1. **Crime Type Classification**: Predicting crime types based on attributes such as location, victim details, and weapon used using machine learning models.
2. **Hotspot Clustering**: Identifying and analyzing spatial patterns of crimes by detecting hotspots using clustering algorithms.
3. **Text-Based Topic Modeling**: Analyzing crime descriptions to extract common topics and patterns with LDA and clustering algorithms.
4. **Temporal Crime Forecasting**: Using LSTM networks to predict future crime occurrences based on historical data.

### Key Techniques Used:
- **Supervised Learning** (XGBoost, LightGBM, AdaBoost, etc.) for crime type classification.
- **Unsupervised Learning** (DBSCAN, HDBSCAN, OPTICS, KMeans) for clustering crime hotspots.
- **Topic Modeling** using LDA (Latent Dirichlet Allocation) for textual data.
- **Deep Learning** using LSTM (Long Short-Term Memory) for crime prediction.

## Dataset Overview

The dataset used in this project consists of crime reports from the Los Angeles Police Department (LAPD), covering the period from 2020 to January 2024. The dataset contains 19 columns and 180,000 rows after cleaning. The primary features include:

- **Crime Type**: Different crime categories (e.g., assault, robbery).
- **Victim Information**: Victim age, sex.
- **Crime Location**: Latitude, Longitude, Reporting District.
- **Crime Date**: Date and time of the occurrence.
- **Weapon Information**: Weapon used and weapon description.
- **Crime Descriptions**: Text data describing the nature of the crime.

The dataset is provided in CSV format and cleaned to remove irrelevant entries, standardize features, and handle missing data.

## Project Requirements

Ensure you have Python 3.x installed and the following dependencies:

```bash
pip install -r requirements.txt
```

### Required Libraries:
- **Pandas**: For data manipulation.
- **NumPy**: For numerical operations.
- **Scikit-learn**: For machine learning models.
- **XGBoost**, **LightGBM**, **CatBoost**: For boosting algorithms.
- **HDBSCAN**, **DBSCAN**, **KMeans**: For clustering algorithms.
- **Keras**: For building LSTM models.
- **Gensim**: For topic modeling with LDA.
- **Folium**: For visualizing spatial data on maps.

## Methodology

### 1. **Crime Type Classification**
- **Objective**: Classify the type of crime (e.g., assault, robbery) using features like victim's age, weapon used, crime location, etc.
- **Models Used**: XGBoost, LightGBM, AdaBoost, Naive Bayes, Random Forest, and other classifiers.
- **Evaluation Metrics**: Accuracy, F1-score, and confusion matrix.

### 2. **Hotspot Clustering**
- **Objective**: Identify geographical hotspots for crimes using clustering algorithms.
- **Methods Used**: DBSCAN, HDBSCAN, Mean Shift, and OPTICS were employed to identify dense areas of crime incidents in Los Angeles.
- **Spatial Features**: Latitude, Longitude, Reporting District.
- **Visualization**: Crime hotspots mapped using Folium to provide geographical insights.

### 3. **Text-Based Topic Modeling**
- **Objective**: Extract common topics from the textual descriptions of crimes.
- **Methods Used**: Latent Dirichlet Allocation (LDA) for topic extraction, followed by clustering using HDBSCAN and MiniBatchKMeans.
- **Features Used**: TF-IDF vectors were created from crime descriptions to represent textual data.
- **Results**: Key topics include domestic violence-related crimes (e.g., "partner assault"), robbery, and bodily harm.

### 4. **Temporal Crime Forecasting**
- **Objective**: Predict future crime occurrences using historical crime data.
- **Methods Used**: LSTM (Long Short-Term Memory) models were used to forecast the number of crimes per day.
- **Evaluation**: The model's performance was evaluated using loss metrics such as Mean Absolute Error (MAE) and Root Mean Squared Error (RMSE).

## Visualizations

### 1. **Choropleth Map of Crime Distribution**
A choropleth map visualizing the spatial distribution of crimes across Los Angeles. Areas with darker red shades represent regions with higher crime occurrences.

![image](https://github.com/user-attachments/assets/110d79a8-a766-42b0-9c01-c6f725cd73f1)

![image](https://github.com/user-attachments/assets/5f981cbb-bb43-4735-be14-cef678cba9e7)


### 2. **Word Cloud of Crime Descriptions**
A word cloud highlighting the most frequent terms found in crime descriptions, emphasizing patterns related to weapon usage and the nature of crimes (e.g., "assault," "robbery," "strong-arm").
![image](https://github.com/user-attachments/assets/10ce6698-00ca-4ea7-b939-0321d7e0eb22)

### 3. **Pie Chart of Crime Location Types**
A pie chart visualizing the proportion of crimes occurring in different location types, such as residential areas, commercial areas, and public spaces.
![image](https://github.com/user-attachments/assets/3b98807b-5724-4e84-a37e-f8daa2dd2eb2)

### 4. **Bar Chart of Crime Types** 
A bar chart showing the distribution of crime types, with "Battery Simple Assault" as the most frequent crime, followed by "Intimate Partner Simple Assault."
![image](https://github.com/user-attachments/assets/3d6bac23-9c7a-4303-b8f8-1603c439da8f)


## How to Run the Project

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/yourusername/crime-analysis.git
   cd crime-analysis
   ```

2. **Install Required Libraries**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the Analysis**:
   Execute the main script to perform the analysis:
   ```bash
   python main.py
   ```

   You can also run specific scripts for each part of the analysis:
   - Crime Type Classification: `python crime_classification.py`
   - Hotspot Clustering: `python hotspot_clustering.py`
   - Topic Modeling: `python topic_modeling.py`
   - Crime Prediction (LSTM): `python crime_forecasting.py`

4. **Output**:
   Results are saved in the `outputs/` directory, including trained models, evaluation metrics, and visualizations.

## Results

- **Crime Type Classification**:
  - The best-performing model for crime classification achieved **73% accuracy**. The XGBoost model showed strong performance across multiple crime types.
  - Example: "Battery Simple Assault" and "Intimate Partner Simple Assault" were successfully predicted with high precision.

- **Hotspot Clustering**:
  - Clustering revealed high-crime areas in Los Angeles, with notable hotspots in urban centers and residential districts.
  - **Key Insights**: Certain neighborhoods, especially those with high population density, showed significant crime activity.

- **Topic Modeling**:
  - The most common crime-related topics extracted included **domestic violence** and **assault-related crimes**.
  - The word cloud revealed terms like "robbery," "assault," and "partner crimes," underlining the significance of domestic violence in the dataset.

- **Crime Forecasting**:
  - The LSTM model accurately predicted crime trends, with future crime occurrences showing seasonality and notable peaks during specific months.

## Contributing

If you want to contribute to the project, feel free to fork the repository and submit pull requests. Any improvements, fixes, or new ideas are welcome!

### Issues and Bug Reports
If you encounter any issues or bugs while running the project, please open an issue on the GitHub repository.

## License

This project is licensed under the MIT License.
