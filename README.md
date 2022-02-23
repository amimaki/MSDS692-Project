# MSDS692-Project
Over the past 2 years we have been living in a wordwide pandemic.  About a year ago vaccines began to be available for people to get to fight against Covid-19. 
For my project I wanted to find if there were any patterns on vaccination rates and political party identification.  

The goal of the project was to find if I could use vaccination rates to predict if people would vote republican or democrat.

The data that obtained and focused on for my project were election results organized by county in Washington state for the 2016 election, data on Washington state's K-12 school immunization records, and data on Covid-19 vaccinations by county in Washongton state.

To obtain my goal I decided to use a KNN model and a decision tree model.  

First I needed to clean my data.  In cleaning my data I did hit a few roadblocks because I needed to manipulate the data in ways that I hadn't before.  For example, I needed to combine all of the schools' immunization records to the county they were in, and select only certain rows to keep within the election results data. And then because I was using three different data sets I needed to merge them together to create one data frame and I had not done this before either.  I was able to resolve these roadblocks by searching and watching videos online. 

After cleaning my data I ran an exploratory data analysis to observe the correlation between my variables.  One interesting thing that I noticed at this point was that the Covid-19 vaccination data and the student immunization data had oppposite correlations to poitical party.  

I set up my KNN model to predict for political party.  In this case I was predicting whether or not the county voted republican or democrat in the 2016 presidential election.  I set my training and test group at a 70:30 ratio with 2 groups as I was looking to predict a binary.  In my test group I had 12 predictions and only 1 came back incorrectly predicted.  I used a confusion matrix to see the results as well as a classification report.  I found that my accuracy with the KNN model was 0.92. 
I also ran a table to check the error rate to the number of groups used and as I predicted two groups showed the lowest error rate.  

Next I decided to make a decision tree model to see how it compared to my KNN model.  I found that the accuracy with the decision tree model when using the same training and test sets was lower at 0.75.  Three out of the twelve data points were predicted incorrectly.  Every point that was predicted incorrectly was a democratic county predicted as republican.  I also ran a importance list to find the weight of each feature on determining the party and discovered that Covid-19 vaccination rates had a higher weight than student immunization rates at 0.86 and 0.14 respectively.  

In conclusion I believe it is possible to accurately predict political party alignment based on vaccination rates, however further research could be done to see if this holds true across other states and across the country. With more data points the resuts may differ but I think that it would improve my model.  One of the drawbacks I would say to my research and model is the limited data points I had because I organized it by county.  I also think further research or data could be drawn from using the 2020 election results.  
