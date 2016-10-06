# Internet Penetration and Country GDP for top 100 Populous Country


## Summary
Like food, water and shelter, Internet has become one of human's necessities. Like comparing water quality and malnutrition with country's wealth, its time we start comparing internet usage with country's wealth. In this Graph I am showing how countries GDP affects internet penetration of top 100 populous countries in the world. I extracted information on internet penetration from [internetlivestats](http://www.internetlivestats.com/internet-users-by-country/) and gdp information from [statisticstimes](http://statisticstimes.com/economy/countries-by-projected-gdp-capita-ppp.php). In this graph I have shown how per capita wealth of a country affects percentage of internet users of that particular country.

From the graph we can  see  that  as  the  country's  wealth (GDP per capita) increases  internet  usage (internet penetration)  also  increases. The  richer countries  like USA, Singapore  and many  european countries has higher internet penetration. We can clearly see continent europe has many richer countries and high internet usage, on the other hand africa has many poor countries and lower internet usage.

## Design

In this graph I have used bubble chart to show how country's wealth affects its internet penetration. The GDP per-capita is represented using x axis and internet penetration using y-axis. Since I am taking the top 100 populous country into consideration, its a good idea to size the bubble based on the country's population. Furthermore I have grouped the countries based on their continent and different color is used to show different continents. Continent color information is shown in the legend. So the position, color and size are various visual encoding schemes used in this graph. 

I have also made graph user iterative, users can show or hide particular continent by clicking on the legend. By this interaction they can see how their country fares compared to other countries in the continent or compare only two or three continents of their choice.



## Feedback

My Graph before any feedback looked as below

![Alt text](screenshot/FirstDraft.png?raw=true "Optional Title")

I have added all the feedback I received

### Feedback1 (Bilal Tahir)

This is so cool!
one thing I will biggest is to move the data source link a little bit down so it does not overlap with the bar chart. you can also add commas or round population in millions in the details section (which shows up when you hover).

### Feedback2 (Ron Rihoo)

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


### Feedback3 (Arturo Battinelli)

Hi Praveen,
I like this visualization! Here my two suggestions:

i. Adding a legend or a note which gives the definition of "internet penetration" (and GDP).

ii. Since the data-points seem to follow a pattern (could be a square root or an arctan), it would be interesting to add an interpolation curve. This may give an interesting insight on the link between GDP and internet penetration.


### Feedback 4 (Saad Khan)

Great representation of the data!

I would suggest, take some help for this visualization

http://www.nytimes.com/interactive/2009/03/01/business/20090301_WageGap.html

1. add 3-4 line brief description at the top
2. try to bring the legend inside the plot, may be at the bottom right where you do not have any points
3. May be highlight the most internet using country as part of the legend(example: N. America [USA], S.America [Brazil]) or any other brief detail you think would be useful at first glance to the viewer.

I think you are almost done, few minor tweaks and you are good to go.



### Changes  made after feedback received

Based on user comments I have  reshaped the svg to width and height of 1300 and 720 respectively, so to avoid scroll spaces. I have also added some information on what internet penetration and GDP per capita means. I have changed the population tick format so the population data is shown with comma separation. I don't want to add graph description as mentioned in some feedback, mainly because I want users to understand what I want to convey from the graph but not based on the text present in the graph.

My graph looked as follows after making these changes

![Alt text](screenshot/AfterFeedback.png?raw=true "Optional Title")


note: I have used Udacity's Data Analyst Nanodegree google plus group to get feedback for my visualization. 

### Feedback From Udacity Reviewer

#### The visualization centers on a specific, clear finding in the data.

Very nice visualization! This project greatly demonstrated your technical skills in data visualization. To pass this specification, however, we also need that the visualization to center on a specific, clear finding in the data. In other words, this means the visualization needs to be explanatory rather than exploratory (still remember the lesson on Martini Glass principle?).

There are various ways to present this information, here are a couple of ideas, but what you can do here is not limited to only my suggestions:

You may update the title of this visualization to include the finding directly.
Or expand the paragraph below it.
Or, my favorite way of doing this, by updating the visualization so it can tell a narration that leads to main finding. For this, you will need to add some interactivity to the visualization. You'll get to learn much useful data visualization techniques by doing this. I really can't tell you exactly what to do for this, since you are the expert for your data, but generally first you want to ensure what main finding you wish to explain (e.g. how GDP is correlated with internet penetration, and for countries with larger population internet population is generally low), then animate and add explanation as the visualization shows different parts (perhaps first show some countries that show linear correlation, then show countries with large populations).

#### The selected finding is clearly communicated. Design choices foster communication between the reader and the visualization.

As explained above, make sure that design choices communicates your main finding well to readers. There are also a couple of technical improvements I can suggest to improve this visualization. Current visualization is already great, but these are just small things I noticed to make it perfect:

##### Add a legend for circle sizes

Without reading the README file, I wasn't initially sure what values were encoded by circle size. Could you please add a legend showing this information somewhere in the visualization?

##### Use circle area instead of radius

in these circles you seem to encode the values in radius, which conveys non linear rate of significance. What I mean by this is due to how circle area is calculated, small difference in radius may be shown as large difference in area. Instead of using radius, I suggest that you root-square the values before using them in radius. Remember that area of a circle is calculated with formula π * r^2, so by square rooting the radius the rate of change becomes linear.

Here is the related article explaining about this issue.

Watch this lesson that explains how to correct radius for d3js. For dimple js it is similar, you just need to update "r" attribute of circles.

### Changes Made after Udacity reviewer feedback

I changed the radius of the bubble to square root of the population, to do this I introduced new column in the csv file containing square root of population. This change improved my graph vastly as countries with smaller population are represented by more visible bubble. Previously in my chart bubbles are vastly exaggerated for countries with high population such as India and China. I have made the graph more explanatory by changing title and adding some explanation.

After the changes my graph looked as follows

![Alt text](screenshot/Final.png?raw=true "Optional Title")





## Resources
[1] http://dimplejs.org/

[2] http://www.w3schools.com/

[3] https://github.com/d3/d3-format/blob/master/README.md#format

[4] https://github.com/d3/d3/blob/master/API.md#number-formats-d3-format
