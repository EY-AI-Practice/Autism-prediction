# Autism-prediction
Use of machine learning algorithms to predict autism

## Introduction 
The following notebook is based on the [Autism Prediction Kaggle competition](https://www.kaggle.com/competitions/autismdiagnosis/overview). As stated, the objective is to improve autism screening through machine learning and to create awareness among the data science community to develop an AI-based system for the early diagnosis of autism. It is relevant to mention that, nowadays, autism screening is both time-consuming and expensive, and Artificial Intelligence represents an opportunity to tackle this challenge.

The data collected is the result of applying a synthetic data creation algorithm to the dataset from [Autism Screening on Adults](https://www.kaggle.com/datasets/andrewmvd/autism-screening-on-adults), whose original source is a donation from researcher Fadi Thabtah to the Machine Learning Repository of UC Irvine ([UCI Machine Learning Repository: Autism Screening Adult](https://archive.ics.uci.edu/dataset/426/autism+screening+adult)) [1]. As you can imagine, the generation of synthetic data points caused some discrepancies that will be addressed below.

## About the dataset

The data contains answers from people who took the Autism Spectrum Quotient test on an [app](https://www.asdtests.com/) This test includes 10 questions and scores in a range from 0 to 10. If an individual scores 6 or above, it is suggested to visit a specialist for further assessment. The columns of the dataset are listed below:

* ID - ID of the patient
* A1_Score to A10_Score - Score based on Autism Spectrum Quotient (AQ) 10 item screening tool
* age - Age of the patient in years
* gender - Gender of the patient
* ethnicity - Ethnicity of the patient
* jaundice - Whether the patient had jaundice at the time of birth
* autism - Whether an immediate family member has been diagnosed with autism
* contry_of_res - Country of residence of the patient
* used_app_before - Whether the patient has undergone a screening test before
* result - Score for AQ1-10 screening test
* age_desc - Age of the patient
* relation - Relation of patient who completed the test
* Class/ASD - Classified result as 0 or 1. Here 0 represents No and 1 represents Yes. This is the target column, and during submission submit the values as 0 or 1 only.

Strangely, the synthetic data creation included individuals with scores above 6 but without an autism diagnosis, and vice versa. Moreover, if this test indicates a potential autism diagnosis after scoring 6 or more, then the only thing a predictor should do is sum the question points to classify an individual. AI is absolutely unnecessary. Although this discredits the purpose of the Kaggle competition referenced, this data could serve another research objective.

## Scope
