## LMM modeling on LOG transformed and cleaned metabolic measurement without outliers(z-score > 6) as outcome
---

###Objectives

We collected longitudinal data of SGA prescriptions, concomitant medications, fasting blood glucose (BG), lipid profiles, and BMI in a cohort of 767 patients with SCZ, with follow-up up to 18.7 years (median ~6.2 years). A total of 192,152 prescription records were retrieved, with 27,723 metabolic measures analysed. Linear mixed models were used to estimate the effects of SGA on BG, lipid profiles and BMI. Besides studying the effects of SGA medications (as binary predictors), we also investigated the effects of SGA dosage on metabolic profiles.


###Data cleaning
*Before outliers removal:*
No. of metabolic measures=4051, 4051, 4051, 4051, 4076, 7598 for TC, HDL, LDL, TG, BGF, BMI respectively.
No. of metabolic measures (without NA)=4050, 3917, 4037, 4045, 4076, 7598 for TC, HDL, LDL, TG, BGF, BMI respectively.


[1] "cholestrol: 2 outliers found."
[1] "LDL_Chol: 0 outliers found."
[1] "HDL_Chol: 2 outliers found."
[1] "Triglycerides: 11 outliers found."
[1] "BGF: 27 outliers found."
[1] "BMI: 2 outliers found."

*After outliers removal:*
No. of metabolic measures (without NA)=4048, 3917, 4035, 4034, 4049, 7596 for TC, HDL, LDL, TG, BGF, BMI respectively.

###Getting Started
1. Installation of R Pakcages via install.packages():
- data.table (1.14.0)
- dplyr (1.0.6)
- lme4 (1.1.27)
- lubridate (1.7.10)
- sjPlot (2.8.7)
- zoo (1.8.9)

2. Load the *.Rmd scripts in this repository in RStudio (v1.4.1106) with R (v4.0.5).


** Source code:**

This project consists of 2 R markdown file for data pre-processing and modelling respectively. The files should be self-explanatory via the comments.

*1_data_denormalization.Rmd*

  Clean and preprocess the raw data to a dataset suitable for linear mixed modelling.

*2_Modeling_and_Visualization_with_dose.Rmd*

  Build Hybrid Linear Mixed Models (LMM) with between-subject and within-subject component.


- 
