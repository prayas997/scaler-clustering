# 📊 Scaler Learner Clustering – Unsupervised Learning Case Study

## 📌 Project Overview

Scaler is an online tech-versity offering intensive Computer Science and Data Science programs for working professionals. The goal of this project is to **segment Scaler learners into meaningful groups** based on their job roles, experience, compensation, and company background.

Using **unsupervised learning (clustering)**, this project identifies distinct learner personas that can help Scaler personalize learning paths, mentorship, and career guidance.

---

## 🎯 Business Objective

The primary objective of this analysis is to:

* Understand different learner segments
* Identify patterns in career stage, compensation, and company tier
* Enable data-driven personalization of courses and engagement strategies

There is **no target variable**, making clustering the right approach to uncover hidden structures in the data.

---

## 📂 Dataset Description

Each row in the dataset represents a Scaler learner with information such as:

* **Job & Company Details**: Job position, company (anonymized)
* **Career Information**: Experience, employment start year
* **Compensation**: Current CTC, CTC update year
* **Derived Features**: Log-transformed CTC, career class, company tier

Sensitive fields such as email and company identifiers are anonymized.

---

## 🛠️ Key Steps Performed

### 1️⃣ Data Cleaning & Preprocessing

* Handled missing values using mean / KNN imputation
* Fixed invalid year values and extreme salary outliers
* Log-transformed CTC to reduce skewness
* Cleaned noisy company names using regex

### 2️⃣ Feature Engineering

* **Class Flag**: Entry / Mid / Senior / Leadership (based on experience & role)
* **Tier Flag**: Tier-1 / Tier-2 / Tier-3 companies (based on frequency & prominence)
* **Job Role Grouping**: Manual clustering of job titles into meaningful categories

### 3️⃣ Feature Selection & Scaling

Only **numerical, distance-meaningful features** were used for clustering:

* Log CTC
* Experience
* Encoded job role
* Encoded company tier

All selected features were standardized before clustering.

---

## 🤖 Clustering Techniques Used

### ✔️ K-Means Clustering

* Elbow Method used to find optimal number of clusters
* Silhouette Score used to validate cluster quality
* Final number of clusters chosen based on both metrics and business interpretability

### ✔️ Hierarchical Clustering

* Used as a secondary method to validate segmentation patterns

---

## 📈 Key Insights

* Majority of learners fall into **Senior-level roles** with high experience
* Mid-level professionals form a strong upskilling segment
* Learners from Tier-2 & Tier-3 companies show higher intent for career growth
* Different job roles exhibit different learning and growth patterns

---

## 📌 Actionable Recommendations

* Design advanced leadership and system design tracks for senior learners
* Focus marketing and mentorship on mid-level professionals
* Provide stronger foundational support for entry-level learners
* Personalize learning paths based on role and company tier

---

## ⚠️ Limitations

* Manual rules for role and tier classification may introduce bias
* KMeans assumes spherical clusters
* Company tiering is heuristic-based

---

## 🚀 Future Improvements

* Use NLP embeddings for job titles instead of manual grouping
* Experiment with Gaussian Mixture Models (GMM)
* Validate clusters using downstream outcomes (placements, promotions)

---

## 🧰 Tech Stack

* Python
* Pandas, NumPy
* Scikit-learn
* Matplotlib, Seaborn

---

## 🏁 Conclusion

This project demonstrates how unsupervised learning can be used to transform raw learner data into actionable insights. By understanding learner segments, Scaler can move towards **personalized, data-driven education experiences**.

---

📌 *This project was built as part of a real-world data science case study and is intended for learning and demonstration purposes.*
