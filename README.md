# Crime_and_Poverty
Our hypothesis is the following. We hypothesize that a decrease in the violent crime rate results in decreases in the poverty rate and an simultaneous increase in median income and median home prices. Our confidence level is 95% or a p-value of 0.05. We hypothesize that the p-value of these statistics in Oak Park, zip codes 95817 and 95820, is statistically different from the rest of the population, which consists of the rest of Sacramento County. Our observed variables are the crime rate, poverty rate, income rate, and median home prices of Oak Park. Our expected values are the crime rate, poverty rate, income rate, and median home prices for all of Sacramento County. Based upon the observed versus the expected values we can calculate the chi-square and one-tailed t-test. If the p value is greater than 0.05 we will accept the hypothesis and test it out by applying it to the rest of Sacramento County.
## Questions
1. List the Poverty Rates versus Crime Rates for years 2014-2019.
2. List the Property Values versus Crime Rates for year 2014-2019.
3. Which Sacramento zip codes have the highest median home price?
4. Which Sacramento zip codes have the lowest median home price?
5. Is there a correlation between home price and crime rate?
6. Is crime increasing in either the lowest or highest property value areas?
7. Analyze the crime data by "bucket." Make a bar char of the crimes per bucket per year to see the changes over time.
*  b1y1, b1y2, b1y3...b4y1, b4y2, b4y3
8. Make a heat map of all of the crimes for the area for the "Crimes against the person *" (Title 8 and Title 9)
9. Make a heat map of all of the high poverty areas.
10. Analyse the crime rates versus the high poverty areas.
11. Analyse the crime rates versus the low poverty areas.

## Jupyter Notebooks
* Crime_CleanUp.ipynb: this notebook performs many manipulations on the raw Crime.csv data file to produce Crime_clean.csv and Crime_Persons_clean.csv. The manipulations involved include renaming columns and, adding new columns to store resultant data.

## To Do List:
1. Sean: 
* Add the raw Crime.csv file to the Resources file --> Done
* Clean the crime data, limit to 2014-2019 and store in Resources/Crime_clean.csv --> Done
* Store a clean "Crimes Agains Persons" csv file in Resources/Crime_Persons_clean.csv --> Done
* Create the zip code to city csv file and store Resources/ZipCode.csv --> Done
2. Cora:
   *update the Readme with our hypothesis  --> Done
   *Test out hypothesis
3. Eliot:
* Do a date frame from census for 2014-2019. Store in Resources/Census.csv
4. Peter:
* Document the steps needed for the various plots and diagrams so they are ready to drop in once the other data is available.

## Data Sets
1. https://data.saccounty.net/datasets/9a7f2df25a584ff9b55db274704ad7c9_0/geoservice
2. http://www.ciclt.net/sn/clt/capitolimpact/gw_ziplist.aspx?FIPS=06067
3. https://leginfo.legislature.ca.gov/faces/codedisplayexpand.xhtml?tocCode=PEN


