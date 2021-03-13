
Project 1: Green Cities 
Summary

This project investigated whether cities should invest in becoming more “green.” 

Hypothesis:
Green cities positively influence the standard of living for residents compared to cities that are not  green (“nongreen cities”).

Questions & Data Exploration

Specifically, our questions are:

1)	Does living in a green city lead to lower poverty rates than in a nongreen city?
2)	Does living in a green city lead to higher life expectancies than living in a nongreen city?


We asked these questions because we wanted to prove that cities that invest in and prioritize sustainable practices will improve the standard of living of their residents. These cities will also be more attractive to those who are seeking to relocate.


What is a green city?
We had to first find a list of green cities for the U.S. that included appropriate indicators for classifying the cities as such. After a Google search, we decided to use the “Greenest Cities in America”  list from WalletHub.com (compiled in 2019). WalletHub is an online financial website that provides free credit scores and other credit card and banking services. WalletHub compared the 100 cities in the U.S. with the highest populations by using “28 relevant metrics” such as air quality index, water quality, accessibility of jobs by public transit, and share of electricity from renewable sources. For more information on how their list was compiled, please see: https://wallethub.com/edu/most-least-green-cities/16246.

According to the WalletHub list, San Francisco was the most green city (at # 1 on the list) and Baton Rouge was the least green city (at #100 on the list). They also happened to be located in two different geographic areas – one in the West of the U.S. and one in the South. We decided to also compare them with another city that was not on the Greenest Cities list at all and that was in another geographic area. In this way, we chose Pittsburgh, PA which is in the Northeast of the U.S.

What standards of living or quality of life indicators should we measure?
We next researched standards of living and quality of life indicators to determine what datasets to use. We looked at a number of sources such as the Statistics Explained website (Statistics Explained (europa.eu) and Investopedia.com.  We chose to focus on standard of living rather than quality of life because the indicators are more quantifiable. We originally sought to investigate 3-4 indicators including education and median household income. However, datasets for education that included the necessary data were difficult to find and it was also difficult to find data for median household income over enough  years and broken down by county. Due to time constraints and availability of data, we chose to investigate two indicators only: life expectancy (health indicator) and poverty rate (economic indicator).

We chose to look at the data filtered by county within each of the 3 metropolitan areas and for a period of 6 years so that we had enough data to analyze. We used data from 2010 – 2015 because while we wanted to investigate more recent data, 2015 was the latest year that we could find all of the data by county for each indicator, at least in the time that was available for this project. Baton Rouge has a total of 9 counties, Pittsburgh has 5, and San Francisco has 9. 

Data Sources

We learned from the data gathering stage that this step can be quite time consuming, that you may need to adjust your requirements, and that the Census Bureau provides one of the best sources for this type of standard of living data. While we tried to access data for some type of education indicator such as literacy rate or school ratings, we were unable to find reliable data broken down by county or city. We were excited when we found a source that seemed to have the appropriate schools data but when we tried to procure the API, we were told by the site that they are no longer providing APIs. 

Our final data sources were: the U.S. Census website (https://www.census.gov/programs-surveys/saipe/data) for income and poverty rate data and the Centers for Disease Control and Prevention (https://data.cdc.gov/NCHS/U-S-Life-Expectancy-at-Birth-by-State-and-
Census-T/5h56-n989) for life expectancy data. After attempting to use APIs to collect the data, we ran into issues with getting the files to work and so imported csv files instead. We had to search through many pages of the websites to find the exact data – especially because we wanted to see county data and not just state or national data. Most of the census csv files had numerous columns and rows and so it took time to examine them and see what data they contained.


Data Cleanup 

After finding the appropriate data, we were ready to clean the data using Pandas with the goal of having the following final datasets:


Poverty Rate:  
One dataframe for each of the three metropolitan areas, filtered by counties, with corresponding poverty rates for 2010-2015. The column that we used from the census csv file was “All Ages in Poverty Percent.” 

Life Expectancy:
One dataframe for each of the three metropolitan areas, filtered by counties, with corresponding life expectancy rate for 2010-2015. The column that we used from the CDC csv file was “Median Household Income in Dollars.”

We dropped null values and deleted extraneous columns. Once we had these cleaned dataframes, we were able to perform calculations to find the poverty rate and the life expectancy (cumulative from adding amounts from all counties in each area) for each of the three areas. We also compared them to the averages for the U.S. One lesson learned during this stage is to make sure to have constant communication between teammates. For example, it is important to make sure that there is no double work being done and that everyone is working on the most up-to-date files (for example, if one teammate works on the first part of the cleaning and a second teammate works on finishing the cleaning). This is why using the branches, pull requests, and merging functions of GitHub is useful.


Data Analysis


We organized the Jupyter notebooks with the following folders: Analysis, Output, and Resources. Once we had the final cleaned data files, we were ready to plot the data. We started by saving the dataframes from the previous stage into a single csv file so that we could use it for all of the plots that we wanted to complete. The dependencies that we used were: NumPy, Pandas, Matplotlib, SciPy.stats, and Seaborn. We then created bar charts and scatter plots and performed a linear regression analysis. Please see below for the linear regression comparing poverty rate and life expectancy for San Francisco.



Insights and Problems 

We were surprised about the disparity in poverty rates between different counties in Baton Rouge. There was a large difference between the county with the highest poverty rate and the one with the lowest. The disparity was over 12% while most counties were only  4-5% different. The biggest issues that arose were using the right dependencies and making sure that we did the coding is such a way to make the required data manipulation possible. 


Discussion

We thought there would be a significant difference for standards of living in green cities compared to nongreen cities. What we found, however, was that we could not tell from just this data from the bar charts and box plots. We performed an analysis of variance test (ANOVA) instead of another type of statistical test because we were studying 3 cities rather than just 2 and because the bar charts were not telling us the required information.  The differences were too small to see using bar charts alone. However, through the ANOVA, with 95% confidence, we were able to determine that we are unable to reject the null hypothesis. We did not do a chi square test because we didn’t find enough information from doing the ANOVA. What’s more, linear regression models showed that there was no correlation between average life expectancy and poverty rates in any of the areas.


We can say that San Francisco life expectancy was higher than Baton Rouge, Pittsburgh, and U.S. during 2010-2015. We can also say that the poverty rate in Baton Rouge was higher than in the other cities. The differences were not significant enough to say that being a green city influences these factors though.


Conclusions

We would ideally study at least 10 additional green cities compared to 10 additional nongreen cities.We would also use more indicators for standard of living including an education component and another health indicator. It would also be interesting to see if there is any survey information asked of residents about their city and their perceived quality of life.











.



