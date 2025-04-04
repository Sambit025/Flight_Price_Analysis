
# ✈️ Flight Price Data — Feature Engineering Project

## 📊 Overview
This project explores and performs feature engineering on a **flight price dataset** to prepare it for potential modeling or analytical use. The primary objective is to clean, preprocess, and transform raw flight booking data into a structured format that captures relevant travel and pricing insights.

## 📁 Data Source
The dataset used is `flight_price.xlsx`, which contains flight booking details such as:
- Journey Date  
- Airline  
- Source & Destination cities  
- Departure and Arrival times  
- Duration  
- Total Stops  
- Additional Info  
- Price

## 🛠️ Feature Engineering Performed
Here’s what was done to clean and enhance the dataset:

### ✅ Datetime Feature Extraction
- Extracted **Day**, **Month**, and **Year** from `Date_of_Journey`
- Converted `Dep_Time` and `Arrival_Time` into **hour** and **minute** features

### ✅ Duration Handling
- Parsed the `Duration` string into two separate numerical columns: `Duration_hr` and `Duration_min`

### ✅ Categorical Encoding
- Mapped `Total_Stops` into numerical format (e.g., non-stop → 0, 1 stop → 1, etc.)
- Replaced missing values in categorical features with placeholder values (`'unknown'`, `'No Info'`)
- Used `OneHotEncoder` to convert text-based categorical columns like:
  - `Airline`
  - `Source`
  - `Destination`
  - `Additional_Info`

### ✅ Data Cleaning
- Dropped redundant or unneeded columns like `Route`, `Date_of_Journey`, `Dep_Time`, `Arrival_Time`, and `Duration`
- Filled missing values appropriately for categorical and numeric features

## 📦 Tools & Libraries Used
- `pandas`, `numpy` for data manipulation  
- `scikit-learn`'s `OneHotEncoder` for categorical feature encoding

## 🚀 How to Use
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/flight-price-feature-engineering.git
   ```
2. Run the Jupyter Notebook:
   - Make sure to place `flight_price.xlsx` in the same directory
   - Execute the cells to perform feature engineering

## 📌 Future Work
- Apply regression models to predict flight prices
- Visualize pricing trends across different airlines or times of year
- Perform hyperparameter tuning and model evaluation
