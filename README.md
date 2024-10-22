# Swiggy Delivery Time Prediction and Churn Analysis!

This project is a comprehensive analysis of Swiggy delivery data, aimed at identifying factors that contribute to slower delivery times and predicting customer churn using machine learning techniques. By leveraging Python libraries such as `pandas`, `scikit-learn`, and `matplotlib`, the analysis not only provides insights into customer behaviors but also predicts churn rates based on delivery performance.

## Project Overview

- **Dataset**: The dataset contains information about Swiggy deliveries, including delivery time, area, city, restaurant details, food types, ratings, and more.
- **Objective**: The primary goal is to build a churn prediction model to determine whether a restaurant will experience a churn (due to slow delivery) based on features such as city and area.

## Key Features

1. **Data Preprocessing**:
    - Load and clean the Swiggy dataset.
    - Encode categorical variables such as city and area using `LabelEncoder`.
    - Define a new target variable (`churn2`), which is based on delivery times greater than 30 minutes.

2. **Churn Prediction Model**:
    - Used a `RandomForestClassifier` to build a churn prediction model based on the encoded city and area variables.
    - Split the dataset into training and testing sets using `train_test_split`.
    - Achieved an accuracy of **96.54%** in predicting slow delivery churn.

3. **City and Area Selector**:
    - Dynamically list available cities and areas, allowing users to select their city and area of interest.
    - Predicts churn for the selected city and area.

4. **User Interaction**:
    - Asks for user input (city and area) and provides churn prediction based on the selected location.

## Tools & Technologies

- **Programming Language**: Python
- **Libraries**:
  - `pandas`: For data manipulation and preprocessing.
  - `numpy`: For numerical operations.
  - `matplotlib` and `seaborn`: For data visualization.
  - `scikit-learn`: For building machine learning models (Random Forest) and encoding categorical data.

## Installation & Usage

1. Clone the repository and navigate to the project directory.
   ```bash
   git clone <repo-link>
   cd swiggy-churn-analysis

2. Ensure the dataset `swiggy.csv` is present in the same directory.

3. Run the Python script to perform churn prediction and interact with the city and area selector.
   ```bash
   python swiggy_churn.py
   ```

4. Enter the city and area details as prompted, and the system will predict whether a customer churn is likely due to slow delivery.

## Example Output
```
Enter the city: Hyderabad
Enter the area: L.B Nagar
In Hyderabad (L.B Nagar), Slow delivery Churn prediction: 1
```

## Accuracy

- The `RandomForestClassifier` achieved an accuracy of **96.54%**, making it a robust model for predicting churn based on delivery time and location.

## Conclusion

This project provides insights into delivery performance and customer churn using real-world data from Swiggy. The interactive city and area selection feature, combined with machine learning predictions, makes it an engaging tool for exploring the delivery dynamics of food services in various cities.

