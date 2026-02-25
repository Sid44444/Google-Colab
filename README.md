# Google-Colab
First Google Colab project using load_diabetes
Dataset can be found here: https://scikit-learn.org/stable/api/sklearn.datasets.html

Initially it was necessary to understand a little more about the data provided. 

In the scikit-learn (sklearn) diabetes dataset, the variables
s1 through s6 represent blood serum measurements (blood tests) taken from 442 patients, rather than direct diagnostic markers of having diabetes. These features are used to predict a quantitative measure of disease progression one year after baseline, not just to determine a "yes/no" diagnosis. 
Here is what the indicators s1–s6 mean based on the dataset documentation:

    s1 (tc): Total serum cholesterol.
    s2 (ldl): Low-density lipoproteins ("bad" cholesterol).
    s3 (hdl): High-density lipoproteins ("good" cholesterol).
    s4 (tch): Total cholesterol / HDL ratio.
    s5 (ltg): Log of serum triglycerides level.
    s6 (glu): Blood sugar level. 

How These Indicators Suggest Diabetes Progression
While the dataset is used for regression (predicting a score) rather than classification, certain indicators are strongly associated with higher diabetes progression: 

    Positive Indicators (Higher value = Higher Progression): s1, s2, s4, s5, and s6 generally have positive correlations with the target variable, meaning higher levels of these compounds (especially triglycerides and LDL) are associated with worse disease progression.
    Negative Indicator (Higher value = Lower Progression): s3 (HDL/Good Cholesterol) is negatively correlated with the target. Higher levels of HDL generally mean lower diabetes progression.
    Key Predictors: According to analyses, s5 (triglycerides) is highly predictive of disease progression. 

Important Notes on the Data

    Normalized: The s1-s6 values in sklearn are pre-scaled, meaning they are not raw mg/dL measurements, but rather mean-centered and standardized.
    Context: The target (y) is not a "diabetes/no diabetes" label, but a number representing "disease progression one year after baseline". 

For diagnosis in a medical context, doctors typically look at s6 (blood sugar) and other metrics like HbA1c, not the scaled serum data found in this machine learning dataset
