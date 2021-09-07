# Project 2 - Ames Housing Data and Kaggle Challenge

### Catherine Ang, DSIF-1

### Introduction
**J.S. Consultancy LLP** ("company") is a real estate consulting firm in the United States (the U.S.) that specialises in the provision of independent market research and consulting services related to the real estate industry in the U.S.
**Iowa Real Estate ("IRE")** is the largest real estate agency in the state of Iowa, that helps homeowners identify potential buyers for their houses. 


### Problem Statement
IRE has achieved tremendous success and commanded a significant presence in the real estate industry across multiple cities in Iowa,  except for Ames. It plans to expand its real estate agency services into Ames, a city in Iowa, which currently encompasses several smaller real estate agencies.

IRE has engaged J.S. Consultancy LLP to conduct a thorough market research of the real estate industry in Ames to aid in its advancement into Ames. Some of the questions that IRE have include:
- To predict the **sale price of the houses in Ames**;
- To identify the **top 5 neighborhoods in Ames** that command high sale price of housing;
- To identify the **top 2 features that would lead to an increase in the sale price** of the house.


### Executive Summary


INTRODUCTION

To predict the housing sale prices in Ames, Iowa, the Ames Housing Data Set was used. This dataset contains information of features used in the computation of the value of individual residential properties sold in Ames, Iowa from 2006 to 2010, together with the actual sale prices of the properties. By analysing the actual sale prices of the houses, this allows for a comparison of the sale prices over the years, and identification of features that may have a stronger impact on the sale prices. 


METHODOLOGY

A data science workflow was introduced to conduct this analysis. Firstly, the problem statement was defined — IRE is looking to expand its real estate agency services into Ames, Iowa, and has engaged J.S. Consultancy to conduct a thorough market research of the real estate industry in Ames to aid in its advancement into Ames. Next, the appropriate datasets were imported to a Pandas DataFrame, which included the training and test data sets of around 2,930 properities in Ames, Iowa, across 2006 to 2010. Thereafter, an exploratory data analysis was conducted to identify the general trends of the variables, as well as patterns in the missing values. Both datasets were merged into a singular DataFrame for ease of cleaning; missing values were handled differently, depending on whether they belong to categorical or numerical variables, and whether the missing values represent the lack of the particular attribute. New features were then created, while most categorical variables were mapped to an integer value wherever feasible (otherwise float), so that a correlation analysis could be conducted across all variables. 

All statistical findings were then utilised to perform data visualisation, which included the use of heat map, histogram, line plots, subplots and scatterplots. Concurrently, descriptive and inferential statistical analysis was conducted to identify trends that appeared in the data. External research about the housing prices in Ames was also conducted, to support observations made. Thereafter, regression techniques were employed to predict the housing sale prices. This was further enhanced by feature engineering to identify new features that could be included to boost the performance of the model, as well as regularization and grid search for hyperparameters. Eventually, the Elastic Net (Regularization) Regression model was selected to predict the actual housing sale prices of the test dataset, as well as to identify the top 5 neighborhoods that command the highest sales prices, and top 2 features that would increase the sale prices of the houses. The recommendations for IRE were compiled. 


FINDINGS

When analysing the datasets, various insights about the Ames Housing Data Set were obtained. The following consists of the most significant findings:
* The top 3 variables that have the highest positive correlation with housing sale prices (based on training data set) are: Overall quality of house (+0.803462), Neighborhood (+0.720388), and Above grade (ground) living area in square feet (+0.719463). 
* The top 3 variables that have the highest negative correlation with housing sale prices (based on training data set) are: Age of the house (-0.572441), Age of the garage (-0.556550) and Age of remodelling/addition (-0.552218) when the house was sold. 


---

### Data Dictionary

The dataset consists of information for around 2,930 properties in Ames, Iowa, with around 77 variables used to predict the pricing of these properties. These variables can be classified into the following categories: 
- Categorical & nominal: *non-numerical, lacks clear order, e.g. neighorhood, type of heating*
- Categorical & ordinal: *non-numerical, but has a clear order, e.g. overall material and finish quality, overall condition rating*
- Non-categorical & discrete: *numerical, with intervals, e.g. year house was sold, year garage was built*
- Non-categorical & continuous: *numerical, and able to take any values, e.g. above grade (ground) living area square feet*

The data dictionary can be found [here](http://jse.amstat.org/v19n3/decock/DataDocumentation.txt).


---

### External Research

Ames is a town in Iowa, with a population of around 66,000.  It has been rated as one of the top places to live in Iowa, where it provides residents with the vibe of staying in an urban suburban - great mix of city and rural. At present, more than half of the residents rent their homes in Ames.
* Source: [Niche (Jan 2021)](https://www.niche.com/places-to-live/ames-story-ia/)

Following the burst of the dotcom bubble, the U.S. Federal Reserve reduced interest rates to tackle recession in the early 2000s. Policies that encouraged home ownership were introduced, alongside financial products that increased the liquidity of assets in the real estate industry. Thus, more investors shifted their focus into the business of buying and selling houses, away from the stock market. This resulted in a spike in number of houses built after 2003. 

In addition, with banks offering lower interest rates and relaxing their lending requirements, this prompted a home-buying frenzy which resulted in higher housing sale prices, as speculators would buy and sell houses for profits within a short period of time. The number of houses sold from 2006 to 2007 increased, alongside increasing housing sale prices. 

However, as the stock market began to recover and interest rates started to rise from 2006-2007 onwards, investors stopped purchasing houses as the risk premium was too high and beyond control. This resulted in the decline of housing prices from 2007 to 2009, with investors selling their mortgage-backed securities, while others defaulted on their mortgage payments; this gave rise to the burst of the housing bubble. 
* Source: [Investopedia (Dec 2020)](https://www.investopedia.com/terms/h/housing_bubble.asp)


---

### Conclusion and Recommendations

#### Prediction of sale prices of houses in Ames

In predicting the sale prices of the houses in Ames (using the test dataset) for IRE's review, the following information is derived derived:
- Mean Sale Price: USD 179,059
- Median Sale Price: USD 158,494
- Minimum Sale Price: USD 50,556
- Maximum Sale Price: USD: 877,683

#### Identification of top 5 neighborhoods in Ames that command high sale prices of housing

By computing the mean Sale Price for each Neighborhood, we observe that the top 5 neighborhoods include: 
* Northridge - USD 362,221
* Northridge Heights - USD 319,262
* Stone Brook - USD 291,626
* Timber - USD 268,284
* Veenker - USD 248,203

On the other hand, when computing the mean Sale Price per Total Area (in square feet), we observe that the top 5 neighborhoods include:  
* Northridge - USD 73.46/square feet
* Northridge Heights - USD 73.46/square feet
* Stone Brook - USD 70.49/square feet
* Timber - USD 69.15/square feet
* Greens - USD 67.32/square feet 
    
To earn higher profit margins from the sale of houses, we would recommend that IRE focuses on houses in the neighborhoods of **Northridge, Northridge Heights, Stone Brook, Timber and Veenker**. As Ames expands its northern area, newer neighborhoods such as Northridge Heights will benefit from the construction of modern houses, thus commanding higher sale prices. 


#### Identification of top 2 features that would lead to an increase in sale price of the houses

The top 2 features that would result in the highest positive change in sale prices of houses are:
* **Overall material and finish quality** - a house that has an Overall Qual score that is one rank above will allow the mean sale price to increase by USD 13,124, all else being equal.
    - What this means is that IRE should consider the following aspects when identifying houses to invest in: 
        - Materials used should be highly decorative and of structural quality; 
        - Materials used should be designed for maximum durability, so that they can handle the effects of climate and environmental changes (i.e. use of stainless steel doors for an outdoor kitchen). 
        - Colours (i.e. light vs dark color scheme) and finishes (i.e. glossy vs matte surfaces) can affect the overall ambience of the house.
        - Source: [CWI.Design (2021)](https://www.creativewallcoverings.com/choosing-materials-and-finishes-important-aspects-to-consider/)
    
* **Overall condition rating** - a house that has an Overall Cond score that is one rank above will allow the mean sale price to increase by USD 7,396, all else being equal.
    - What this means is that IRE should consider the following aspects when identifying houses to invest in: 
         - Any repair works for damages to structures, fixtures should be carried out promptly;
         - Interior refinement works are carried out such that the houses come across as though they have been individually designed; 
         - Immense amount of attention is given to the intricate details (both the interior and exterior), such that the house can be characterised by its excellent quality of workmanship. 
         - Source: [Spartanburg County (2021)](https://www.spartanburgcounty.org/DocumentCenter/View/291/Physical-Condition-Codes?bidId=)

---

### Datasets

The sources of datasets used in this analysis: 
* [`train.csv`](./datasets/train.csv): Ames Housing Data Set - Training set 
* [`test.csv`](./datasets/test.csv): Ames Housing Data Set - Test set 