# Analyzing the Leading Causes of Death in United Stated
#### By Pratyush Painuly, Mohammad Shiwani and Brandon Valmont



## About - 
CDC releases Mortality data set for each death occured in United States annually, under the National Vital Statistics Systems. This mortality dataset gives insight into every death in the country, including the cause of death, location(State), Time and scientific description of the respective cause. Data.cdc.gov takes that data to present the age-adjusted death rates for the 10 leading causes of death in the United States beginning in 1999, which we will be analysing for this project. Our goal is to look into the pattern of death distribution across the country/states and explore the complex circumstances which dominate this dataset, hence get a better understanding of leading causes around the country. We also aim to look at this data with a global stand point and analyse how the mortality rates of countries with similar size, per capita and GDP match with United States. At a more micro level and local level, the group want to understand what the leading causes of death are in Texas and what the trends over time are for the leading causes in Texas. The group also aims to investigate what could impact those age adjuste death rate trends.  

## Dataset Overview
The [dataset](https://data.cdc.gov/NCHS/NCHS-Leading-Causes-of-Death-United-States/bi63-dtpu) was obtained in .csv format from Data.CDC.gov under the publisher National Center for Health Statistics. The information in the dataset compiles the death certificates filed in each state and presents it as a summary for each year by state and cause of death. Age-adjusted death rates (per 100,000 population) are based on the 2000 U.S. standard population. The source dataset has 10,296 rows and 6 columns (Year, 113-Cause,Cause Name,State, Deaths and Age Adjusted Deaths). We downloaded the dataset directly from the website and imported as a dataframe in jupyter notebook before beginning our analysis. The data for unemployment rates in TX, CA, and NY came form Fred (https://fred.stlouisfed.org/series/TXUR) in the form of a .csv file.  The data was included in jupyter notebooks was a dataframe and merged with a previous dataframe to be analyzed.  

## Questions regarding the Dataset - 
We discussed in details various ways to approach the dataset. We divided our approach into sections, each one aiming to look at the data in a different perspective. 

### Section 1 - Causes of Death, Nation Wide/Global Insights
We looked at the dataset in a general countrywise view. We looked at what have been the leading causes throughout the timeframe and how have they changed. How can we look at the same questions for each state. Now, how does the number of deaths compare with the rest of the world? Espcially to "similar" countries with respect to size, GDP and wealth(or poverty). How does United States rank with other countries in mortality rate and what is the progression of time?

### Section 2 - Add Title and summary (Mohammad)
<ADD SUMMARY>

### Section 3 Leading Causes of Death in Texas  (Brandon)
The original data was taken from the CDC included all states and the District of Columbia.  In this section of the project, the group wanted to answer what the leading causes of death were on a micro level.  The discision was made to analyze Texas since that state would satisfy slicing the data to a micro level and would also be the state local to Rice University.  After drilling down into the original dataset and filtering for Texas, it was determined that heart disease, cancer, and stroke were the three leading causes of death respectively.  

### Section 4 Leading Causes' Trends (Brandon)
After determing heart disease, cancer, and stroke were the top 3 leading causes of death in Texas respectively, the next question to answer was how does the age adjusted death rates for these leading causes of death trend over time relative to the data set that was available from the CDC (1999-2000).  Overall, it was found that the age adjusted death rates for heart disease, cancer, and stroke were decreasing starting from 1999.  However, 2015 saw the age adjusted death rate tick up for heart disease and stroke while the age adjusted death rate for cancer held steady but did not decline.  

### Section 5 Unemployment Rates and Age Adjusted Death Rates (Brandon)
The age adjusted death rates' trends in Texas seemed to change in 2015 along with the total amounts of deats in 2015 relative to years approximate to 2015.  Since Texas has many oil and gas jobs and a major downturn in the industry began after Thanksgiving of 2014, a hypothesis was made that age adjusted death rates for Texas increased when the unemployment rate increased.  Unemployment data for TX was found and merged into a previous dataframe.  The leading causes of death over time was plotted with the Texas unemployment rate trend over time and overall it did not visually seem to correlate with the age adjusted death rate.  California's, New York's, and Texas' unemployment trends were then plotted with California's, New York's, and Texas' age adjusted deat rates by all causes and again, a trend could not be conslusively visualized.  In fact, during 2010, each state had its highest unemployment rates and the age adjusted death rates continued to decrease.  Texas had the lowest unemployment rates of the states compared in the dataset but also had the higest age adjuste death rates of the states in the comparison.  It is interesting that in 2015, Texas' uneployment rate started to tick up wile California and New York's unemployment rate continued to decrease.  Pearson's correlation coefficient was calculated to be
-0.241 Texas's age adjusted death rate and its unemployment rates.  The unemployment rates of each state seemed highly correlated as calculted with Pearson's coefficient using pearsonr from scipy.stats.

  What are the leading causes of Death in Texas - 
  ![Texas Leading Causes](Charts/texleadingcauses.png)












## Research Questions and Analysis




## Conclusion
  * Heart Diseases, Cancer and Stroke are the three leading causes of Death in United States.
  * Suicide rates and Alzheimer's Disease rates are on the rise
  * New York has the highest distribution of a leading cause for state(Heart Diseases in this case).
  * Texas had lower unemployment rates compared to California and New York, but a higher age-adjusted death rate overall.
  * For Stroke and Heart Diseases, there was a spike in Texas. We investigated if that had a correlation with the Major Oil and Gas Downturn on 2015 and consequently unemployment rates for Texas.
  * Since 1985, United States has the worst Mortality rate(per 100000 people) when compared to other countries of "similar" size and wealth.
  * We formed our null hypothesis that Countries of similar wealth and size will have a similar mortality rate. After performing ANOVA test on the dataa seat featuring 7 countries, the null hypothesis was rejected. However, when we take a group of 4 countries and perform th same test, the dataset is significant. 
  
