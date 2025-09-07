# 🎯 Customer Response Prediction Project

This project analyzes customer behavior data to predict which customers are most likely to respond to marketing campaigns. By understanding key factors influencing response rates, businesses can improve targeting, increase ROI, and reduce wasted marketing spend.

---

## 📊 Project Overview

### 💡 Purpose
To build a predictive model that identifies customers most likely to respond to a marketing campaign using historical customer data.

### 🔍 Objective
- Understand what drives customer responses.
- Build a reliable prediction model.
- Provide actionable business recommendations.

### 🗺 Scope
The analysis uses a dataset containing customer demographics, purchase history, campaign responses, and website activity to:
1. Clean and prepare the data.
2. Explore key patterns.
3. Build a Logistic Regression model.
4. Evaluate performance and derive insights.

---

## 📂 Dataset

The dataset (`ifood_df.csv`) contains anonymized customer records from a retail/ed-tech company. Key features include:

| Feature | Description |
|--------|-----------|
| `Income` | Annual household income |
| `Kidhome`, `Teenhome` | Number of children/teenagers at home |
| `Recency` | Days since last purchase |
| `MntWines`, `MntFruits`, etc. | Amount spent on product categories |
| `NumWebPurchases`, `NumStorePurchases` | Purchase channels |
| `AcceptedCmp1-5` | Whether customer accepted past campaigns |
| `Response` | Target variable: 1 if responded to latest campaign |

> 🔧 Data Source: Publicly available (similar to iFood or EdTech datasets)

---

## 🛠️ Tools & Technologies

- **Python**: Primary programming language
- **Pandas**: Data manipulation and cleaning
- **Scikit-learn**: Machine learning (Logistic Regression)
- **Matplotlib / Seaborn**: Data visualization
- **Jupyter Notebook**: Interactive coding environment
- **Tableau Public**: Dashboard creation and sharing

---

## 🧪 Methodology

The project followed a standard data science workflow:

1. **Data Cleaning & Preparation**
   - Handle missing values
   - Convert categorical variables to dummy variables
2. **Exploratory Data Analysis (EDA)**
   - Visualize distributions and correlations
   - Identify trends and outliers
3. **Feature Engineering**
   - Create new features (e.g., `TotalSpent`)
   - Select relevant variables
4. **Model Building**
   - Train a Logistic Regression model
   - Compare with Random Forest (optional)
5. **Evaluation**
   - Measure accuracy, AUC, precision, recall
   - Interpret feature importance
6. **Business Insights & Recommendations**

---

## 📈 Key Findings

### 📉 Overall Campaign Response Rate
Only **15.1%** of customers responded to the campaign.

![Overall Campaign Response Rate](https://github.com/sriks023/Camping-Marketing-Analysis-/blob/main/Overall%20Campaign%20Response%20Rate.png)

### 📊 Top Features Increasing Likelihood of Response
Customers who are more active online and have responded before are more likely to engage.

![Top Features Increasing Likelihood of Response](https://github.com/sriks023/Camping-Marketing-Analysis-/blob/main/Top%20Features%20Increasing%20Likelihood%20of%20Response.png)

### 📊 Top Features Decreasing Likelihood of Response
Customers who haven't purchased recently or have teenagers at home are less likely to respond.

![Top Features Decreasing Likelihood of Response](https://github.com/sriks023/Camping-Marketing-Analysis-/blob/main/Top%20Features%20Decreasing%20Likelihood%20of%20Response.png)

### 📊 Response Rate by Education Level
Customers with higher education levels (especially PhD) have higher response rates.

![Response Rate by Education Level](https://github.com/sriks023/Camping-Marketing-Analysis-/blob/main/Response%20Rate%20by%20Education%20Level.png)

### 📊 Model Performance
- **Accuracy**: 89.57%
- **AUC Score**: 0.5000
- **Confusion Matrix**: Shows true vs. predicted labels

![Confusion Matrix](https://github.com/sriks023/Camping-Marketing-Analysis-/blob/main/Confusion%20Matrix.png)

> ⚠ Note: High accuracy but low AUC suggests the model is good at predicting "No Response" but struggles to rank high-probability responders.

---

## 🎯 Business Insights & Recommendations

### ✅ Who Should Be Targeted?
- **Recent Shoppers**: Customers who bought recently (`Recency`).
- **Online Engagers**: Frequent website visitors (`NumWebVisitsMonth`).
- **Meat & Wine Buyers**: Spend more on specific products (`MntMeatProducts`, `MntWines`).
- **Past Responders**: Customers who accepted previous campaigns (`AcceptedCmpOverall`).
- **Singles**: Higher likelihood to respond (`marital_Single`).
- **Highly Educated**: Especially those with a PhD (`education_PhD`).

### ❌ Who Might Be Less Responsive?
- **Long-Time No See**: Customers with high `Recency`.
- **In-Store Shoppers**: Prefer physical stores (`NumStorePurchases`).
- **Families with Teenagers**: `Teenhome` is negatively correlated with response.

### 💡 How This Helps the Business
- **Improve Marketing ROI**: Focus budget on high-probability customers.
- **Reduce Customer Acquisition Cost**: Retain existing customers instead of acquiring new ones.
- **Enhance Customer Experience**: Send personalized offers to the right people.
- **Learn About Customers**: Gain deeper insights into customer behavior.

---

## 🏁 Conclusion

This project successfully demonstrated how data analysis can be used to make smarter marketing decisions. By building a predictive model and interpreting its results, we identified clear patterns in customer behavior. These insights provide a practical roadmap for improving campaign effectiveness and driving better business outcomes.

---
