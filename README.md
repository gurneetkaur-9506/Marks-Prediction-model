Learning Project
Student Marks Prediction
This project explores a simple end-to-end machine learning workflow for forecasting Portuguese secondary-school students' final exam marks (G3). It uses the classic Student Performance dataset and walks through cleaning, encoding, training, and evaluating a linear regression model inside the marks_prediction.ipynb notebook.

Dataset
Source: Adapted from the UCI Student Performance dataset (Portuguese language course).
File: student_data.csv
Target: G3 (final grade, 0-20 scale).
Core predictors used for the baseline model:
Study habits: studytime, failures, absences
Lifestyle indicators: Dalc (weekday alcohol), Walc (weekend alcohol)
Prior performance: G1, G2
Additional categorical columns (e.g., sex, address, Mjob, guardian) are encoded via label or one-hot encoding to make them model-friendly.
Requirements
Install Python 3.10+ along with the notebook dependencies:

pip install pandas numpy scikit-learn matplotlib seaborn
Project Structure
marks_prediction.ipynb: Full workflow (EDA, preprocessing, modeling, visualization).
student_data.csv: Raw dataset.
README.md: Project overview and instructions (this file).
Workflow Highlights
Load & Inspect: Preview the dataset, schema, and descriptive statistics.
Data Cleaning: Drop nulls/duplicates and remove unrealistic studytime outliers.
Feature Engineering: Map binary categories (e.g., sex, address) and one-hot encode multi-class fields (Mjob, Fjob, guardian).
Train/Test Split: Use train_test_split with an 80/20 split and fixed seed (random_state=42).
Modeling: Fit a LinearRegression model using the selected numerical predictors.
Evaluation: Report Mean Squared Error (MSE) and 
R
2
 to gauge accuracy.
Visualization: Plot actual vs. predicted marks to visually inspect fit quality.
Running the Notebook
Launch VS Code or Jupyter Lab and open marks_prediction.ipynb.
Ensure the kernel has the required packages (see Requirements).
Execute cells sequentially. Intermediate prints confirm each preprocessing step.
Review the final MSE/$R^2$ output and inspect the line chart comparing actual vs. predicted marks.
Extending the Project
Experiment with additional regressors (e.g., Random Forest, Gradient Boosting) or add regularization.
Perform feature importance analysis or SHAP explanations to interpret predictions.
Add k-fold cross-validation and hyperparameter tuning to improve generalization.
Package the workflow into a script or REST API for easier deployment.
Notes
The dataset includes sensitive student attributes; ensure responsible use if sharing results.
If you alter preprocessing (e.g., keeping more categorical variables), rerun the full notebook to refresh the trained model and plots.
