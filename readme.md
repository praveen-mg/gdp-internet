#Internet Penetration and Country GDP for top 100 Populous Country


##Summary
Like food, water and shelter, Internet has become one of human's necessities. Like comparing water quality and malnutrition with country's wealth, its time we start comparing internet usage with country's wealth. In this Graph I am showing how countries GDP affects internet penetration of top 100 populous countries in the world. I extracted information on internet penetration from [internetlivestats](http://www.internetlivestats.com/internet-users-by-country/) and gdp information from [statisticstimes](http://statisticstimes.com/economy/countries-by-projected-gdp-capita-ppp.php). In this graph I have shown how per capita wealth of a country affects percentage of internet users of that particular country.

##Design

In this graph I have used bubble chart to show how country's wealth affects its internet penetration. The GDP per-capita is represented using x axis and internet penetration using y-axis. Since I am taking the top 100 populous country into consideration, its a good idea to size the bubble based on the country's population. Furthermore I have grouped the countries based on their continent and different color is used to show different continents. Continent color information is shown in the legend. So the position, color and size are various visual encoding schemes used in this graph. 

I have also made graph user iterative, users can show or hide particular continent by clicking on the legend. By this interaction they can see how their country fares compared to other countries in the continent or compare only two or three continents of their choice.



##Feedback

I have added all the feedback I received

###Feedback1 (Bilal Tahir)

This is so cool!
one thing I will biggest is to move the data source link a little bit down so it does not overlap with the bar chart. you can also add commas or round population in millions in the details section (which shows up when you hover).

###Feedback2 (Ron Rihoo)

1)What do you notice in the visualization?
2)What questions do you have about the data?
3)What relationships do you notice?
4)What do you think is the main takeaway from this visualization?
5)Is there something you don’t understand in the graphic?


1) The size of the circle appears to be based on the population size (I had to inspect by comparing to figure this out). There appears to be a curve/trend relating internet penetration to GDP for the provided data.

2) What is meant by "internet penetration"? Having some background in Cyber Security -- from my angle of it at least -- the word "penetration" makes me want to think of security vulnerabilities. But I'm guessing, here, it means to have tapped into the internet.

3) Higher GDP and higher internet penetration appear to be related at some rate.

4) A country's internet penetration rate is related to its GDP, while its population does not seem to have a significant effect on its internet penetration rate.

5) No.

Quick advice:

It looks like there's a lot of scroll space created. If the SVG tag had a width="1300" and height="620", then it would look more neat with respect to open space.

I'm making this assumption based off the x and y values and a little bit of trial-and-error using Chrome's Inspect tool.

Great job!
Photo


###Feedback3 (Arturo Battinelli)

Hi Praveen,
I like this visualization! Here my two suggestions:

i. Adding a legend or a note which gives the definition of "internet penetration" (and GDP).

ii. Since the data-points seem to follow a pattern (could be a square root or an arctan), it would be interesting to add an interpolation curve. This may give an interesting insight on the link between GDP and internet penetration.


###Feedback 4 (Saad Khan)

Great representation of the data!

I would suggest, take some help for this visualization

http://www.nytimes.com/interactive/2009/03/01/business/20090301_WageGap.html

1. add 3-4 line brief description at the top
2. try to bring the legend inside the plot, may be at the bottom right where you do not have any points
3. May be highlight the most internet using country as part of the legend(example: N. America [USA], S.America [Brazil]) or any other brief detail you think would be useful at first glance to the viewer.

I think you are almost done, few minor tweaks and you are good to go.

###Changes  made 

Based on user comments I have have reshaped the svg to width and height of 1300 and 720 respectively, so to avoid scroll spaces. I have also added some information on what internet penetration and GDP per capita means. I have changed the population tick format so the population data is shown with comma separation. I don't want to add graph description as mentioned in some feedback, mainly because I want users to understand what I want to convey from the graph but not based on the text present in the graph.

note: I have used Udacity's Data Analyst Nanodegree google plus group to get feedback for my visualization. 


##Resources
[1] http://dimplejs.org/

[2] http://www.w3schools.com/

[3] https://github.com/d3/d3-format/blob/master/README.md#format

[4] https://github.com/d3/d3/blob/master/API.md#number-formats-d3-format