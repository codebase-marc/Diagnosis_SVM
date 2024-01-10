# Diagnosis_SVM
Code from a Kaggle.Com competition to diagnose disease occurrence within a patient based on columns of snapshotted (non-time series) health data.

# Purpose
At any given time, people have a set of health factors associated with them.

Based on this, we may be able to predict the likelihood of a patient having a disease. --> This can then be used to suggest patient intervention/screening/outreach.

# This Code
I wrote this in Julia as it is a rockstar language for stats and similar enough to Python. Also, Jupyter Notebooks support Julia so long as you have the "IJulia" package installed.

Using 2 .csv files of Train & Test data, this code will:

1. Read the Train file.
2. Make a clean Train file --> Load as DataFrame --> Transform it to a Matrix (CAN'T REMEMBER IF I TRANSPOSE THIS MATRIX..... CONFIRM).
3. Build an SVM Model on this Clean Train Matrix.
4. Back-test that SVM model against the Train Data.
  5. OPPORTUNITY - MAKE IT AUTOIMPROVE BASED ON ITERATIVE BACKTESTS (maybe this is built into SVM modeling though).
6. Read the Test File.
7. Make a clean Test file --> Load as DataFrame --> Transform it to a Matrix (CAN'T REMEMBER IF I TRANSPOSE THIS MATRIX..... CONFIRM)
8. Run the SVM model built earlier against the Test data.
9. Produce a "Submission" variable and .csv output that assigns the likelihood of not having vs. having a diagnosis.



# REMAINING WORK
1. Autodetect all row and column lengths in the Training & Test files & save as variables.
2. Autodetect whether a particular column is a Binary, Categorical, or Quantitative value.
3. For each unique column type, specify an imputing method/technique when a row in that column has a null value. (JUSTIFY EACH IDEAL METHOD OF IMPUTING!!)
4. Figure out how to automatically detect and apply the ideal SVM kernel specifications & weights.
5. Figure out how to deal with a time-series version of this (tensor).


