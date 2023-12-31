# Individual project - Ana Paula Cipriano
Reference article: Arce, A. N., David, T. I., Randall, E. L., Ramos Rodrigues, A., Colgan, T. J., Wurm, Y., & Gill, R. J. (2017). Impact of controlled neonicotinoid exposure on bumblebees in a realistic field setting. Journal of Applied Ecology, 54(4), 1199-1208.

# Background
Pesticide exposure is associated with insect pollinator declines, and it may have an impact on bees' behaviour, health, and colony development. Arce et al. (2017) exposed 20 bumblebee colonies to neonicotinoid clothianidin for 5 weeks, establishing a realistic field setting. I wanted to explore the articles' dataset containing the bee groups, such as eggs, pupae, larval, queen, worker, male, and gyne, developing a Python project to implement some statistical analysis and explore the impact of the treatment on these groups. This project can be applied to studies with a behavioural ecology scope.

# Step 1
First of all, it is necessary to use the following libraries and modules in this code:

- pandas (import pandas as pd): data manipulation and analysis
- seaborn (import seaborn as sns): statistical data visualization
- matplotlib.pyplot (import matplotlib.pyplot as plt): basic plotting library for data visualization
- numpy (import numpy as np): numerical computing and array operations
- scipy (from scipy import stats): scientific computing toolkit
- scipy.stats (from scipy.stats import mannwhitneyu): statistical operations and hypothesis testing
- statsmodels (import statsmodels.api as sm, import statsmodels.formula.api as smf): statistical models and hypothesis testing
- sklearn.model_selection (from sklearn.model_selection import train_test_split): model selection tools, dataset splitting for training and testing
- sklearn.linear_model (from sklearn.linear_model import LinearRegression): linear regression modeling
- datetime (from datetime import datetime): date and time manipulation, introducing randomness

Next, import the data that is available in this directory: Arce.et.al_census.
- The data frame is named as bees_complete: bees_complete = pd.read_csv("Arce.et.al_census.csv"). The data has several columns and we will select the ones that are interesting to our project by dropping the others.
![image](https://github.com/anapcipriano/assessment/assets/153204519/826b8dda-b078-4697-94b6-d3d3b9a30cb5)

Brief explanation of the variables of interest: they represent the census of the colonies. 'workers_st' and 'pupae_st' are the data about these individuals at the beginning of the experiment, before the treatment or control weeks. The variables 'eggs,' 'pupae,' 'queen,' 'workers,' 'males,' 'gyne,' 'weight_increase,' and 'sum_larval_no' were collected after the 5 weeks of treatment/control. Each variable represents a group of bees within the colonies, and 'weight_increase' is the difference in the weight of the colonies at the start and in the end of the treatment.

# Step 2
Now with the data frame selected, it is interesting to explore the data distribution by plotting histograms to each column, and then boxplots to visualise the data in the control and treatment groups.

Next, create subgroups to analyse the data in the control and pesticide-treated groups, and perform descriptive statistics and correlation analyses. Then, check the data normality to proceed to the hypothesis tests.

# Step 3
The first analysis is the Mann-Whitney U test since some variables are non-normal. After performing the Mann-Whitney U test, implement a Generalized Linear Model (GLM), to explore the relationship between the response variables, the treatment, and the weight of the colonies at the beginning of the experiment. 
Finally, perform linear regressions to explore the relationship between the final weight of the colonies and the bumblebee groups within each one of them.

- In general, the Mann-Whitney U test results were not significant. However, the GLM analysis with the treatment plus the weight of the colonies indicates that the treatment may be associated with changes in the colony census for all of the bee groups, except the gynes. Lastly, the linear regression models did not have good scores; further analysis can be done with the dataset, especially incorporating foraging information to improve the understanding of the colonies' weight and bee census.

- This code can be used in the Jupiter Notebook.

# Examples
Exploring the data set:
- Histogram
  
![image](https://github.com/anapcipriano/assessment/assets/153204519/510bf837-1590-4684-a665-2ddc9d754998)
- Boxplot
  
![image](https://github.com/anapcipriano/assessment/assets/153204519/62b42251-daa2-4636-beb7-8e6057c401df)
- Descriptive statistics for the control subgroup
  
![image](https://github.com/anapcipriano/assessment/assets/153204519/fc1b83e4-4241-41e9-919c-1f450ce93697)
- Correlation analysis for the pesticide subgroup
  
![image](https://github.com/anapcipriano/assessment/assets/153204519/849bb13a-9c22-40e0-8fc7-dd3e41ba53c0)
- Correlation heatmap plotting for the pesticide subgroup
  
![image](https://github.com/anapcipriano/assessment/assets/153204519/870910e3-b9f8-44cc-bd4b-82a9fcb6d51b)

- Mann-Whitney U test

![image](https://github.com/anapcipriano/assessment/assets/153204519/9cf037de-e1db-4b8c-944c-0933534e885d)

- GLM

  ![image](https://github.com/anapcipriano/assessment/assets/153204519/2a36f4d6-b6c9-4e25-b813-3cfb4c0258f6)

- Regression analysis

 ![image](https://github.com/anapcipriano/assessment/assets/153204519/62486818-ee1b-4227-83c5-36e29ac1649f)
 

# Conclusion
Finally, the colonies' census may be impacted in colonies exposed to the pesticide treatment after 5 weeks, and this relationship can vary depending on the group. For example, gynes were affected differently compared to workers. Furthermore, other factors, such as bees' performance during foraging, might also influence the weight of the colonies, and this aspect can also be investigated for a general comprehension of the pesticide impacts on bees' health and nutrition.

This code can be used to explore datasets from ecological and behavioral projects. It implements statistical analysis to investigate the relationship of the control or pesticide groups on the condition of bumblebee colonies, but it can be adapted for projects with similar scopes.

 - **This project is open source, feel free to view, use, and contribute to it!!**



