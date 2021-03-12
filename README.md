# green_city

Green or Ungreen Cities: Where do you want to live?

Description
The purpose of this project was to analyze whether being a "green" city positively influences the standard of living for its residents, including the surrounding metro area. In other words, if you were a city leader who wanted to attract people to your city, would it be beneficial to invest in making your city more "green?" As stated on WalletHub.com:
"Apart from employing Americans, clean energy and other 'green'practices, such as recycling programs and urban agriculture, benefit the environment and public health, all of which contribute to America’s bottom line, according to many experts. Recognizing those advantages, cities across the U.S. have increased their sustainability efforts and benefited economically."

We used the list of "Greenest Cities in America" compiled by WalletHub.com to determine which cities to analyze. They evaluated the cities based on factors such as percentage of green space, greenhouse-gas emissions per capital, amount of people who bike vs. drive, and so on. The top or "best" green city is San Francisco, CA and the lowest (at number 100 on the list) or "worst" green city is Baton Rouge, LA. We also compared these cities with Pittsburgh, which wasn't on the "Greenest Cities" list at all. We chose Pittsburgh because it is a relatively large city located in a different geographic area from the other two cities (Baton Rouge and San Francisco).

We determined which quality of life indicators to use to measure how living in a green city (or ungreen city) could influence a resident's wellbeing. Through research on various websites such as investopedia.com, we determined that indicators include employment opportunities, life expectancies, and rates of disease and illness among others. We chose three indicators because we were able to find appropriate data for them: median household income, poverty rate, and life expectancy. We used the United States census  (https://www.census.gov/programs-surveys/saipe/data), to extract this data. While we attempted to use APis to call the data, we  had better success at extracting the data using csv files on the website. We were able to filter based on counties contained in each of the metropolitan study areas (Baton Rouge, Pittsburgh, San Francisco). We used data for the years 2010-2015 because full datasets for all 3 indicators are available for those years.

Cleaning the Data
We used Pandas to clean and organize the data once it had been extracted. This involved quite a bit of trial and error as we determined how to best categorize the information for analysis. For example, we needed to determine 


Analyzing the Data



Conclusion

Usage
Use examples liberally, and show the expected output if you can. It's helpful to have inline the smallest example of usage that you can demonstrate, while providing links to more sophisticated examples if they are too long to reasonably include in the README.

Contributors: Jennifer Duffy, Brianna Papparotto, Vijitha Samarasinghe
Acknowledgements: We would like to thank our instructor, Soheil Hosseini and our TA, Jurgen Arias, for their input and guidance with this project.


Authors and acknowledgment
Show your appreciation to those who have contributed to the project.
