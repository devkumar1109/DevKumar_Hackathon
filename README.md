# DevKumar_Hackathon
# Vaccine Prediction Project

## Overview
This project aims to predict the likelihood of individuals receiving two types of vaccines: the xyz flu vaccine and the seasonal flu vaccine. The project explores various machine learning models to make these predictions, including Support Vector Machine (SVM), Logistic Regression, and Naive Bayes. Among these models, Naive Bayes performed the best with a mean ROC AUC score of 81%.

## Problem Description
The goal is to predict the probability that a respondent will receive the xyz flu vaccine and the seasonal flu vaccine. This is a multilabel problem where each label is a binary variable:
- xyz_vaccine: Whether the respondent received the xyz flu vaccine (0 = No, 1 = Yes)
- seasonal_vaccine: Whether the respondent received the seasonal flu vaccine (0 = No, 1 = Yes)

## Dataset
The dataset consists of 36 columns:
- respondent_id: Unique identifier for each respondent
- 35 feature columns providing information on respondents' behaviors, opinions, and demographics

### Features
- *Concerns and Knowledge*:
  - xyz_concern: Level of concern about the xyz flu (0-3 scale)
  - xyz_knowledge: Level of knowledge about the xyz flu (0-2 scale)
- *Behavioral Factors*:
  - behavioral_antiviral_meds: Taken antiviral medications (binary)
  - behavioral_avoidance: Avoided close contact with others with flu-like symptoms (binary)
  - behavioral_face_mask: Bought a face mask (binary)
  - behavioral_wash_hands: Frequently washed hands or used hand sanitizer (binary)
  - behavioral_large_gatherings: Reduced time at large gatherings (binary)
  - behavioral_outside_home: Reduced contact with people outside own household (binary)
  - behavioral_touch_face: Avoided touching eyes, nose, or mouth (binary)
- *Medical and Health*:
  - doctor_recc_xyz: xyz flu vaccine recommended by doctor (binary)
  - doctor_recc_seasonal: Seasonal flu vaccine recommended by doctor (binary)
  - chronic_med_condition: Has chronic medical condition (binary)
  - child_under_6_months: Regular close contact with a child under six months (binary)
  - health_worker: Healthcare worker (binary)
  - health_insurance: Has health insurance (binary)
- *Opinions*:
  - opinion_xyz_vacc_effective: Opinion about xyz vaccine effectiveness (1-5 scale)
  - opinion_xyz_risk: Opinion about risk of getting xyz flu without vaccine (1-5 scale)
  - opinion_xyz_sick_from_vacc: Worry of getting sick from xyz vaccine (1-5 scale)
  - opinion_seas_vacc_effective: Opinion about seasonal flu vaccine effectiveness (1-5 scale)
  - opinion_seas_risk: Opinion about risk of getting seasonal flu without vaccine (1-5 scale)
  - opinion_seas_sick_from_vacc: Worry of getting sick from seasonal flu vaccine (1-5 scale)
- *Demographics*:
  - age_group, education, race, sex, income_poverty, marital_status, rent_or_own, employment_status
- *Geographical Information*:
  - hhs_geo_region: Geographic region (random character strings)
  - census_msa: Residence within metropolitan statistical areas (MSA)
- *Household Information*:
  - household_adults: Number of other adults in household (top-coded to 3)
  - household_children: Number of children in household (top-coded to 3)
- *Employment*:
  - employment_industry: Type of industry (random character strings)
  - employment_occupation: Type of occupation (random character strings)

## Models
We evaluated three models:
- *Support Vector Machine (SVM)*
- *Logistic Regression*
- *Naive Bayes*: Achieved the best performance with a mean ROC AUC score of 81%.

## Performance Metric
The performance is evaluated using the area under the receiver operating characteristic curve (ROC AUC) for each target variable. The overall score is the mean of the ROC AUC scores for xyz_vaccine and seasonal_vaccine.


## Results
The Naive Bayes model achieved the highest mean ROC AUC score of 81%.


## Acknowledgments
- Dataset provided by [dataset and all]
- Machine learning models implemented using [scikit-learn](https://scikit-learn.org/)

---

This README provides a comprehensive overview of the project, including the problem description, dataset details, models used, and instructions for setting up and using the code.
