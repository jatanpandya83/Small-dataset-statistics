# Small-dataset-statistics
Statistical analysis of small dataset
# About Platelet Count
Platelets are the smallest type of cell found in the blood. Platelets help stop bleeding after an injury by gathering around the injury site, plugging the hole in the bleeding vessel and helping the blood to clot more quickly. Platelet counts may be done if you are prone to bruising or if you are about to have surgery. The platelet count may change with bleeding disorders, heart disease, diabetes and inflammatory disorders.

The reference range for healthy platelet count is 140-400 thousand/uL.

A lower-than-normal platelet count is called thrombocytopenia. Low platelet count can be divided into 3 main causes:

- Not enough platelets are being made in the bone marrow
- Platelets are being destroyed in the bloodstream
- Platelets are being destroyed in the spleen or liver

# My story!!
I am a software engineer by profession. In general, I am curious and inquisitive about data; especially when the data means something to me, at a personal level. That is exactly what happened to me a few months ago, when my doctor found out through lab tests that my platelet count had dropped in the last year; and she wanted me to see a hematologist. She wanted to find out if I had thrombocytopenia (a medical condition causing low platelet count)?

I wanted to know how worrisome are my results? And the statistician inside me wanted to answer that same question a bit more quantitatively. I was infact, too excited to apply some statistical techniques and tools that I had recently learnt in a statistics course.

# How many data points?
When you start analyzing health data, you are hit by the reality that it may be too small. What that means is that central limit theorem(CLT) may not kick-in.

I had 16 data points of platelet count collected over past 3-4 years, which is obviously too small. You need the i.i.d(identical independent) assumption and atleast 30 data points to apply CLT.

# What questions did I want to answer?
How likely is it that my platelet count indicates thrombocytopenia? 

Naturally, I decided to perform hypothesis test at level alpha = 5%. I applied the test over all the data-points obtained in the past 3-4 years: 16 data points.
Hypothesis test: In this case it is a one sample, one sided test, as below: 
- Null hypothesis: I do not have thrombocytopenia
- Alternate hypothesis: Reject the null hypothesis that I do not have thrombocytopenia

# About the data
The data published in the notebook is generated data, for privacy reasons. However the general approach to the problem remains the same.

# My approach

I could use the student's T test, if my data was approximately normal. So I plotted the QQ plot(code in the notebook):

![alt text](https://github.com/jatanpandya83/Small-dataset-statistics/blob/main/QQ-plot.png?raw=true)

The data suggests that its distibution is approximately normal.

Now that the data is approx. normal, and further on, making i.i.d assumption, I applied the Student's T test.

# Calculations
Calculate the test statistic (Tn)
![equation](https://bit.ly/3IvRqCN)
Where:
-Xn bar is the empirical mean
-Mu is the expectation under null hypothesis. This is obtained by averaging the range 140-400, .i.e (140+400)/2 = 270
-Sn hat is the sample variance
-Tn is the test statistic
![equation](https://bit.ly/344Rx9D)
Where:
-psi_alpha is the statistic where psi belongs to {0,1}
-Tn is the test statistic
-Q_alpha is the quantile at level alpha 
