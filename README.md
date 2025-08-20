### **Cardiovascular Disease Prediction**

This project focuses on building and optimizing a machine learning model to predict a patient's risk of cardiovascular disease based on their medical history and lifestyle records.

#### **Project Overview**

Cardiovascular diseases (CVDs) are the leading cause of death globally. Early prediction of a patient's risk is crucial for timely intervention and preventative care. This project addresses that need by analyzing a comprehensive dataset to identify key risk factors and build a robust classification model.

-----

#### **Key Findings & Insights**

Through in-depth Exploratory Data Analysis (EDA), I uncovered several key insights that guided the model-building process:

  * **Age and BMI are Major Risk Factors:** There is a strong positive correlation between a patient's age and BMI and the likelihood of having cardiovascular disease.
  * **Lifestyle Matters:** Patients who reported exercising regularly and having a healthier diet (higher fruit and vegetable consumption) were significantly less likely to have heart disease.
  * **Medical History is a Strong Predictor:** The presence of other conditions like diabetes and arthritis showed a very strong correlation with heart disease.
  * **Data Imbalance:** The dataset was highly imbalanced, with a large majority of patients not having heart disease. This was a key challenge that was addressed throughout the project.

-----

#### **Methodology**

I followed a complete end-to-end machine learning workflow:

1.  **Data Acquisition & Preprocessing:** I sourced the dataset and performed meticulous cleaning. This included handling outliers, converting all categorical variables to a numerical format using **One-Hot Encoding** and **Manual Ordinal Mapping**, and dropping redundant features.
2.  **Exploratory Data Analysis (EDA):** I used various visualizations (histograms, bar plots, violin plots) to understand the data's distribution and the relationships between features and the target variable.
3.  **Model Selection & Evaluation:** I trained several classification models, including **Logistic Regression, Decision Tree, and Random Forest**, and advanced models like **Gradient Boosting Machines** and **LinearSVC**.
4.  **Handling Imbalance:** To address the imbalanced data, I used parameters like `class_weight='balanced'` and `scale_pos_weight` to ensure the models correctly identified the minority class.
5.  **Hyperparameter Tuning:** I performed **Grid Search** to find the optimal hyperparameters for the best-performing model to maximize its performance.

-----

#### **Best Performing Model**

The **LinearSVC model** emerged as the final chosen model due to its exceptional performance on the most critical metric: `recall`.

  * **Model:** LinearSVC (tuned)
  * **Final Recall:** **0.83**
  * **Interpretation:** This model is capable of correctly identifying **83% of all patients with cardiovascular disease** in the test set. This high recall makes it highly suitable for a real-world medical application where the goal is to find as many at-risk patients as possible.

-----

#### **Technologies Used**

  * Python
  * pandas
  * NumPy
  * scikit-learn
  * Matplotlib
  * Seaborn
  * Jupyter Notebook
  * KaggleHub

-----

#### **How to Run the Project**

1.  **Clone the repository:**
    ```bash
    git clone [your-repository-url]
    cd [your-repository-name]
    ```
2.  **Install prerequisites:** Ensure you have Python and `pip` installed.
    ```bash
    pip install pandas numpy scikit-learn matplotlib seaborn kagglehub
    ```
3.  **Download the data:** You can download the `CVD_cleaned.csv` file from Kaggle or use the provided KaggleHub code in the notebook to download it. Place the CSV file in your project directory.
4.  **Run the notebook:** Open the Jupyter Notebook file and run the cells in order. The notebook contains all the code from data acquisition to the final model evaluation.
