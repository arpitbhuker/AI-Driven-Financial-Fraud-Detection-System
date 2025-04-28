# AI-Driven-Financial-Fraud-Detection-System

# Objective:
The primary aim of this project is to design and implement a machine learning-based system to detect fraudulent financial transactions.
The focus is on accurately distinguishing fraudulent activities from legitimate transactions to support financial institutions in reducing losses and increasing customer trust.


# Implementation:

•	Data Collection: 

- Collected a dataset containing various types of financial transactions, labeled as fraudulent or legitimate.


•	Data Preprocessing:

- Managed missing values.

- Created new features like diffOrg and diffDest to detect balance discrepancies.

- Removed unnecessary columns such as nameOrig and nameDest.

- Focused on specific transaction types (TRANSFER and CASH_OUT) for enhanced fraud detection.


•	Feature Engineering:

- Applied log transformation to deal with skewed transaction amounts.

- Normalized feature values for consistent model input.


•	Handling Class Imbalance: 

- Applied SMOTE (Synthetic Minority Oversampling Technique) to generate synthetic examples of minority (fraud) cases and balance the dataset.


•	Model Training:

- Trained an XGBoost Classifier, leveraging its robustness and efficiency for classification tasks.

- Developed two models: one using the full dataset, another specialized for selected transaction types.


•	Model Evaluation: 
- Evaluated model performance based on F1 Score, Accuracy, and ROC AUC Score.



# Applications:

•	Online banking fraud detection.

•	E-commerce transaction monitoring.

•	Credit card fraud detection and prevention.

•	Insurance fraud investigation systems.

•	Anti-money laundering (AML) compliance support.



# Final Result:

•	Developed two high-performing machine learning models.

•	The model focused on TRANSFER and CASH_OUT transactions showed superior accuracy and fraud detection capabilities.

•	The models achieved strong F1 scores and high ROC AUC scores on test data, indicating reliable performance.



# Evaluation Metrics:


- Accuracy	    99.2%

- Precision	    96.5%

- Recall	        94.8%

- F1-score	    95.6%

- AUC-ROC Score	0.987


•	The model achieved very high overall accuracy (99.2%).

•	Precision and recall values indicate that the model is effective at correctly identifying fraud cases while minimizing false positives.

•	A high AUC-ROC score (0.987) demonstrates excellent discriminatory power between fraudulent and legitimate transactions.



# Analysis:

•	Fraudulent transactions were mainly found in TRANSFER and CASH_OUT types.

•	Feature creation (diffOrg, diffDest) significantly improved detection ability.

•	Using SMOTE for balancing helped the models to better recognize fraud cases.



# Feature Importance:

The top 8 most important features identified by the model are:

•	newbalanceOrig – New balance of the originator (sender) after the transaction.

•	oldbalanceOrg – Original balance of the sender before the transaction.

•	amount – Transaction amount.

•	diffOrg – Difference in the sender’s balance before and after the transaction.

•	CASH_OUT – Indicator feature for cash-out transactions.

•	step – Time step at which the transaction occurred.

•	PAYMENT – Indicator feature for payment transactions.

•	diffDest – Difference in the receiver’s balance before and after the transaction.

These features were critical in identifying suspicious patterns and enhancing the model’s prediction accuracy.



# Future Development:

•	Real-time deployment of the fraud detection system using REST APIs.

•	Advanced modeling with deep learning techniques like LSTM for sequential transaction behavior analysis.

•	Integration of additional features like location, device data, and IP address tracking for richer fraud signals.

•	Adaptive learning models that continuously update with new fraud trends.

•	Explainable AI (XAI) methods to improve model transparency and help financial auditors understand fraud predictions.

