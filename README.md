# How the onset of the COVID-19 pandemic affected the happiness of different regions of the world

### Overview

This project analyzes the impact of the COVID-19 pandemic on the collective happiness of individuals from different regions worldwide. Using data from the 2020-2021 World Happiness Report, this study examines variations in happiness scores across regions and over time, employing statistical methods such as one-way ANOVA, paired t-tests, Pearson correlation, and multiple linear regression.

### Statistical Methods Used
- One-way ANOVA: Tested whether happiness scores significantly differed across regions.
- Paired t-tests: Analyzed whether happiness scores changed significantly from 2020 to 2021.
- Pearson correlation: Measured relationships between happiness and six factors (GDP, social support, life expectancy, corruption perception, freedom of choice, and generosity).
- Multiple linear regression: Modeled happiness scores based on predictor variables to quantify their impact.

### Key Insights
- Significant Regional Differences: One-way ANOVA tests confirmed that happiness scores significantly varied across different regions in both 2020 and 2021.
- Limited Impact of Time: Paired t-tests showed that, except for Latin America and the Caribbean, happiness scores did not significantly change from 2020 to 2021, indicating that region played a bigger role than the pandemic’s onset in determining happiness.
- Top Influencing Factors:
  - Strong Positive Correlation:
    - Logged GDP per capita (economic prosperity)
    - Social support (having someone to rely on)
    - Healthy life expectancy (long-term well-being)
  - Moderate Effects:
    - Freedom to make life choices (moderate positive impact)
    - Perceptions of corruption (moderate negative impact)
  - No Effect:
    - Generosity had no statistically significant correlation with happiness.
- Regression Analysis: A multiple linear regression model explained 75.4% of the variation in happiness scores, confirming the importance of economic and social factors. However, the model did not fully meet the assumption of normality of residuals, suggesting the need for further refinement.

### Data Sources

World Happiness Report 2021 (Kaggle)
World Happiness Report 2020
