# Lead Conversion Prediction with Machine Learning

## Business Context

A growing EdTech company wants to improve how it identifies high-conversion leads from incoming traffic. With marketing costs rising and conversion rates lagging, the goal is to focus sales efforts on leads most likely to convert—and stop wasting budget on low-intent prospects.

## Objective

Build a predictive model that classifies leads as likely to convert or not, and extract actionable insights to inform marketing strategy and sales follow-up.

---

## Dataset Overview

* \~4,600 lead records
* 20+ features including:

  * Demographics (age, occupation, education)
  * Behavior (website time, page views, last activity)
  * Source/channel (referral, print ads, digital media)
  * Funnel progress (profile completion %)

---

## Approach

1. **Exploratory Data Analysis (EDA)**

   * Cleaned and encoded categorical features
   * Identified key trends in high- vs. low-converting leads
   * Detected class imbalance (used class weights in modeling)

2. **Modeling**

   * Benchmarked 4 classifiers:

     * Logistic Regression
     * SVM
     * Decision Tree
     * Random Forest
   * **Best Model:** Random Forest

     * F1 Score: 0.77
     * Precision: 0.73
     * Recall: 0.81
   * Tuned hyperparameters using `GridSearchCV`

3. **Model Explainability**

   * Used SHAP and feature importances to explain predictions
   * Identified key conversion drivers (e.g., time spent on site, profile completion)
   * Surfaced low-impact features and channels (e.g., print ads, outbound calls)

---

## Key Drivers of Conversion

| Top Positive Signals          | Weak/Negative Signals                   |
| ----------------------------- | --------------------------------------- |
| Time spent on website         | Last touch = phone activity             |
| First interaction via website | Generic digital/print media campaigns   |
| High profile completion       | Students/unemployed occupation segments |
| Page views per session        | Low engagement or incomplete profiles   |

<img width="704" height="691" alt="image" src="https://github.com/user-attachments/assets/2dd24033-c77d-478c-8c6a-ad1c607a583b" />


---

## Actionable Insights

* **Double down on site engagement:** Long sessions and high page views are strong intent signals. Improve UX and reduce friction.
* **Send traffic to website, not mobile app:** Website-first users convert more often.
* **Nudge profile completion:** Add progress bars or incentives. It's a top predictor of conversion.
* **Deprioritize cold calls and print ads:** These are low ROI channels. Reallocate budget.
* **Segment by occupation:** Working professionals are more likely to convert than students or unemployed users.
* **Rethink top-of-funnel targeting:** Filter for users who engage on the website and complete their profile.

---

## Business Impact

This project demonstrates how machine learning can support marketing and sales teams by identifying which leads are worth pursuing—and which channels to improve or eliminate. With over 77% precision in flagging high-conversion leads, the model enables more focused campaigns and smarter resource allocation.

---
