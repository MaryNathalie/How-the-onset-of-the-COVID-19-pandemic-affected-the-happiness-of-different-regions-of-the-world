# How the onset of the COVID-19 pandemic affected the happiness of different regions of the world

### 🔍 Overview

This project analyzes the impact of the COVID-19 pandemic on the collective happiness of individuals from different regions worldwide. Using data from the 2020-2021 World Happiness Report, this study examines variations in happiness scores across regions and over time, employing statistical methods such as one-way ANOVA, paired t-tests, Pearson correlation, and multiple linear regression.

🔗 [Research Paper](https://github.com/MaryNathalie/How-the-onset-of-the-COVID-19-pandemic-affected-the-happiness-of-different-regions-of-the-world/blob/main/documents/written_report.pdf)

### 🎯 Objectives

The following research questions were answered:
1. How does the happiness of each region vary in 2021 data compared to 2020 data and other regions?
2. What factors are associated with the change in the happiness of each region?
3. How well can the change in the happiness of each region be predicted by the selected factors?

### 🏭 Data Sources

Dataset: [World Happiness Report 2020 ](https://worldhappiness.report/ed/2020/)and [World Happiness Report 2021](https://worldhappiness.report/ed/2021/)  
Link: [Kaggle](https://www.kaggle.com/datasets/ajaypalsinghlo/world-happiness-report-2021)  

The report primarily sourced the data from the Gallup World Poll and incorporates it with data from other sources such as the World Risk Poll, the COVID Data Hub, and the Oxford COVID-19 Government Response Tracker for the 2021 report.
- The 2020 data is based on surveys and reports conducted in 2019 and early 2020.
- The 2021 data is based on surveys and reports conducted in 2020 and early 2021.

The number of samples in this study was determined by the availability of the data from the World Happiness Report, which includes data from countries grouped into 10 regions based on the regional indicator variable. The table below shows the number of samples or countries for each region varies.

<div align="center">

| Region                                 | No. of Samples (2020) | No. of Samples (2021) |
|----------------------------------------|----------------------|----------------------|
| Sub-Saharan Africa                     | 36                   | 14                   |
| Western Europe                         | 21                   | 19                   |
| Latin America & the Caribbean          | 20                   | 11                   |
| Middle East & North Africa             | 17                   | 11                   |
| Central and Eastern Europe             | 17                   | 16                   |
| Commonwealth of Independent States     | 12                   | 7                    |
| Southeast Asia                         | 9                    | 5                    |
| South Asia                             | 7                    | 2                    |
| East Asia                              | 6                    | 6                    |
| North American and ANZ                 | 4                    | 4                    |

</div>

The predictors involved are the following variables from the World Happiness Report:
- Freedom to make life choices: the extent to which people feel they have control over their own lives
- Generosity: average contribution of people to charity
- Healthy life expectancy: number of years a person can expect to live in good health
- Logged GDP per capita: logarithm of the gross domestic product per person, where higher values indicate higher income and economic development
- Perceptions of Corruption: the extent to which people think that corruption is widespread in their country
- Social Support: the degree to which people feel they have someone to count on in times of trouble

### 🏗 Methodology
1. One-way ANOVA: Tested whether happiness scores significantly differed across regions.
2. Paired t-tests: Analyzed whether happiness scores changed significantly from 2020 to 2021.
3. Pearson correlation: Measured relationships between happiness and six factors (GDP, social support, life expectancy, corruption perception, freedom of choice, and generosity).
4. Multiple linear regression: Modeled happiness scores based on predictor variables to quantify their impact.

### 📊 Key Insights
1. One-way ANOVA tests: Significant Regional Differences
- P-value < 0.05
- Null Hypothesis: There was no difference in the mean happiness score among the regions.
- Alternative Hypothersis: There was at least one region that had a different mean happiness score. 
<div align="center">

| Year                                 | F statistic    | P-value     |
|--------------------------------------|----------------|-------------|
| 2020                                 | 14.69          | 4.59e-14    |
| 2021                                 | 25.34          | 2.57e-25    |

</div>

2. Paired t-tests: Limited Impact of Time
- P-value < 0.05
- Null Hypothesis: The mean difference in the happiness score between the two years within each region was equal to zero
- Alternative Hypothersis: The mean difference in the happiness score between the two years within each region was equal to zero

<div align="center">

| Region                                 |  T statistic    | P-value     |
|----------------------------------------|-----------------|-------------|
| Sub-Saharan Africa                     | 1.06            | 0.31        |
| Western Europe                         | -1.52           | 0.15        |
| Latin America & the Caribbean          | -5.00           | 5.37e-4     |
| Middle East & North Africa             | -0.87           | 0.41        |
| Central and Eastern Europe             | 1.90            | 7.67e-2     |
| Commonwealth of Independent States     | 1.90            | 0.11        |
| Southeast Asia                         | -1.19           | 0.30        |
| South Asia                             | 4.38            | 0.14        |
| East Asia                              | 1.55            | 0.18        |
| North American and ANZ                 | -0.50           | 0.65        |

</div>

The only region that had a statistically significant mean happiness score difference, as shown above, was Latin America and the Caribbean region. As shown below, the mean happiness score difference for this region was 0.26, which means that the region had a slightly higher happiness score in 2021 than in 2020, contrary to what was expected for it to be due to the pandemic.

<p align="center">
<img src="https://github.com/MaryNathalie/How-the-onset-of-the-COVID-19-pandemic-affected-the-happiness-of-different-regions-of-the-world/blob/main/images/mean_happiness_score.png" width=50% height=50%>
</p> 

4. Top Influencing Factors: Pearson Correlation Coefficient
  - Strong Positive Correlation:
    - Logged GDP per capita (economic prosperity)
    - Social support (having someone to rely on)
    - Healthy life expectancy (long-term well-being)
  - Moderate Effects:
    - Freedom to make life choices (moderate positive impact)
    - Perceptions of corruption (moderate negative impact)
  - No Effect:
    - Generosity had no statistically significant correlation with happiness.

<div align="center">

| Factors                            |  Correlation Coefficient |
|------------------------------------|--------------------------|
| Freedom to make life choices       | 0.54                     | 
| Generosity                         | -0.061                   |
| Healthy life expectancy            | 0.74                     | 
| Log GDP per capita                 | 0.84                     | 
| Perceptions of corruption          | -0.51                    | 
| Social support                     | 0.77                     | 

</div>

4. Regression Analysis:  
A multiple linear regression model explained 75.4% of the variation in happiness scores, confirming the importance of economic and social factors. However, the model did not fully meet the assumption of normality of residuals, suggesting the need for further refinement.

<p align="center">
<img src="https://github.com/MaryNathalie/How-the-onset-of-the-COVID-19-pandemic-affected-the-happiness-of-different-regions-of-the-world/blob/main/images/linear_regression.png" width=50% height=50%>
</p> 

