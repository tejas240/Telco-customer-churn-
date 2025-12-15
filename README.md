# Telco-customer-churn-EDA & Modelling
This repo is for understanding factors effecting customer churn for a telecomm business. It dives into understanding customer traits and preferences, services to predict likelihood of a customer churning out.
Recommendations to Reduce Customer Churn

Based on the analysis of categorical and numerical parameters, several factors influence churn, including contract type, tenure, monthly charges, payment method, internet service type, and family status. The following recommendations are designed to reduce churn and improve customer retention:

1. Contract & Tenure

   Issue: Month-to-month customers churn more, especially in the first 6 months.
<img width="751" height="562" alt="image" src="https://github.com/user-attachments/assets/efe3b324-f03b-442a-ab94-39714e23684f" />


   Recommendation:

   Offer discounts or loyalty rewards for customers who commit to 1- or 2-year contracts.

   Create welcome offers for new customers to keep them engaged during the risky early months.

2. Pricing & Monthly Charges

   Issue: High monthly charges correlate with churn.
   <img width="765" height="534" alt="image" src="https://github.com/user-attachments/assets/fa1bd182-6d7d-445f-a854-72a117557a4b" />


   Recommendation:

    Introduce tiered pricing or bundled packages to reduce perceived cost.

    Offer personalized discounts to high-risk customers flagged by the churn model.

3. Payment Method

    Issue: Customers using electronic checks churn more.
   <img width="802" height="719" alt="image" src="https://github.com/user-attachments/assets/658d1d9a-f7f5-4604-9d04-5771dbc0ad16" />


    Recommendation:

    Encourage auto-payment methods (credit card, bank transfer) with incentives like cashback or fee waivers.

    Simplify payment processes to reduce friction.

4. Internet Service Type

    Issue: Fiber optic customers churn more than DSL.
   <img width="792" height="553" alt="image" src="https://github.com/user-attachments/assets/77dce986-1eb5-4101-9a87-34a85f29472c" />


    Recommendation:

    Improve fiber service reliability and customer support.

    Offer service guarantees or proactive maintenance for fiber customers.

5. Family & Dependents

    Issue: Single customers churn more than those with family ties.
   <img width="749" height="553" alt="image" src="https://github.com/user-attachments/assets/fc524fe5-f2bc-4790-8aac-97e029067866" />


    Recommendation:

    Design family bundles or multi-line discounts to increase stickiness.

    Target single customers with engagement campaigns to build loyalty.

6. Customer Engagement

    Issue: New customers churn quickly if they don’t feel valued.
   <img width="713" height="538" alt="image" src="https://github.com/user-attachments/assets/3fc6c228-e5ff-4b20-b616-5181117b1635" />


    Recommendation:

    Launch onboarding programs (tutorials, welcome calls, personalized offers).

    Provide proactive support in the first 90 days.

Conclusion
    By implementing these strategies, businesses can reduce churn significantly. The focus should be on incentivizing long-term contracts, offering personalized pricing, improving service quality, and enhancing customer engagement. These actions not only reduce churn but also strengthen customer loyalty and lifetime value.


Churn Prediction using Logistic Regression Model:

Data Preparation
Cleaned the dataset by converting TotalCharges to numeric and imputing missing values (median for numeric, mode for categorical).
Removed problematic features like tenure_bin that introduced NaNs or categorical strings.
Applied one‑hot encoding to categorical variables and standardized numeric features for model stability.
Ensured train/test sets were aligned and free of missing values before modeling.

⚙️ Model Choice
Selected Logistic Regression as the baseline model.
Used class_weight='balanced' to address class imbalance between churners and non‑churners.
Logistic Regression was chosen for its interpretability and ability to connect coefficients directly to business drivers.

📈 Evaluation
Evaluated using Recall, F1‑Score, and ROC‑AUC, since accuracy alone is misleading in imbalanced datasets.
Achieved strong recall for churners, ensuring the model effectively identifies at‑risk customers.
ROC‑AUC demonstrated good discrimination between churn and non‑churn classes.

🔎 Insights from Coefficients
Positive drivers of churn:
Month‑to‑month contracts
Higher monthly charges
Lack of online security or tech support services

Negative drivers (reduce churn):
Longer tenure
Automatic payment methods
Bundled services

🎯 Business Impact
The model highlights actionable strategies:
Incentivize long‑term contracts to reduce churn.
Offer discounts or loyalty rewards to high‑charge customers.
Promote auto‑payment and bundled services to improve retention.

✅ Conclusion
Logistic Regression provided a clean, interpretable baseline model that not only predicts churn but also explains why customers leave. This interpretability makes it ideal for consultancy and business storytelling, where actionable insights matter as much as predictive accuracy.
