# **Titanic Survival Prediction 🚢**

A Machine Learning project that predicts whether a passenger survived the Titanic disaster based on passenger information such as age, gender, ticket class, fare, and family relationships. This project demonstrates a complete ML workflow including data preprocessing, feature engineering, model training, hyperparameter tuning, cross-validation, evaluation, and feature importance analysis.

📌 **Project Overview**

The sinking of the RMS Titanic is one of the most famous shipwrecks in history. In this project, a machine learning model is built to predict passenger survival using the Titanic dataset.

**The project covers:**

Data loading and exploration
Data preprocessing
Handling missing values
Feature encoding and scaling
Model training using Random Forest Classifier
Hyperparameter tuning using GridSearchCV
Cross-validation for model validation
Model evaluation using classification metrics
Confusion matrix visualization
Feature importance analysis
🎯 Objective

Build a classification model that predicts:

 **Survived = 1 → Passenger survived**

**Survived = 0 → Passenger did not survive**

**📊 Dataset**

The dataset is loaded using Seaborn's built-in Titanic dataset.

Features Used
Feature	Description
pclass	Passenger Class
sex	Gender
age	Passenger Age
sibsp	Number of siblings/spouses aboard
parch	Number of parents/children aboard
fare	Ticket Fare
class	Ticket Class
who	Man, Woman, or Child
adult_male	Whether passenger is an adult male
alone	Whether passenger traveled alone
Target Variable
Variable	Description
survived	Survival status
🛠 Technologies Used
Python
NumPy
Pandas
Matplotlib
Seaborn
Scikit-Learn
📂 Project Structure
Titanic-Survival-Prediction/
│
├── Titanic_Survival_Prediction.ipynb
├── README.md
└── requirements.txt
⚙️ Installation
Clone the Repository
git clone https://github.com/pavandesh14/Titanic-Survival-Prediction.git
cd Titanic-Survival-Prediction
Install Dependencies
pip install numpy pandas matplotlib seaborn scikit-learn
🚀 Workflow
1. Data Collection

Load the Titanic dataset using Seaborn.

titanic = sns.load_dataset('titanic')
2. Data Preprocessing
Numerical Features
Missing values filled using median
Standardization using StandardScaler
Categorical Features
Missing values filled using most frequent value
One-Hot Encoding applied
3. Pipeline Creation

A Scikit-Learn Pipeline is used to automate preprocessing and model training.

Pipeline(
    preprocessing +
    RandomForestClassifier
)
4. Hyperparameter Tuning

GridSearchCV is used to find the best model parameters.

Parameters tested:

{
    'n_estimators': [50,100],
    'max_depth': [None,10,20],
    'min_samples_split': [2,5]
}
5. Cross Validation

5-Fold Stratified Cross Validation ensures robust model performance evaluation.

StratifiedKFold(
    n_splits=5,
    shuffle=True
)
6. Model Evaluation

Evaluation metrics include:

Accuracy
Precision
Recall
F1 Score
Confusion Matrix

Example:

classification_report(y_test, y_pred)
7. Feature Importance

Random Forest feature importances are extracted to identify the most influential survival factors.

Visualization is created using Matplotlib.

📈 Results

The optimized Random Forest model successfully predicts passenger survival with high accuracy after:

Data preprocessing
Hyperparameter optimization
Cross-validation

Key influential features typically include:

Gender
Passenger Class
Fare
Age
Adult Male Status
📉 Confusion Matrix

The confusion matrix provides a visual representation of:

True Positives
True Negatives
False Positives
False Negatives

Heatmap visualization is generated using Seaborn.

🔍 Feature Importance Analysis

The project ranks features according to their contribution toward prediction.

This helps understand:

Which passenger characteristics most affected survival.
How the model makes decisions.
🎓 Learning Outcomes

By completing this project, you will learn:

End-to-end Machine Learning workflow
Data preprocessing techniques
Pipeline construction
Feature engineering
Hyperparameter tuning
Cross-validation
Model evaluation
Model interpretability
📚 Future Improvements
Compare multiple algorithms (XGBoost, SVM, Logistic Regression)
Feature engineering for improved accuracy
Deploy model using Flask or Streamlit
Build an interactive web application
Use Kaggle Titanic dataset for competition-style predictions
🤝 Contributing

**Contributions are welcome.**

Fork the repository
Create a new branch
Commit changes
Push changes
Open a Pull Request
📜 License

This project is intended for educational and learning purposes.

👨‍💻 Author

**Pavan Deshpande**

**Machine Learning | AI Engineering | Data Science Enthusiast**

⭐ If you found this project useful, consider giving it a star on GitHub!
