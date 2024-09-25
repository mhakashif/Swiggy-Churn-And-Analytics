# Swiggy-Churn
Overview
This project focuses on predicting customer churn using historical data on city, area, customer ratings, and delivery times. We define two types of churn:

Churn1: Determined by whether a customer gives a low total rating (certain threshold).
Churn2: Determined by whether a customer experiences slow delivery (set time threshold).
The goal is to provide a machine learning model that predicts the likelihood of customer churn based on these factors. The model allows users to input a city and area and receive predictions about potential churn in that location.

Problem Statement
Many businesses struggle to retain customers, especially when they receive poor service. In this project, we use a dataset with columns like:

City: Where the service was provided.
Area: The specific area within the city.
Total Ratings: The customer’s overall rating of the service.
Delivery Time: The time it took for the service or product to be delivered.
Based on these inputs, we aim to predict two types of churn:

Churn1: If the customer is likely to churn based on low ratings.
Churn2: If the customer is likely to churn due to long delivery times.

Project Steps
1. Data Preparation
We create two target columns:

Churn1: Customers with total ratings below a threshold (e.g., less than 3) are considered likely to churn.
Churn2: Customers who experienced delivery times above a threshold (e.g., more than 30 minutes) are considered likely to churn.
We also encode categorical variables like City and Area using Label Encoding to convert them into numerical formats suitable for machine learning models.

2. Model Training
We train two separate Random Forest Classifiers for predicting churn:

Model for Churn1: Predicts if a customer is likely to churn based on low ratings.
Model for Churn2: Predicts if a customer is likely to churn based on slow delivery times.
The dataset is split into training and testing sets (80% training, 20% testing) to ensure the model is not overfitted and generalizes well on unseen data.

3. Model Evaluation
After training, we evaluate the performance of both models using accuracy scores. The accuracy score tells us how well the models predict churn on the test dataset.

4. User Input Prediction
The model allows users to input a city and area to predict the likelihood of churn in that location. We handle cases where the city or area is not present in the training data by providing a default value and warning.

Installation and Usage
Prerequisites
Before running the code, make sure you have the following libraries installed:

pandas
sklearn (scikit-learn)
You can install the required packages using the following command:

bash
Copy code
pip install pandas scikit-learn
Running the Code
Prepare the Dataset: Load the dataset into the df DataFrame. The dataset should contain the following columns:

City
Area
Total Ratings
Delivery Time
Run the Model:

The model will automatically process the data, train itself, and output the accuracy of both churn predictions.
Predict Churn for a New City/Area:

The code allows users to enter a city and area for which the model will predict Churn1 and Churn2.
Example Output
If you input a city and area that exists in the dataset:

Copy code
Enter the city: 
Enter the area:
In city, Churn1 prediction: 1, Churn2 prediction: 0
Results Explanation:
Churn1 prediction: Indicates if customers in this area are likely to churn due to low ratings (1 for churn, 0 for no churn).
Churn2 prediction: Indicates if customers in this area are likely to churn due to slow delivery (1 for churn, 0 for no churn).
Code Structure
Here is a summary of the key files:
The main Python script that contains the churn prediction logic.
README.md: This explanation document.
Model Accuracy
The model uses accuracy scores to evaluate its performance:

Accuracy for Churn1: The percentage of correct predictions for churn based on ratings.
Accuracy for Churn2: The percentage of correct predictions for churn based on delivery times.
These accuracy scores provide a measure of the model’s performance on unseen test data, ensuring the model is reliable for future predictions.

Future Improvements
To further improve the model’s performance and extend its usage:

Feature Engineering: Add more features (e.g., order size, customer type) that could influence churn.
Model Optimization: Perform hyperparameter tuning on the Random Forest models to achieve better accuracy.
Handle New Data: Implement better handling of unseen cities or areas that are not present in the training data.
Model Persistence: Save the trained models using joblib or pickle so that they can be reused without retraining.
Conclusion
This project successfully provides a framework for predicting customer churn based on ratings and delivery time. It enables businesses to target areas with high churn risk, allowing them to take corrective actions to improve customer retention.
