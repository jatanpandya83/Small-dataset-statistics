# Small-dataset-statistics
Statistical analysis of small dataset
# About Platelet Count (Source: Quest Diagnostics)
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

Naturally, I decided to perform hypothesis test at level alpha = 10%. I applied the test in two situations:

- Over all the data-points obtained in the past 3-4 years: 16 data points
- Last one year: 5 data points

Hypothesis test: In this case it is a one sample, one sided test, as below: 
- Null hypothesis: I have no medical condition
- Alternate hypothesis: I have thrombocytopenia


# My approach

I could use the student's T test, if my data was approximately normal. Below is the QQ plot:


The data suggests that its distibution is approximately normal.

Now that the data is approx. normal, and further on, making i.i.d assumption, I applied the Student's T test.

# Calculations

Peforming the test over all the data points obtained in past 3-4 years:

Performing the test over the data points obtained in past 1 year:

# Concluding remarks
Be curious. Be inquistive. Keep learning!

Kudos to the Statistics and data science certification from MiTx on edX (https://www.edx.org/micromasters/mitx-statistics-and-data-science), where I learnt many of these concepts and techniques.





