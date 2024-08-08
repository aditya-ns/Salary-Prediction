# Salary Prediction

## Introduction
This project aims to predict job salaries based on various features such as job title, job category, company location, and more. By utilizing machine learning models like Linear Regression and Decision Tree Regressor, we can analyze and forecast salary trends in the data industry. This tool is designed to help both job seekers and employers understand salary expectations and make informed decisions.

## Objectives
The primary objective of this project is to develop a predictive model that accurately estimates job salaries based on various job-related features. By leveraging machine learning techniques, the project seeks to:

1. Analyze the impact of different job titles, categories, and locations on salary.
2. Identify key factors that influence salary variations within the data industry.
3. Provide a reliable tool for job seekers to gauge salary expectations based on their job profile and location.
4. Assist employers in understanding competitive salary benchmarks for different roles and regions.

Ultimately, the project aims to bridge the information gap in salary expectations, facilitating better career and hiring decisions.

## Methodology

The methodology for this project involves several key steps to build and evaluate the predictive model for job salaries:

1. **Data Collection**:
   - The dataset used in this project is sourced from `jobs_in_data.csv`, which contains job-related information including job title, job category, salary, company location, and more.

2. **Data Preprocessing**:
   - **Data Cleaning**: Handle missing values and outliers. Outliers in salary data are detected and removed based on the Interquartile Range (IQR) method.
   - **Feature Encoding**: Convert categorical features into numerical values using `LabelEncoder` to prepare the data for machine learning algorithms.
   - **Feature Selection**: Select relevant features for modeling, excluding columns not needed for prediction.

3. **Model Training**:
   - **Linear Regression**: A linear model is trained to predict salaries based on the provided features.
   - **Decision Tree Regressor**: A decision tree model is used to capture non-linear relationships and interactions between features and salary.

4. **Model Evaluation**:
   - **Performance Metrics**: Evaluate model performance using metrics such as Mean Squared Error (MSE), Root Mean Squared Error (RMSE), and Mean Absolute Error (MAE).
   - **Model Comparison**: Compare the performance of Linear Regression and Decision Tree Regressor to choose the best model for prediction.

5. **Model Deployment**:
   - **Model Saving**: Save the trained model and preprocessing steps using `pickle` for future use and easy deployment.

6. **Prediction**:
   - **Loading the Model**: Load the saved model and preprocessing objects to make predictions on new data.

## Results

The results of the project include the performance evaluation of the predictive models and their accuracy in estimating job salaries.

### Model Performance

1. **Linear Regression**:
   - **Root Mean Squared Error (RMSE)**: $50,896.92

   The Linear Regression model provides a baseline for salary prediction. While it captures linear relationships between features and salary, it may not account for complex interactions.

2. **Decision Tree Regressor**:
   - **Root Mean Squared Error (RMSE)**: $44,755.94

   The Decision Tree Regressor demonstrates improved performance over the Linear Regression model. It effectively captures non-linear relationships and interactions between features, resulting in a lower RMSE.

### Example Prediction

Using the Decision Tree Regressor, we can predict the salary for a job with the following attributes:

- **Job Title**: Data Engineering
- **Job Category**: Germany
- **Experience Level**: Mid-level
- **Employment Type**: Full-time
- **Company Location**: United States
- **Company Size**: M

The predicted salary for this job profile is approximately $80,000.

### Model Saving and Deployment

The trained Decision Tree Regressor model and preprocessing steps have been saved using `pickle`. This allows for easy loading and usage in future predictions.


## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
