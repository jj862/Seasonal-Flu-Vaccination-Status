# Seasonal Flu Vaccination Status


#### Author: Jonah Devoy

The purpose of this assignment was to assemble a classifier to predict whether an individual was vaccinated against the seasonal flu or not as accurate as possible while looking at factors that influence whether someone elects to get vaccinated against the seasonal flu.


## The Data
Taken from <a href="https://www.drivendata.org/competitions/66/flu-shot-learning/page/211/"> DrivenData</a>
* **h1n1_vaccine** - Whether respondent received H1N1 flu vaccine.
* **seasonal_vaccine** - Whether the respondent received seasonal flu vaccine.
* **h1n1_concern** - Level of concern about the H1N1 flu.
0 = Not at all concerned; 1 = Not very concerned; 2 = Somewhat concerned; 3 = Very concerned.
* **h1n1_knowledge** - Level of knowledge about H1N1 flu.
0 = No knowledge; 1 = A little knowledge; 2 = A lot of knowledge.
* **behavioral_antiviral_meds** - Has taken antiviral medications. (binary)
* **behavioral_avoidance** - Has avoided close contact with others with flu-like symptoms. (binary)
* **behavioral_face_mask** - Has bought a face mask. (binary)
* **behavioral_wash_hands** - Has frequently washed hands or used hand sanitizer. (binary)
* **behavioral_large_gatherings** - Has reduced time at large gatherings. (binary)
* **behavioral_outside_home** - Has reduced contact with people outside of own household. (binary)
* **behavioral_touch_face** - Has avoided touching eyes, nose, or mouth. (binary)
* **doctor_recc_h1n1** - The H1N1 flu vaccine was recommended by a doctor. (binary)
* **doctor_recc_seasonal** - Seasonal flu vaccine was recommended by a doctor. (binary)
* **chronic_med_condition** - Has any of the following chronic medical conditions: asthma or another lung condition, diabetes, a heart condition, a kidney condition, sickle cell anemia or other anemia, a neurological or neuromuscular condition, a liver condition, or a weakened immune system caused by a chronic illness or by medicines taken for a chronic illness. (binary)
* **child_under_6_months** - Has regular close contact with a child under the age of six months. (binary)
* **health_worker** - Is a healthcare worker. (binary)
* **health_insurance** - Has health insurance. (binary)
* **opinion_h1n1_vacc_effective** - Respondent's opinion about H1N1 vaccine effectiveness.
1 = Not at all effective; 2 = Not very effective; 3 = Don't know; 4 = Somewhat effective; 5 = Very effective.
* **opinion_h1n1_risk** - Respondent's opinion about risk of getting sick with H1N1 flu without vaccine.
1 = Very Low; 2 = Somewhat low; 3 = Don't know; 4 = Somewhat high; 5 = Very high.
* **opinion_h1n1_sick_from_vacc** - Respondent's worry about getting sick from taking the H1N1 vaccine.
1 = Not at all worried; 2 = Not very worried; 3 = Don't know; 4 = Somewhat worried; 5 = Very worried.
* **opinion_seas_vacc_effective** - Respondent's opinion about seasonal flu vaccine effectiveness.
1 = Not at all effective; 2 = Not very effective; 3 = Don't know; 4 = Somewhat effective; 5 = Very effective.
* **opinion_seas_risk** - Respondent's opinion about the risk of getting sick with seasonal flu without a vaccine.
1 = Very Low; 2 = Somewhat low; 3 = Don't know; 4 = Somewhat high; 5 = Very high.
* **opinion_seas_sick_from_vacc** - Respondent's worry about getting sick from taking the seasonal flu vaccine.
1 = Not at all worried; 2 = Not very worried; 3 = Don't know; 4 = Somewhat worried; 5 = Very worried.
* **age_group** - Age group of respondents.
* **education** - Self-reported education level.
* **race** - Race of respondent.
* **sex** - Sex of respondent.
* **income_poverty** - Household annual income of respondent with respect to 2008 Census poverty thresholds.
* **marital_status** - Marital status of the respondent.
* **rent_or_own** - Housing situation of the respondent.
* **employment_status** - Employment status of the respondent.
* **hhs_geo_region** - Respondent's residence using a 10-region geographic classification defined by the U.S. Dept. of Health and Human Services. Values are represented as short random character strings.
* **census_msa** - Respondent's residence within metropolitan statistical areas (MSA) as defined by the U.S. Census.
* **household_adults** - Number of other adults in the household, top-coded to 3.
* **household_children** - Number of children in household, top-coded to 3.
* **employment_industry** - Type of industry the respondent is employed in. Values are represented as short random character strings.
* **employment_occupation** - Type of occupation of the respondent. Values are represented as short random character strings.


## Models Used: 

#### Logistic regression: Score: 0.78
Why logistic regression? 
- Logistic regression is a machine learning algorithm that is used for binary classification. You should use logistic regression when your Y variable takes only two values, e.g. True and False, "spam" and "not spam", "churn" and "not churn" and so on. The variable is said to be a "binary" or "dichotomous", taking two variables. 

#### Random Forest Classifier: Score: 0.77
Why Random Forest Classifier? 
- Training decision trees on random data samples from the training dataset can reduce variance. Sampling features for each split in a decision tree decorrelates trees.

#### K Neighbors Classifier: Score: 0.69
Why K Neighbors Classifier? 
- K Neighbors Classifier uses proximity to make classifications or predictions about the grouping of an individual data point.

#### Decision Tree Classifier: Score 0.69
Why Decision Tree Classifier? 
- easy to implement
- fast training
- fast inference
- good explainability


## Feature Importance: 
* opinion_seas_vacc_effective - how effective on a scale from 1 to 5 (5 being very effective) the respondent believes the vaccine to be at protecting against the flu
* doctor_rec_seasonal - whether or not the individual's doctor recommended they get the vaccine, specifically 1: their doctor did recommend getting vaccinated was the best predictor
* opinion_seasonal_risk - how concerned on a scale from 1 to 5 (5 being very effective) the respondent is about getting the seasonal flu without the vaccine
* age_group - 2 specific age groups were especially useful for predicting vaccination status: 65+ years and 18-34 years, and a third also made it into the top 20 predictive features (55 - 64 Years)
* health_worker - whether or not the individual is a health worker

## Conclusion:
3 most influential factors in determining whether someone got vaccinated against the seasonal flu in 2009 were:
* How effective they believed the vaccine to be at protecting against the flu.
* Whether a doctor recommended they get the vaccine.
* Their perceived level of risk of getting sick with the flu without the vaccine.

## Recommendations:

* Increase public awareness of the effectiveness of the vaccine in protecting against the flu.
* Doctors should regularly recommend that their patients get vaccinated against the seasonal flu each year. 
* Increase the health literacy of patients. 





