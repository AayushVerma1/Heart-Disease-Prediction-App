# Heart-Disease-Prediction-Model using Machine Learning

This repository contains a machine learning project focused on predicting the risk of cardiovascular disease (CVD) in patients based on clinical data. The project implements and compares several classification models to identify the most accurate and reliable approach for early risk stratification.

<h2>Project Overview </h2> <br>
Cardiovascular disease is a leading cause of death globally, and early detection is crucial for effective treatment and prevention. This project leverages machine learning to build a predictive model that can assist healthcare professionals in identifying high-risk patients. The study demonstrates a complete workflow from data preprocessing and model training to hyperparameter optimization and comparative analysis.

<h2>Key Features</h2> <br>
<ul>
  <li><b>Data Cleaning & Preprocessing</b>: Robust handling of missing data and feature scaling.</li>

 <li><b>Multiple Model Implementation</b>: Compares baseline models (Logistic Regression, KNN) with advanced ensemble methods (Random Forest).</li> 

  <li><b>Hyperparameter Optimization</b>: Utilizes GridSearchCV to fine-tune the Random Forest model, significantly boosting performance and preventing overfitting.</li>

  <li><b>Comprehensive Evaluation</b>: Assesses models using multiple metrics including Accuracy, Precision, Recall, and F1-Score.</li>
</ul>

<h2>Dataset</h2>
This project uses the Heart Disease Dataset from the Kaggle.
<ul>
  <li><b>Instances</b>: 1025</li>
  <li><b>Features</b>: 14 clinical features, including age, sex, chest pain type, resting blood pressure, cholesterol, and more.</li>
  <li><b>Target</b>: Binary classification - presence (1) or absence (0) of heart disease.</li>
</ul>


<h2>Methodology</h2>
The project follows a systematic machine learning pipeline:
<ol>
  <li><b>Data Loading & Cleaning:</b> The dataset is loaded, and missing values (denoted by '?') are imputed using the mode of their respective columns.</li>
  <li><b>Data Preprocessing:</b> The multi-class target variable is converted into a binary format. All features are then standardized using StandardScaler to ensure that all variables contribute equally to model performance.</li>
  <li><b>Model Training:</b> The data is split into an 80% training set and a 20% testing set. Three different models are trained.</li>
  <ul>
    <li><b>Logistic Regression</b></li>
    <li><b>K-Nearest Neighbors (KNN)</b></li>
    <li><b>Random Forest</b></li>
  </ul>
  <li><b>Hyperparameter Tuning:</b> The Random Forest model is optimized using GridSearchCV with 5-fold cross-validation. This process systematically searches for the best combination of hyperparameters to enhance accuracy and generalizability.</li>
  <li><b>Evaluation:</b> All models are evaluated on the unseen test set, and their performances are compared.</li>
</ol>

<h2>Results</h2>

The hyperparameter-tuned Random Forest model demonstrated superior performance, achieving a state-of-the-art accuracy. The optimization process was also crucial in mitigating the overfitting observed in the untuned Random Forest model.
<table border="4">
        <thead>
            <tr>
                <th>Model</th>
                <th>Accuracy</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>Tuned Random Forest</td>
                <td>98.5%</td>
            </tr>
            <tr>
                <td>K-Nearest Neighbors</td>
                <td>86.3%</td>
            </tr>
            <tr>
                <td>Logistic Regression</td>
                <td>81.0%</td>
            </tr>
        </tbody>
    </table>
The final tuned model is both highly accurate and robust, making it a reliable tool for this prediction task.
