# Projectstest
This is my first Data analysis project done in python.
For the project I used two data sets: https://github.com/fivethirtyeight/data/tree/master/police-killings and  http://factfinder.census.gov/faces/tableservices/jsf/pages/productview.xhtml?src=bkmkl
All full analysis can be found in the police killing analysis.docx found in the files above
#An analysis on Police Killings
The names of Trayvon Martin, Michael Brown, and Jordan Davis may sound familiar to you. All three suffered similar fates at the hands of police, and all three have become martyrs for the fight against police corruption and social inequality.   
While emotional damage and social injustice can never be truly quantified, police killings can. In the following analysis we explore 538’s 2015 Police killing data set to explain arguments and observe trends. 
#Two types of arguments
Aren’t there more white victims from police shootings than there are black? Why are we focusing so much attention on black victims? I mean if we simply plot the numbers it seems pretty clear. There is almost twice as much white victims than black victims!

![alt tag](https://github.com/allenlu95/Police_shootings/blob/master/download%20(2).png)


While most people seem to understand the logical fallacy behind such an argument, it is astounding to see the amount of people on social media who fall for this over and over again. It is the same idea as if I told you driving sober causes more accidents than driving drunk. While word for word the statement is true we fail to notice there are many more sober drivers than drunk drivers on the road. A true representation can only be found by scaling the number of shootings against population percentage. Once scaled we get the following:

![alt tag](https://github.com/allenlu95/Police_shootings/blob/master/download%20(3).png)

Amazing how much changes with some basic statistic knowledge. With 1.0 set as the rate of shootings being exactly proportionate to population percentage, we see black people are more than doubly overrepresented. To confirm such a distribution is not due to chance (maybe police happened to kill more black people in 2015) we perform a chi-square test. This test measures the squared difference between our observed values (numbers given in the data above) against our expected values (if every race got killed by the percentage they represent).  The resulting p-value of our test is 
2.75 x 10<sup>-22</sup>, essentially 0, more than enough to satisfy the null hypothesis test of being below 0.05. In English this means there’s far less than a 1 percent chance such a distribution was due to chance.
#Killings based on Income
While the media tend to focus on racial factors when talking about police shootings, income level is often overlooked. Here we explore the relationships between police killings and income levels, specifically personal income (one person).

![alt tag](https://github.com/allenlu95/Police_shootings/blob/master/download%20(5).png)

With the national average personal income for 2014 set at 33,000 the income of victims are much lower than normal with a median of 22,348. Interestingly enough, blacks have the one of lowest average incomes among all races at 27,000. This leads us to the question if police injustice results from racial prejudice or economic discrimination. It is interesting to note both Native Americans and the category classified as Unknown have lower median income than African Americans do, but are killed at a much lower rate than African Americans are. This observation may lead us towards the view that police in general have racial prejudice, but we must also factor in that sample sizes for Native Americans and unknown are very small, making conclusions less reliable.  

#Police Killings By State

To check the results of our two observations above we take a look of police killings by state. We check the five top and bottom states in police shootings for similarities and differences. From our data we see the bottom five consists of mainly northeast states, such as Connecticut and Pennsylvania, while the top five consists of southern and western states like Arizona, and Oklahoma. We explore these states even further by looking at two key statistics, racial make up and average income. We notice states with more police killings tend to have lower average income, 48706 compared to 54830 confirming our income based hypothesis; however, we notice something interesting in the racial breakdown. There are actually a higher percentage of African Americans (21%) in states with the LOWEST police killings compared to the national percentage of African Americans at 12%. Another interesting trend is, regions with higher Latino percentages (20% compared to national average of 16%) have the HIGHEST rate of police killings. This trend may be purely geographical as West coast states have higher Hispanic populations than east coast states do. This observation may also lead to many differing arguments, ranging from more African Americans in a state lessen prejudice towards them, to racial injustice is just a myth and is a side effect of economic discrimination.  Data in this case only get us so far; further investigation will require a more direct approach.

#Future updates
I will go back on this particular project in the future and analyze information on age and gender as well as create a choropleth map with matplotlib. I will also split up the income ranges and see if the distribution for police killings remain the same among races. This method will give me a better picture of the race versus income level debate.




