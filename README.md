## Data Analysis Report: Exploring Potential Contributing Factors to Diabetes

### Introduction

Diabetes, also known as Diabetes mellitus, represents a significant global health challenge, with its prevalence steadily increasing. According to the International Diabetes Federation, approximately 537 million adults aged 20-79 were affected worldwide in 2021. In the United States, the Centers for Disease Control and Prevention's 2022 data indicate that over 133 million individuals are affected by either Diabetes (37.3 million) or prediabetes (96 million). This escalating burden highlights the importance of understanding the contributing factors.

Our analysis focused on the diabetes prediction dataset; we aimed to see if there are possible relationships between an individual diagnosed with Type 2 Diabetes and other behaviors, conditions, or demographics. Age, gender, body mass index (BMI), hypertension, heart disease, smoking history, HbA1c level, and blood glucose level were analyzed. \

Our exploratory data analysis aimed to address the following questions:

1. What are some of the trends between contributing factors?
2. How many diabetics do not have any of the other illnesses/behaviors?
3. Is there a combination of factors that tend to correlate with a diagnosis of Diabetes?


### Data Sources, Collection, and Preparation

The data for this exploratory analysis was sourced from the diabetes prediction dataset created by Mohammed Mustafa and accessed via Kaggle. This dataset was last updated in 2023 and is a collection of medical and demographic data from patients and their diabetes status (positive or negative). 

The dataset consists of 100,000 rows and nine variables, including gender, age, hypertension, heart disease, smoking history, body mass index (BMI), HbA1c level, blood glucose level, and diabetes status. The dataset was imported from the provided CSV file and stored in a new variable for analysis.

Data cleaning and preparation were done to ensure the integrity and reliability of the analysis. This involved:

- Replacing the values (0, 1) in the hypertension, heart disease, and diabetes status columns with more interpretable True/False values.
- Limiting the scope of the study to adults aged 21 years and above.
- Removing patients whose smoking history was labeled as "ever," as this could not be confirmed as a mistyping of "never." These instances constituted less than 5% of the dataset and were deemed potentially unreliable.
- Eliminating rows with null values in essential variables such as gender, hypertension, heart disease, smoking history, and diabetes status.
- Following the data cleaning and preparation steps, the dataset had 73,978 rows. Further filtering was then applied to isolate individuals who reported having Diabetes, resulting in a subset of 7,913 individuals. 


### Data Analysis Methods

Summary statistics, including mean, median, and standard deviation, were calculated for continuous variables such as age, BMI, HbA1c, and blood glucose. For categorical variables like gender, smoking history, hypertension, heart disease, and BMI categories, percentages were used to show the distribution of each category within the sample.

Additionally, visualization techniques such as bar charts were employed to compare the percentage of individuals diagnosed with Diabetes across different categories, such as BMI and age groups, as well as heart disease and hypertension status. Scatter plots were utilized to visualize the relationship between age and BMI. Furthermore, box plots were employed to visualize the distribution of diabetes status across different variables.


### Findings

#### Analysis of Contributing Factors and Trends (Question #1)

**Gender and Age:**
Among individuals in the dataset, approximately one-tenth (10.7%) reported having Diabetes. Of those with Diabetes:
a slightly higher proportion (53%) identified as female, and
47% identified as male.

The average age for individuals with Diabetes was 61.7 years (median = 63.0 and SD = 13.55), while the average age for non-diabetic individuals was 49.43 years (median = 48.0 and SD = 16.87).

The majority (88%) of those who reported having Diabetes were aged 45 years and older. The remaining age distribution among those with Diabetes are:
7.8 % were between 35 and 44 years old.
3.4 % were between 25 and 34 years old.
0.47 % were below 24 years old.

**Hypertension and Heart Disease:**
Among individuals with Diabetes:
a quarter (25%) reported having hypertension, and
15% reported having heart disease.

**Smoking History:**
Among those with Diabetes, a significant amount (42%) reported never smoking, whereas:
20% were former smokers.
12% were current smokers.
27% had no reported smoking history (18%) or current status (9%).

**Body Mass Index (BMI):**
On average, individuals with Diabetes had a BMI of 32.12 kg/m² (median = 30.06 and SD = 7.54), compared to 28.39 (median = 27.3 and SD = 5.72) for non-diabetics.

The majority of those with Diabetes were overweight (40%) and obese (50%). The other BMI distribution among individuals with Diabetes are:
9% were of healthy weight.
1% were underweight.

**Blood glucose and HbA1c levels:**
The average HgA1c level for those with Diabetes was 6.9% (median = 6.6 and SD = 1.08), whereas the average HgA1c level for non-diabetics was 5.4 % (median = 5.8 and SD = 0.97). According to the CDC (2022), hemoglobin A1C (HbA1c) levels are normally below 5.7% for non-diabetics, between 5.7% and 6.4% for prediabetics and 6.5% or higher for those with Diabetes.

The average blood glucose level was 194.4mg/dL (median of 160 and SD= 58.69) for Diabetics and 132 mg/dL (median = 140 and SD = 34.2) for non-diabetics.

#### Prevalence of Diabetes without Comorbidities (Question #2)

In evaluating the comorbidities (illnesses) among individuals who reported having Diabetes, we observe varying prevalence rates of heart disease and hypertension. The majority (65%) of individuals diagnosed with Diabetes in the dataset do not have heart disease or hypertension. Whereas:

21% of individuals diagnosed with Diabetes in the dataset have hypertension but no heart disease.

11% of individuals diagnosed with Diabetes in the dataset have heart disease but no hypertension.

Only 4% of individuals diagnosed with Diabetes in the dataset have both hypertension and heart disease.


#### Exploring Correlations with Diabetic Diagnosis (Question #3)

In examining the correlations between various demographic and health factors for those individuals who reported having Diabetes, we found that the majority (80%) of individuals diagnosed with Diabetes in this dataset are aged 45 or older and have a BMI of 25 or higher. While: 

10% of individuals diagnosed with Diabetes in the dataset are under the age of 45 and have a BMI of 25 or higher.

9% of individuals diagnosed with Diabetes in the dataset are aged 45 or older but have a BMI under 25.

Only 1% of individuals diagnosed with Diabetes are under the age of 45 and have a BMI under 25.

### Limitations

While our analysis provides insights into the potential contributing factors to Diabetes, it is important to acknowledge several limitations that may affect the interpretation and generalizability of our findings. Firstly, the classification of Diabetes types (Type 1, Type 2, or Gestational Diabetes) was not provided in the dataset. Without this information, our analysis lacks specificity regarding the different subtypes of Diabetes and their respective risk factors.

Secondly, the dataset did not specify the blood glucose level measurement type (e.g., fasting or random blood glucose tests). This omission limits our ability to differentiate between fasting and non-fasting blood glucose levels. Thirdly, some individuals were excluded from the analysis due to discrepancies in their smoking history labeling. Specifically, individuals labeled "ever" smokers were removed from the dataset; this exclusion may introduce a potential bias. Additionally, the uncertainty surrounding the accuracy of the labeling (whether "ever" was a mistyping of "never") highlights a limitation in the quality and reliability of the data.


### Implications

An understanding of the demographic patterns associated with diabetes diagnosis, such as age and gender, allows for targeted interventions that are tailored to specific populations. For example, interventions aimed at preventing and managing Diabetes may prioritize older age groups (45 years and older), given their higher prevalence.

Given the association between obesity (indicated by BMI) and Diabetes, interventions focusing on weight management and lifestyle modifications are vital. Emphasizing the importance of healthy dietary habits and regular physical activity can help mitigate the risk of Diabetes and its associated complications.

Overall, the implications of these findings highlight the need for comprehensive, multifaceted approaches to diabetes prevention, management, and intervention strategies that consider the diverse factors influencing diabetes risk and outcomes.



### Conclusion

We found that the majority (88%) of those who reported having Diabetes were 45 years and older. A slightly higher proportion (53%) of females reported having Diabetes. A substantial portion (42%) of individuals with Diabetes report having never smoked, and 90% of those who reported having Diabetes were overweight or obese.

This analysis highlights the complex relationship between demographic factors, lifestyle behaviors, and the prevalence of Diabetes. Understanding these correlations is crucial for informing targeted interventions aimed at both preventing and managing Diabetes effectively. The next steps should involve developing and implementing comprehensive health promotion strategies, including targeted education campaigns, smoking cessation programs, behavior change interventions, and obesity management initiatives (Wu, Ding, Tanaka, & Zhang, 2014).

Moreover, it is imperative to investigate additional contributing factors such as alcohol consumption, genetics, family history, prediabetes, race, and ethnicity. Further research into these variables' complex relationship and long-term impact on diabetes outcomes is vital. This exploratory data analysis will inform evidence-based interventions and policies aimed at alleviating the burden of Diabetes on both individuals and healthcare systems.


### References

1. Centers for Disease Control and Prevention (2022). Diabetes basics. https://www.cdc. gov/diabetes/basics/index.html

2. Centers for Disease Control and Prevention (2022). All About Your A1C. Retrieved from https://www.cdc.gov/diabetes/managing/managing-blood-sugar/a1c.html
 
3. International Diabetes Federation (2024). https://idf.org/about-diabetes/diabetes-facts-figures/

4. Mohammed Mustafa (2023). Diabetes prediction dataset: A comprehensive dataset for predicting Diabetes with medical and demographic data. https://www.kaggle.com/datasets/iammustafatz/diabetes-prediction-dataset/data

5. Wu Y, Ding Y, Tanaka Y, & Zhang W. (2014). Risk factors contributing to type 2 diabetes and recent advances in the treatment and prevention. International J Medical Sciences 6;11(11):1185-200. doi: 10.7150/ijms.10001. PMID: 25249787; PMCID: PMC4166864.

