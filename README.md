# MSDS692-Project
Over the past 2 years we have been living in a wordwide pandemic.  About a year ago vaccines began to be available for people to get to fight against Covid-19. 
For my project I wanted to find if there were any patterns on vaccination rates and political party identification.  

The goal of the project was to find if I could use vaccination rates to predict if people would vote republican or democrat.

The data that obtained and focused on for my project were election results organized by county in Washington state for the 2016 election, data on Washington state's K-12 school immunization records, and data on Covid-19 vaccinations by county in Washongton state.  When cleaning the data I removed a lot of data points that I did not need for my project.  For the student immunization data I needed to combine all of the schools to their respective county and did so by finding the average.  For the Covid-19 data I really only needed to isolate the two columns that I needed for my final dataframe, this dataset required the least amount of cleaning.  For the election data set I needed to remove rows of information that I did not need and I needed to figure out how to only keep the party with the highest amount of votes.  Then I needed to compbine all three datasets to get my final dataframe. I did have some roadblocks in this stage as I needed to manipulate my dataframe in ways I had never done before, however I was able to resolve these problems by looking up advice online and have the resources sited below.  

After cleaning my data I ran an exploratory data analysis to observe the correlation between my variables.  One interesting thing that I noticed at this point was that the Covid-19 vaccination data and the student immunization data had oppposite correlations to poitical party.  

![Student Immunization Data](/images/Student Visual.png)

![Covid-19 Data](/images/Covid-19 Visual.png)

![correlations](/images/correlation.png)

To obtain my goal I decided to use a KNN model and a decision tree model.  

I set up my KNN model to predict for political party.  In this case I was predicting whether or not the county voted republican or democrat in the 2016 presidential election.  I set my training and test group at a 70:30 ratio with 2 groups as I was looking to predict a binary.  In my test group I had 12 predictions and only 1 came back incorrectly predicted.  I used a confusion matrix to see the results as well as a classification report.  I found that my accuracy with the KNN model was 0.92. 
I also ran a table to check the error rate to the number of groups used and as I predicted two groups showed the lowest error rate.  

Next I decided to make a decision tree model to see how it compared to my KNN model.  I found that the accuracy with the decision tree model when using the same training and test sets was lower at 0.75.  Three out of the twelve data points were predicted incorrectly.  Every point that was predicted incorrectly was a democratic county predicted as republican.  I also ran a importance list to find the weight of each feature on determining the party and discovered that Covid-19 vaccination rates had a higher weight than student immunization rates at 0.86 and 0.14 respectively.  

In conclusion I believe it is possible to accurately predict political party alignment based on vaccination rates, however further research could be done to see if this holds true across other states and across the country. With more data points the resuts may differ but I think that it would improve my model.  One of the drawbacks I would say to my research and model is the limited data points I had because I organized it by county.  I also think further research or data could be drawn from using the 2020 election results. 

Resources

All students, kindergarten through 12th grade, immunization data by school, 2015-2016 | Data.WA | State of Washington. (n.d.). Retrieved March 3, 2022, from https://data.wa.gov/Health/All-students-kindergarten-through-12th-grade-immun/ie96-cgrn

Covid-19 vaccinations in the united states,county | data | centers for disease control and prevention. (n.d.). Data.CDC.Gov. Retrieved March 3, 2022, from https://data.cdc.gov/Vaccinations/COVID-19-Vaccinations-in-the-United-States-County/8xkx-amqh

Cummings, M. (2020, October 27). Politics affect public buy-in on COVID-19 vaccine, study shows. YaleNews. https://news.yale.edu/2020/10/27/politics-affect-public-buy-covid-19-vaccine-study-shows

Galston, W. A. (2021, October 1). For COVID-19 vaccinations, party affiliation matters more than race and ethnicity. Brookings. https://www.brookings.edu/blog/fixgov/2021/10/01/for-covid-19-vaccinations-party-affiliation-matters-more-than-race-and-ethnicity/
How to combine dataframes in python? - Askpython. (2021, July 9). https://www.askpython.com/python-modules/pandas/combine-dataframes-in-python

November 8, 2016 general election—Export results. (n.d.). Retrieved March 3, 2022, from https://results.vote.wa.gov/results/20161108/export.html

Python—How can i “merge” rows by same value in a column in pandas with aggregation functions? (n.d.). Stack Overflow. Retrieved March 3, 2022, from https://stackoverflow.com/questions/46826773/how-can-i-merge-rows-by-same-value-in-a-column-in-pandas-with-aggregation-func

Reset index in pandas dataframe. (2018, December 4). GeeksforGeeks. https://www.geeksforgeeks.org/reset-index-in-pandas-dataframe/
Why the COVID-19 debate has everything to do with politics, and nothing to do with health. (2021, August 6). Deseret. https://www.deseret.com/2021/8/5/22606477/messaging-politics-of-covid-19-vaccine-coronavirus-mcdonalds-vaccination-delta-variant-biden-fauci

