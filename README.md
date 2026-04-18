# Customer Purchase Prediction & Marketing Optimization

## Project Overview
This project focuses on predicting whether a customer will respond to a marketing campaign using machine learning techniques.

The objective is not only to build accurate models but also to evaluate their effectiveness in identifying potential buyers and improving marketing strategies.

Three models were implemented and compared:

- Logistic Regression (Baseline)
- Random Forest Classifier
- XGBoost Classifier (Advanced Model)

The dataset includes customer demographics, purchasing behavior, and campaign interaction data.

---

## Objective
To build a predictive model that identifies customers likely to respond to marketing campaigns, while evaluating performance based on business impact rather than accuracy alone.

---

## Dataset
**Source:** https://www.kaggle.com/datasets/imakash3011/customer-personality-analysis  

**Dataset Used:** `marketing_campaign.csv`

**Key Characteristics:**
- ~2,240 customer records  
- 29 features (before preprocessing)  
- Mix of numerical and categorical variables  
- Includes demographics, income, spending, and campaign responses  
- Target variable: **Response (0 = No, 1 = Yes)**  

---

## Tools & Technologies
- Python  
- Pandas, NumPy  
- Scikit-learn  
- XGBoost  
- Matplotlib, Seaborn  
- Jupyter Notebook  
- Tableau  

---

## Data Preprocessing

### Steps Performed
- Handled missing values using median imputation  
- Created new features:
  - Age (from Year_Birth)  
  - Total Spending  
  - Total Purchases  
- Dropped irrelevant columns:
  - ID, Dt_Customer, Z_CostContact, Z_Revenue  
- Applied one-hot encoding for categorical variables  
- Split dataset into training (80%) and testing (20%)  
- Applied feature scaling for Logistic Regression  

### Explanation
Feature engineering improves the model’s ability to capture customer behavior patterns, while encoding and scaling ensure compatibility with machine learning algorithms.

---

## Model

### Models Used
- Logistic Regression  
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

| Model | Accuracy |
|------|----------|
| Logistic Regression | ~0.873 |
| Random Forest | ~0.864 |
| XGBoost | ~0.873 |

### Key Observation
- Logistic Regression and XGBoost achieved similar performance  
- Random Forest slightly underperformed  

---

## Visualization (Model Performance)

### Confusion Matrix (XGBoost)
- True Negatives: 366  
- False Positives: 13  
- False Negatives: 44  
- True Positives: 25  

### Interpretation
- Strong performance in identifying non-buyers  
- Weak performance in identifying actual buyers  
- High false negatives indicate missed opportunities  

---

## Tableau Dashboard

To translate model results into business insights, a Tableau dashboard was created.

### Key Metrics
- **Total Customers:** 2,240  
- **Predictive Buyers:** 294  
- **Conversion Rate:** 13.13%  

### Key Visual
- Customer Distribution (Buyers vs Non-Buyers)

### Key Insights
- Conversion rate is low (13.13%), indicating untapped revenue potential  
- Majority of customers are non-buyers (86.87%)  
- Opportunity exists to improve targeting strategies and increase conversion rate  

**View Dashboard:**  
https://public.tableau.com/views/CustomerPurchasePredictionDashboard/Dashboard1?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link

---

## Interpretation
Although overall accuracy is high (~87%), this metric is misleading due to class imbalance.

- The model performs well in predicting non-buyers  
- It struggles to identify buyers (low recall ~35%)  
- A significant number of potential buyers are not detected  

This highlights the importance of evaluating models using business-relevant metrics.

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
This project demonstrates how machine learning can support marketing decision-making:

- Target high-probability customers  
- Reduce unnecessary marketing costs  
- Improve conversion rates  
- Increase return on investment (ROI)  

Improving recall can significantly enhance business impact by capturing more potential buyers.

---

## Limitations
- Imbalanced dataset  
- Low recall for the positive class  
- No hyperparameter tuning  
- Limited feature engineering  

---

## Future Improvements
- Apply SMOTE or resampling techniques  
- Perform hyperparameter tuning  
- Optimize for recall or F1-score  
- Explore advanced models (LightGBM, CatBoost)  
- Implement cross-validation  
- Enhance feature engineering  
- Deploy model using Streamlit for real-time predictions  

---

## Conclusion
Logistic Regression and XGBoost delivered the best performance (~87% accuracy), while Random Forest slightly underperformed.

Despite strong accuracy, all models struggled to identify potential buyers due to low recall, leading to missed revenue opportunities.

This project highlights the importance of aligning machine learning evaluation with business objectives.

---

## Author
**Allen Adajar**  
Cost Accountant | Data Analyst | Aspiring Data Scientist  

GitHub: https://github.com/lenadajar0801-boop
