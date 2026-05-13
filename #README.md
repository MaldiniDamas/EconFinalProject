Does Place Shape Economic Opportunity?
An Empirical Analysis Using County‑Level Mobility Data**

Econ 565 — Final Project
Author: Maldini Damas
1. Introduction
This project examines the extent to which place influences intergenerational economic mobility in the United States. Building on the framework established by Chetty, Hendren, and Katz (2018), the analysis evaluates whether county‑level characteristics—such as poverty, educational attainment, family structure, population density, and regional context—account for observed variation in upward mobility for children from low‑income households.

A central aim of the project is to determine whether racial composition remains a significant correlate of mobility outcomes after controlling for structural socioeconomic factors. This approach allows for an assessment of whether racial disparities in opportunity reflect differences in observable county characteristics or whether they persist even after adjusting for these factors.

2. Data
The analysis draws on two primary sources:

2.1 Opportunity Atlas
mobility_rank_p25: The national percentile rank in adult income for children born to parents at the 25th percentile of the national income distribution.

Data are aggregated at the county level.

2.2 Socioeconomic and Demographic Indicators
Collected from publicly available county‑level datasets:

Poverty rate

College attainment share

Single‑parent household share

Log population density

Census region

Racial composition (share Black, share White)

These variables capture structural features of local environments that prior literature identifies as determinants of mobility.

3. Methodology
3.1 Baseline Regression Model
The empirical strategy begins with an OLS regression of mobility outcomes on socioeconomic and demographic characteristics:
mobility_rank_p25𝑖 = 𝛽0+ 𝛽1poverty𝑖+ 𝛽2college𝑖+ 𝛽3singleparent𝑖+ 𝛽4log(density𝑖)+ 𝛽5region𝑖 + 𝜖𝑖
This specification isolates the portion of mobility explained by structural county characteristics.

3.2 Opportunity Score (Residual Analysis)
To measure the extent to which counties over‑ or under‑perform relative to expectations, the project constructs an Opportunity Score:

Opportunity Score
𝑖 = Actual Mobility 𝑖 − Predicted Mobility 𝑖
A positive score indicates that a county provides more upward mobility than predicted by its socioeconomic profile; a negative score indicates under‑performance.

This residual‑based measure is widely used in applied microeconomics to capture unobserved institutional, social, or structural factors.

4. Results
4.1 Model Fit and Predictive Performance
The regression model explains a substantial share of variation in mobility, consistent with prior literature. However, large residuals remain, indicating that many counties significantly over‑ or under‑perform relative to predicted mobility.

4.2 Opportunity Score Patterns
Analysis of the Opportunity Score reveals:

Counties with similar socioeconomic profiles exhibit markedly different mobility outcomes.

Over‑performing counties tend to cluster in specific regions, suggesting the presence of institutional or social factors not captured by standard covariates.

Racial composition remains strongly associated with the Opportunity Score.
High‑Black‑share counties systematically under‑perform relative to predicted mobility, even after controlling for poverty, education, family structure, density, and region.

These findings suggest that structural racial disparities in opportunity persist beyond what can be explained by observable socioeconomic characteristics.

5. Repository Contents
Does_Place_Shape_Economic_Opportunity_Maldini_Damas.Rmd  
Contains the full analysis, including:

Data cleaning and preparation

Regression estimation

Residual‑based Opportunity Score construction

Visualizations and diagnostic plots

Interpretation of results

Additional knitted outputs (HTML/PDF) may be added for ease of review.

6. Reproducibility
To reproduce the analysis:

Open the .Rmd file in RStudio

Install required packages:

r
install.packages(c("tidyverse", "broom", "ggplot2"))
Knit the document to HTML or PDF.

All code is self‑contained within the R Markdown file.

7. Conclusion
The results provide evidence that place plays a significant role in shaping economic opportunity. While socioeconomic characteristics explain a substantial portion of mobility variation, persistent residual differences—particularly those correlated with racial composition—suggest the presence of deeper structural inequities. These findings align with the broader literature emphasizing the importance of local institutions, social capital, and historical context in shaping intergenerational mobility.

8. References
Chetty, Raj, Nathaniel Hendren, and Lawrence Katz. The Effects of Exposure to Better Neighborhoods on Children: New Evidence from the Moving to Opportunity Experiment. American Economic Review, 2016.

Chetty, Raj, et al. The Opportunity Atlas: Mapping the Childhood Roots of Social Mobility. Opportunity Insights, 2018.
