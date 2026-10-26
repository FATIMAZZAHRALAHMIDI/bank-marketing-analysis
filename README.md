# bank-marketing-analysis
# 🏦 Bank Marketing Analysis & Prediction

## 📖 Project Overview
This project is an end-to-end Data Analysis and Machine Learning study on a dataset from a Portuguese bank. The dataset contains **45,211 clients** contacted during phone marketing campaigns to subscribe to a term deposit.

The main business question is: **"Which clients are most likely to subscribe, and how can the bank optimize its marketing campaigns to increase conversion and reduce costs?"**

## 🛠️ Tools & Technologies Used
- **Python** (Pandas, NumPy) for data manipulation and cleaning.
- **Visualization** (Matplotlib, Seaborn) for Exploratory Data Analysis (EDA).
- **Statistics** (Scipy) for hypothesis testing (Chi-square, T-test).
- **Machine Learning** (Scikit-Learn) for predictive modeling.

## 📂 Project Structure
- `data/`: Contains the raw and cleaned datasets.
- `notebooks/`: Contains the step-by-step Jupyter Notebooks.
  - `01_data_understanding.ipynb`
  - `02_data_cleaning.ipynb`
  - `03_eda.ipynb`
  - `04_statistical_analysis.ipynb`
  - `05_machine_learning.ipynb`
  - `07_business_recommendations.ipynb`

## 📊 Key Insights from EDA
- **Call Duration:** It is the strongest numerical predictor. Subscribers stay on the phone 3x longer than non-subscribers.
- **Target Profiles:** Students and retired people have the highest conversion rates (~30% and ~23%).
- **Campaign Fatigue:** Calling a client more than 5 times drastically reduces their chances of subscribing.
- **Best Months:** March, September, October, and December have the highest conversion rates.
- **Debt:** Clients with a housing or personal loan are less likely to subscribe.

## 🤖 Machine Learning Results
Three models were trained and evaluated: Logistic Regression, Decision Tree, and Random Forest.
- The **Random Forest** model achieved the best performance with an **Accuracy of 91%** and a **Precision of 68%**.
- *Note:* Due to the highly imbalanced dataset (88.3% "No", 11.7% "Yes"), the Accuracy metric is misleading. The model's Recall for the "Yes" class was 39%, meaning it successfully identified 39% of the actual subscribers.

## 💼 Business Recommendations
Based on the analysis, the bank should implement the following strategies:
1. **Target "Golden Profiles":** Prioritize clients who are students, retirees, or have a high bank balance (>60k€), with no loans.
2. **Limit Calls:** Cap the number of calls at 3 per client to avoid campaign fatigue.
3. **Time the Campaigns:** Allocate 80% of the marketing budget to high-conversion months (March, Sept, Oct, Dec) and drastically reduce calls in May and during the summer.
4. **Use the Predictive Model:** Deploy the Random Forest model to generate a targeted list of the top 20% of clients with the highest probability of subscribing, optimizing the sales team's time.

## 🚀 How to Reproduce
1. Clone this repository.
2. Ensure you have Python installed along with the required libraries (`pip install pandas numpy matplotlib seaborn scipy scikit-learn`).
3. Run the notebooks in order (`01` to `07`).

---
*This project was developed as part of a Data Analyst portfolio.*
