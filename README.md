# Customer Purchase Prediction & Marketing Optimization

## Project Overview

This project focuses on predicting whether a customer will respond to a marketing campaign using machine learning techniques.

The goal is not only to build accurate models but also to evaluate their effectiveness in identifying potential buyers and improving marketing strategies.

Three models were implemented and compared:
- Logistic Regression (Baseline)
- Random Forest Classifier
- XGBoost Classifier (Advanced Model)

The dataset contains customer demographics, purchasing behavior, and campaign interaction data.

---

## Objective

To build a predictive model that identifies customers likely to respond to marketing campaigns and to evaluate model performance beyond accuracy, focusing on business impact.

---

## Dataset

Source: https://www.kaggle.com/datasets/imakash3011/customer-personality-analysis  

Dataset Used:

* marketing_campaign.csv  

Dataset characteristics:

* ~2,240 customer records  
* 29 columns (before preprocessing)  
* Mix of numerical and categorical variables  
* Includes demographics, income, spending, and campaign responses  
* Target variable: **Response (0 = No, 1 = Yes)**  

---

## Tools & Technologies

- Python  
- Pandas, NumPy  
- Scikit-learn  
- XGBoost  
- Matplotlib, Seaborn  
- Jupyter Notebook  

---

## Data Preprocessing

### Steps Performed

- Handled missing values using median imputation  
- Created new features:
  - **Age** (from Year_Birth)  
  - **Total Spending**  
  - **Total Purchases**  
- Dropped irrelevant columns:
  - ID, Dt_Customer, Z_CostContact, Z_Revenue  
- Applied one-hot encoding for categorical variables  
- Split dataset into training (80%) and testing (20%)  
- Applied **feature scaling** for Logistic Regression  

### Explanation

Feature engineering improves the model’s ability to capture customer behavior patterns, while encoding and scaling ensure compatibility with machine learning algorithms.

---

## Model

### Models Used

- Logistic Regression (Baseline)  
- Random Forest Classifier  
- XGBoost Classifier  

### Steps Performed

- Trained models using training data  
- Generated predictions on test data  
- Evaluated models using:
  - Accuracy  
  - Classification Report  
  - Confusion Matrix  
- Compared model performance  

---

## Results

| Model                | Accuracy |
|---------------------|----------|
| Logistic Regression | ~0.873   |
| Random Forest       | ~0.864   |
| XGBoost             | ~0.873   |

### Key Observation

- Logistic Regression and XGBoost achieved similar performance  
- Random Forest slightly underperformed  

---

## Visualization

### Confusion Matrix (XGBoost)

- True Negatives: **366**  
- False Positives: **13**  
- False Negatives: **44**  
- True Positives: **25**  

### Interpretation of Visualization

- Strong performance in identifying non-responders  
- Weak performance in identifying actual buyers  
- High false negatives indicate missed opportunities  

---

## Interpretation

Although overall accuracy is high (~87%), this metric is misleading due to class imbalance.

- The model performs well in predicting non-buyers (Class 0)  
- However, it struggles to identify buyers (Class 1), as shown by low recall (~0.35–0.36)  
- A significant number of actual buyers are not detected  

Logistic Regression and XGBoost performed similarly, suggesting that the dataset may contain relatively simple or near-linear patterns.

---

## Insights

- High accuracy does not guarantee business effectiveness  
- Models are biased toward predicting non-buyers  
- False negatives represent missed revenue opportunities  
- Recall is more important than accuracy in marketing problems  
- Class imbalance significantly impacts model performance  
- Simpler models can perform competitively with advanced models  

---

## Business Value & Application

This project demonstrates how machine learning can be used to improve marketing decision-making.

By predicting customer response, businesses can:

- Target high-probability customers  
- Reduce unnecessary marketing costs  
- Improve conversion rates  
- Increase return on investment (ROI)  

However, the model’s low recall for buyers indicates that some potential customers are not being identified.

Improving recall can significantly enhance business impact by capturing more high-value customers.

The model can also be integrated into marketing systems to support data-driven targeting and campaign optimization.

---

## Limitations

- Dataset is imbalanced (more non-buyers than buyers)  
- Low recall for the positive class  
- No hyperparameter tuning applied  
- Limited feature engineering  
- Models not optimized for business-specific metrics  

---

## Future Improvements

- Apply SMOTE or resampling techniques to handle class imbalance  
- Perform hyperparameter tuning (GridSearchCV / RandomizedSearchCV)  
- Optimize for recall or F1-score instead of accuracy  
- Explore advanced models such as LightGBM or CatBoost  
- Implement cross-validation  
- Enhance feature engineering  

---

## Conclusion

Logistic Regression and XGBoost delivered the best overall performance with similar accuracy (~87%), while Random Forest slightly underperformed.

Despite strong accuracy, all models struggled to identify potential buyers due to low recall for the positive class.

From a business perspective, this limitation leads to missed revenue opportunities by failing to target customers who are likely to respond.

This project highlights the importance of evaluating models beyond accuracy and aligning machine learning metrics with business objectives.

---

## Author

Allen Adajar  
Cost Accountant | Data Analyst | Aspiring Data Scientist  

GitHub: https://github.com/lenadajar0801-boop  
