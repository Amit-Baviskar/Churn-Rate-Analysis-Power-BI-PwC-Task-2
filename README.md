# Churn-Rate-Analysis-Power-BI-PwC-Task-2

### **Churn Analysis Report**

---

### **Table of Contents**
1. **Introduction**
2. **Problem Statement**
3. **Stakeholders**
4. **Data Preparation**
5. **Data Modeling (DAX Formulas)**
6. **Dashboard**
7. **Insights**
8. **Conclusion**

---

### **1. Introduction**
This report provides an analysis of customer churn for PhoneNow, a telecom company. The purpose of this report is to assist in identifying patterns and trends related to customer churn, helping to improve retention rates, and understanding the key drivers behind customer departures. The analysis is presented through interactive dashboards displaying demographics, customer account details, and services subscribed to.

---

### **2. Problem Statement**
PhoneNow has experienced high customer churn over the past year, and there is a need to identify the key factors contributing to this churn. Additionally, the company is working to improve gender balance at the executive level while enhancing customer satisfaction and retention. This report aims to explore the characteristics of churned customers, the services they use, and their payment preferences, as well as to recommend actions to reduce churn rates.

---

### **3. Stakeholders**
The key stakeholders involved in this analysis include:
- **Retention Manager**: Janet, who is responsible for analyzing churn data and driving retention strategies.
- **Executives and Senior Management**: Focused on improving overall customer satisfaction, reducing churn, and promoting diversity at leadership levels.
- **Data Analytics Team**: Responsible for creating the dashboards and analyzing data.
- **Customer Service Department**: Directly involved in managing customer relationships and addressing churn concerns.

---

### **4. Data Preparation**
The data used in this analysis consists of customer demographic details, account information, subscription services, and churn data. Key metrics were calculated using DAX formulas within Power BI to derive insights about customer behavior and churn trends.

Data sources include:
- **Churned Customer Data**: A list of customers who have churned, along with their demographic information.
- **Customer Services**: Information on the services each customer subscribed to, such as phone service, internet service, streaming services, and device protection.
- **Account Details**: Information about the customer's account, including payment methods, monthly charges, and contract types.
- **Demographics**: Gender, age, household structure, and senior citizen status.

---

### **5. Data Modeling (DAX Formulas)**

The following DAX formulas were used in the dashboards to model the data and generate insights:

- **% of Dependents**:
  
          DIVIDE(CALCULATE(COUNT(Churn[Dependents]),Churn[Dependents]="Yes",Churn[Churn]="Yes"),CALCULATE(COUNT(Churn[Dependents]),Churn[Churn]="Yes"),0)
  
- **% of Device Protection**:  

           DIVIDE(CALCULATE(COUNT(Churn[DeviceProtection]),Churn[DeviceProtection]="Yes",Churn[Churn]="Yes"),CALCULATE(COUNT(Churn[DeviceProtection]),Churn[Churn]="Yes"),0)
  
- **% of Online Backup**:  

           DIVIDE(CALCULATE(COUNT(Churn[OnlineBackup]),Churn[OnlineBackup]="Yes",Churn[Churn]="Yes"),CALCULATE(COUNT(Churn[OnlineBackup]),Churn[Churn]="Yes"),0)

- **Churn Rate**:  

          DIVIDE(CALCULATE(COUNT(Churn[Churn]),Churn[Churn]="Yes"),(COUNT(Churn[Churn])))

- **% of Phone Service**:  

           DIVIDE(CALCULATE(COUNT(Churn[PhoneService]),Churn[PhoneService]="Yes",Churn[Churn]="Yes"),CALCULATE(COUNT(Churn[PhoneService]),Churn[Churn]="Yes"),0)

- **% of Senior Citizen**:  

           DIVIDE(CALCULATE(COUNT(Churn[SeniorCitizen]),Churn[SeniorCitizen]=1,'Churn'[Churn] = "Yes"),CALCULATE(COUNT('Churn'[SeniorCitizen]),Churn[Churn]="Yes"),0)

---

### **6. Dashboard** ### 

   ### Page 1: 
   ![Churn 1](https://github.com/user-attachments/assets/4e9f49e9-a5c7-494e-ad2e-316bc8e974d5)
   
   ### Page 2: 
   ![churn 2](https://github.com/user-attachments/assets/6bca6dee-b3eb-4321-bfbf-a58eca5accaa)

### **7. Insights**

1. **Customer Demographics**:
   - 25% of churned customers are senior citizens.
   - 36% of churned customers are partners, and 17.4% have dependents.

2. **Customer Account Information**:
   - **Payment Method**: Over 57% of churned customers use electronic checks, which may indicate higher churn rates for customers using this payment method.
   - **Contract Type**: Month-to-month contracts have a significantly higher churn rate (42.71%) compared to two-year (2.83%) and one-year contracts (11.27%).

3. **Services Subscribed**:
   - 69.4% of churned customers have fiber optic internet, with DSL and no internet service accounting for lower churn percentages.
   - 91% of churned customers use phone services, and a high percentage also subscribe to streaming services and device protection.

4. **Churn Rate by Tenure**:
   - Customers with less than one year of tenure have the highest churn rate (45.29%), indicating that early engagement strategies may be necessary to retain new customers.

---

### **8. Conclusion**
The analysis reveals that churn is heavily influenced by contract type, payment method, and tenure. Month-to-month contracts and electronic check payments are associated with higher churn rates. Strategies such as offering better incentives for long-term contracts and promoting alternative payment methods may help reduce churn. Additionally, targeting new customers with tailored retention strategies could mitigate early churn.

---
