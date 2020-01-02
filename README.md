## Classifying Hospital Readmission Risk in Diabetes Patients

### Project 3 – Metis Data Science Bootcamp  (Weeks 4-5)

**Technical Focus**
- Classification 
	- Logistic regression 
	- KNN
	- Naive Bayes
	- SVM
	- Decision Tree
	- Random Forest
	- Gradient Boosting
---
### Project Goals
1) Provide a tool for doctors and hospital systems that flags patients with a high-risk of hospital readmission

2) Analyze data for any systemic issues in patient care that may increase the chances of readmission

*How can doctors and medical staff leverage hospital encounters most effectively in order to avoid unnecessary readmissions*
---
### Problem Statement
A readmission is defined as a subsequent hospital encounter within 30 days of the original admission. The readmission rate for the general population is ~10% while the rate for diabetic patients is ~20%. This twofold increase can be largely attributed to the host of diabetes' comorbid conditions: high blood pressure, obesity, cardiovascular disease, and kidney disease.   

In 2011, readmissions were responsible for over $41.3 billion dollars in cost. Rehospitalization is frequently more expensive than the original encounter.

---
### Process
- Analyze over 100,000 diabetic hospital encounters (patients for whom diabetes was a medical condition, even if it was not the primary reason for hospitalization). 

- With hundreds of features including patient demographics + medical history and hospital tests, procedures, and discharge decisions, build a model that optimizes for recall and AUC.  In this context, a high false-positive rate is not detrimental.  Hospitals should be willing to be overly cautious with lower-risk patients in order to more robustly capture high-risk patients. 

---
### Results
- A cross-validated random forest model with 600 trees and a max depth of 12 optimized both recall and AUC.  In minimizing the false-negative rate, the ensemble model captured the greatest number of patients at high-risk of readmission. 

-  Patient medical history proved to be the most salient feature – patients who had previously been hospitalized – perhaps multiple times that year – were at an elevated risk to be readmitted within 30 days. 
---
### Why isn't A1c measured more frequently? 

- The A1c test is a simple blood test that measures one’s average blood glucose level over 3 months.

- Regular monitoring of A1c is consistently linked with lower costs and lower readmission rates.
	 - Data analysis showed that just the *decision* to measure A1c led to lower readmission rates.
 
 **80% of readmitted patients did not receive the A1c test.**

It is critical that doctors and hospital systems look beyond a patient's primary diagnosis. For many of the patients in this dataset, diabetes was *not* the primary diagnosis,  However, the administering of the A1c test (no matter the level!) was associated with lower readmission risks. The simple blood test is a valuable biomarker that can reveal insight into a patient's risk of diabetic complications. If we are serious about lower the rate of of avoidable readmissions, accounting for evident risk factors in a prevalent disease such as diabetes is a necessary place to start.
