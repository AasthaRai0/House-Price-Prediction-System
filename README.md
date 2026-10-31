# House Price Prediction using Machine Learning

This project implements an end-to-end Machine Learning pipeline to predict house prices using the California Housing dataset [00:05:26]. It covers data acquisition, exploratory data analysis (EDA), advanced feature engineering via reverse geocoding, missing value imputation using classification models, and training a Random Forest Regressor [00:43:09].

---

## 📌 Project Workflow

1. **Data Collection**: Fetching the dataset directly from `sklearn.datasets` (`fetch_california_housing`) [00:05:26].
2. **Exploratory Data Analysis (EDA)**: Utilizing automated reporting tools (such as Sweetviz) to inspect data distributions, descriptive statistics, and feature correlations [00:11:35].
3. **Feature Engineering**: Extracting geographical metadata (such as **County** and **Road**) from raw latitude and longitude coordinates using `geopy` [00:15:37].
4. **Data Preprocessing & Imputation**: Handling missing categorical values by training a stochastic gradient descent classifier to predict missing records instead of dropping them [00:31:02]. Label encoding is then applied to convert string categories into numeric features [00:40:22].
5. **Model Training**: Splitting the processed dataset into training and testing sets to train a **Random Forest Regressor** for continuous house price prediction [00:44:47].
6. **Evaluation**: Measuring model performance and predictive accuracy using the $R^2$ (R-squared) score [00:46:55].

---

## 🛠️ Tech Stack & Libraries

* **Python**
* **Pandas & NumPy** (Data manipulation, matrix operations, and array handling) [00:06:06]
* **Scikit-Learn (`sklearn`)** (Machine learning algorithms, preprocessing utilities, and metrics) [00:06:16]
* **Geopy** (Reverse geocoding latitude/longitude coordinates into real-world addresses) [00:15:32]
* **Pickle** (Saving incremental feature engineering loops to persistent storage to prevent data loss during API timeouts) [00:24:33]
* **Matplotlib** (Data visualization) [00:06:07]

---

## 🚀 Getting Started & Running the Code

### 1. Installation
Clone or open your project in an environment like Jupyter Notebook or Google Colab [00:03:41], then install the required dependencies:
```bash
pip install pandas numpy scikit-learn geopy sweetviz matplotlib