# Individual project - Ana Paula Cipriano assessment
Reference article: Arce, A. N., David, T. I., Randall, E. L., Ramos Rodrigues, A., Colgan, T. J., Wurm, Y., & Gill, R. J. (2017). Impact of controlled neonicotinoid exposure on bumblebees in a realistic field setting. Journal of Applied Ecology, 54(4), 1199-1208.

# Background
Pesticide exposure is associated with insect pollinator declines, and it may have an impact on bees behaviour, health and colony development. The study exposed 20 bumblebee colonies to neonicotinoid clothianidin for 5 weeks, establishing a realistic field setting. I wanted to explore the articles' dataset containing the bee groups, such as eggs, pupae, larval, queen, worker, male, and gyne, developing a python project to implement some analysis and explore the impact of the treatment on these groups. This project can be applied to projects with a behavioral ecology scope, and I intend to use a similar methodology in my PhD project since I will study the effect of pesticides on social bees. Furthermore, adapting this project to similar data frames is interesting since pesticides are widely used and can affect bees' health and, consequently, their pollination services.

#Step 1
First of all, it is necessary to use the libraries and modules that are needed for running this code:
pandas (import pandas as pd): data manipulation and analysis
seaborn (import seaborn as sns): statistical data visualization
matplotlib.pyplot (import matplotlib.pyplot as plt): basic plotting library for data visualization
numpy (import numpy as np): numerical computing and array operations
scipy (from scipy import stats): scientific computing toolkit
scipy.stats (from scipy.stats import mannwhitneyu): statistical operations and hypothesis testing
statsmodels (import statsmodels.api as sm, import statsmodels.formula.api as smf): statistical models and hypothesis testing
sklearn.model_selection (from sklearn.model_selection import train_test_split): model selection tools, dataset splitting for training and testing
sklearn.linear_model (from sklearn.linear_model import LinearRegression): linear regression modeling
datetime (from datetime import datetime): date and time manipulation, introducing randomness

Next, we have to import the data that is available in this directory: Arce.et.al_census, the data frame is named as bee_complete: bees_complete = pd.read_csv("Arce.et.al_census.csv"). The data has several columns and we will select the ones that are interesting to our project by dropping the others.
![image](https://github.com/anapcipriano/assessment/assets/153204519/826b8dda-b078-4697-94b6-d3d3b9a30cb5)



