# Customer Churn Prediction for Telecom Industry

##  Project Overview

Built a machine learning model to predict customer churn with **85% accuracy (AUC)**, enabling proactive retention strategies that could save **$68,000 annually** with a **377% ROI**.

##  Key Results

- **Model Performance**: 85.3% AUC Score
- **Business Impact**: Identified 180 high-risk customers
- **ROI**: 377% return on retention investment
- **Catch Rate**: 75% of churners identified in high-risk segment

##  Key Insights

1. **Tenure is Critical**: New customers (<12 months) have 3x higher churn rate
2. **Contracts Work**: 2-year contracts reduce churn by 93% vs month-to-month
3. **Service Bundling**: Customers with 5+ services churn 60% less
4. **Pricing Paradox**: Churned customers pay $13 more/month on average

##  Tech Stack

- **Python**: pandas, numpy, scikit-learn, XGBoost
- **Visualization**: matplotlib, seaborn
- **Explainability**: SHAP
- **ML Techniques**: Classification, Feature Engineering, Class Imbalance Handling

##  Project Structure
```
churn-prediction/
├── data/
│   ├── WA_Fn-UseC_-Telco-Customer-Churn.csv
│   ├── high_risk_customers.csv
│   └── project_summary.csv
├── notebooks/
│   └── churn_analysis.ipynb
├── images/
│   ├── 01_tenure_distribution.png
│   ├── 02_contract_churn.png
│   ├── 08_model_comparison.png
│   └── ... (12 visualizations total)
├── models/
│   ├── xgboost_churn_model.pkl
│   ├── scaler.pkl
│   └── feature_names.pkl
└── README.md
```

##  How to Run

1. **Clone the repository**
```bash
   git clone <your-repo-url>
   cd churn-prediction
```

2. **Install dependencies**
```bash
   pip install pandas numpy matplotlib seaborn scikit-learn xgboost shap jupyter
```

3. **Run the notebook**
```bash
   jupyter notebook notebooks/churn_analysis.ipynb
```

##  Model Performance

| Model | ROC-AUC | Precision | Recall | F1-Score |
|-------|---------|-----------|--------|----------|
| Logistic Regression | 0.842 | 0.656 | 0.742 | 0.696 |
| **XGBoost** | **0.853** | **0.672** | **0.758** | **0.712** |

##  Business Recommendations

### Immediate Actions
- Target 180 high-risk customers with contract upgrade offers
- Launch retention campaign: 15% discount for 1-year commitment
- Expected net benefit: $68,000 (377% ROI)

### Short-term (6 months)
- Implement "First Year Success" onboarding program
- Investigate fiber optic service quality issues
- Migrate electronic check users to auto-pay

### Long-term (1 year)
- Deploy real-time churn monitoring dashboard
- A/B test retention strategies by segment
- Increase service bundling initiatives

## 📊 Interactive Power BI Dashboard

Built a professional 2-page Power BI dashboard to translate ML predictions into executive-ready insights and actionable retention strategies.
## 📄 Page 1: Executive Dashboard

![Executive Dashboard](images/Churn_Dashboard_1Page.pdf)

### Key Features

#### 🔢 Real-Time KPIs
- **Total Customers:** 7,043
- **Churn Rate:** 26.5%
- **High-Risk Customers:** 180 (>70% churn probability)
- **Model Accuracy:** 85.3% AUC

#### 📊 Interactive Visualizations

**1. Churn Distribution (Donut Chart)**
- Visual breakdown: 73.5% retained vs 26.5% churned
- Color-coded: Green (retained), Red (churned)

**2. Risk Tier Segmentation (Bar Chart)**
- Low Risk: 2,850 customers (Green)
- Medium Risk: 3,015 customers (Orange)  
- High Risk: 180 customers (Red)
- Click to filter entire dashboard by risk level

**3. Churn Probability Distribution (Area Chart)**
- Histogram showing customer distribution across probability ranges
- Identifies concentration of high-risk customers (0.7-1.0 range)

**4. Contract × Tenure Analysis (Matrix)**
- Heat map with conditional formatting
- **Key Insight:** Month-to-month contracts with <1 year tenure = 45% churn
- Shows contract type as strongest retention lever

**5. Top 10 Churn Drivers (Bar Chart)**
- Feature importance from XGBoost model
- Ranked by predictive power:
  1. Tenure (0.18 importance)
  2. Monthly Charges (0.14)
  3. Total Charges (0.12)
  4. Contract Type (0.11)
  5. Internet Service Type (0.09)

#### 💡 Key Insights Cards

**🔴 New Customers at Risk**
- Customers <12 months tenure have **3X higher churn rate**
- **Action:** Implement 90-day onboarding program

**🟡 Contract Lock-In Works**  
- Month-to-month: 43% churn → 2-year: 3% churn (**93% reduction**)
- **Action:** Offer contract upgrade discounts

**🟢 Service Bundling Pays Off**
- Customers with 5+ services churn **60% less**
- **Action:** Create bundle promotions

#### 🎛️ Interactive Controls
- **Contract Type Slicer:** Filter entire dashboard by Month-to-month/One year/Two year
- **Cross-filtering:** Click any chart to dynamically update all visuals
- **Drill-through:** Expand matrix rows for detailed segment analysis

