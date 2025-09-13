# Medical-Insurance-Cost-Prediction

This project explores the Medical Insurance Dataset (1,338 records) to understand the factors influencing insurance costs and to build a predictive model. The dataset contains demographic and health-related features such as age, sex, BMI, children, smoking status, and region. The target variable is charges, representing the billed medical costs.

The aim of the project is to:

Explore how smoking, BMI, and age impact medical costs.
Build a regression model to predict charges.
Provide insights for health economics and insurance pricing.

🔹 Dataset Description

age: Age of primary beneficiary
sex: Gender (male/female)
bmi: Body Mass Index – measure of body fat
children: Number of dependents covered
smoker: Smoking status (yes/no)
region: Residential area in the US (northeast, northwest, southeast, southwest)
charges: Medical insurance cost billed (target variable)

🔹 Data Preprocessing

Label Encoding was used for binary categorical variables (sex, smoker).
One-Hot Encoding was applied to the region column.
All features were combined into the final dataset for model training.

🔹 Exploratory Data Analysis (EDA) & Visualizations

Impact of Smoking  : Boxplots showed that smokers incur significantly higher medical costs compared to non-smokers.
BMI vs Charges : Scatterplots revealed that higher BMI is associated with increased charges, especially for smokers.
Age vs Charges : Costs generally increase with age, with smokers showing a much steeper rise.
Regional Comparison : No major cost differences were observed across regions, suggesting region is less impactful.

🔹 Model Development
Model Used: Linear Regression
Train-Test Split: 80% training, 20% testing
Target Variable: charges
Input Features: age, bmi, children, sex_encoded, smoker_encoded, region (one-hot encoded)

📌 Model Output
Coefficients: Show how each feature impacts charges (e.g., smoking had the largest positive effect).
Intercept: Baseline charge prediction when all features are zero.

🔹 Model Evaluation
Metrics used:
MAE (Mean Absolute Error): Measures average prediction error in actual cost units.
RMSE (Root Mean Squared Error): Penalizes larger errors.
R² Score: Indicates how much of the variation in charges is explained by the model.

👉 The model performed reasonably well, but due to high variability in charges (especially for smokers), there is room for improvement.

🔹 Key Insights

Smoking is the strongest predictor of high insurance charges.
BMI and Age also significantly influence costs.
Children and Region play a relatively minor role.
Linear Regression provides interpretability, but more advanced models (like Random Forest or XGBoost) may improve accuracy.

🔹 Conclusion

This project demonstrates how demographic and lifestyle factors impact insurance costs and how machine learning can be applied to predict them. The analysis highlights the financial risk associated with smoking and the importance of maintaining a healthy BMI.
