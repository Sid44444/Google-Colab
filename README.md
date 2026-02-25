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

For diagnosis in a medical context, doctors typically look at s6 (blood sugar) and other metrics like HbA1c, not the scaled serum data found in this machine learning dataset.

An example of data is provided below.

      age         sex          bmi         bp           s1          s2          s3         s4          s5           s6      target
0 	0.038076 	0.050680 	0.061696 	0.021872 	-0.044223 	-0.034821 	-0.043401 	-0.002592 	0.019907 	-0.017646 	151.0
1 	-0.001882 	-0.044642 	-0.051474 	-0.026328 	-0.008449 	-0.019163 	0.074412 	-0.039493 	-0.068332 	-0.092204 	75.0
2 	0.085299 	0.050680 	0.044451 	-0.005670 	-0.045599 	-0.034194 	-0.032356 	-0.002592 	0.002861 	-0.025930 	141.0
3 	-0.089063 	-0.044642 	-0.011595 	-0.036656 	0.012191 	0.024991 	-0.036038 	0.034309 	0.022688 	-0.009362 	206.0
4 	0.005383 	-0.044642 	-0.036385 	0.021872 	0.003935 	0.015596 	0.008142 	-0.002592 	-0.031988 	-0.046641 	135.0
5 	-0.092695 	-0.044642 	-0.040696 	-0.019442 	-0.068991 	-0.079288 	0.041277 	-0.076395 	-0.041176 	-0.096346 	97.0
6 	-0.045472 	0.050680 	-0.047163 	-0.015999 	-0.040096 	-0.024800 	0.000779 	-0.039493 	-0.062917 	-0.038357 	138.0
7 	0.063504 	0.050680 	-0.001895 	0.066629 	0.090620 	0.108914 	0.022869 	0.017703 	-0.035816 	0.003064 	63.0
8 	0.041708 	0.050680 	0.061696 	-0.040099 	-0.013953 	0.006202 	-0.028674 	-0.002592 	-0.014960 	0.011349 	110.0
9 	-0.070900 	-0.044642 	0.039062 	-0.033213 	-0.012577 	-0.034508 	-0.024993 	-0.002592 	0.067737 	-0.013504 	310.0

