# 🏠 Morocco Real Estate Price Prediction

This project focuses on building a machine learning pipeline to predict property prices across various Moroccan cities (Casablanca, Marrakech, Tangier, etc.) based on features like surface area, location, and amenities.

## 📊 Project Overview
The goal was to analyze a dataset of property listings and develop a regression model capable of estimating market values with high precision.

### Key Features Used:
* **Location:** City and Neighborhood (`Nighberd`)
* **Property Details:** Surface area ($m^2$), number of bedrooms (`chambres`), and bathrooms (`salles de bains`)
* **Amenities:** Presence of an elevator (`ascenseur`), terrace, and parking
* **Floor Level:** The floor number of the property

---

## 📈 Exploratory Data Analysis (EDA) Highlights
Before modeling, I performed extensive EDA to understand price drivers:
* **City Impact:** Casablanca and Marrakech represent the cities with the highest volume of listings, with average prices ranging between 500K and 3.5M DH.
* **Size Correlation:** There is a strong linear correlation between `Surface Area` and `Price`, although luxury outliers exist in cities like Marrakech.
* **Room Distribution:** Most properties in the dataset feature 1 to 2 bedrooms, with a significant drop-off for larger properties.

---

## ⚙️ Machine Learning Pipeline

### 1. Data Preprocessing
* **Categorical Encoding:** Converted `City` and `Type` into numerical values using One-Hot Encoding.
* **Binary Mapping:** Converted 'Yes/No' features (elevator, parking) into 1s and 0s.
* **Feature Scaling:** Applied `StandardScaler` to normalize numerical ranges for the Linear Regression model.

### 2. Models Evaluated
I compared multiple algorithms to find the best fit:
* **Linear Regression:** Served as a baseline model.
* **Gradient Boosting Regressor:** Effective at capturing non-linear relationships.

### 3. Performance
The models were evaluated using **R² Score** and **Mean Absolute Error (MAE)**. Both models showed high performance, indicating strong feature-to-target correlation.

---

## 🛠️ Installation & Usage
1. Clone the repo: `git clone https://github.com/Badr-Eddine-Elfaji/morocco-real-estate-prediction.git`
2. Install dependencies: `pip install pandas matplotlib seaborn scikit-learn`
3. Run the notebook: `jupyter notebook notebooks/Price_Prediction.ipynb`
