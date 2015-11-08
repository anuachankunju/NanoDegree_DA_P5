# Data Visualization: Baseball players Performance

##Summary
The goal of this visualization is to compare the performance of 1157 baseball player in terms of their Handedness and how the performance measures (batting average and home runs) varies with player’s Height. 

##Design
My design include:
* Two bar charts explaining the performance (Batting Average & Home Runs, encoded in Y-axis) summary by Handedness (Encoded in X-axis). Bar chart was selected as the chart type as its best for comparing categorical variable values like Handedness.

* Two trend charts explaining how the performance (Batting Average & Home Runs , encoded in Y axis) varies with Height(encoded in X axis) for different Handedness (encoded in Color). Line chart is best suited to analyze relationships and show trends. Hence this chart type was selected.

####Exploratory Data Analysis in R
I downloaded the Baseball Data from Udacity’s dataset options that included performance and physical aspects like height, weight and handedness of 1157 players. I have analyzed the data using R. Some basic statistics and plots revealed a clear performance difference between left and  right handed players as shown below:

![Explore 1](https://github.com/anuachankunju/NanoDegree_DA_P5/blob/master/images/Exploratory_1_HomeRunsVsHandedness.JPG)
![Explore 2](https://github.com/anuachankunju/NanoDegree_DA_P5/blob/master/images/Exploratory_2_Handedness.JPG)

The remaining analysis can be found in [PlayerDataExpolration](https://github.com/anuachankunju/NanoDegree_DA_P5/blob/master/PlayerDataExpolration.html)

####Data Visualization (dimple.js)
To emphasize my finding in exploratory analysis that **Left handers usually have better performance** in terms of batting average and Home Runs, I introduced one more variable Height to explain how the performance of left and right hand players varies by Height. Height was showing an interesting trend in my exploratory analysis. Exploratory Analysis shows that players in certain Height range (70-75) have a better average home run. 

Line chart helps to determine the relationship between two sets of values. As my attempt was to show the performance trend by Handedness line chart was selected. 

A players performance can be measured by batting Average as well as home runs. Hence two separate visualizations were created:

* Mean Batting average variance by Height faceted by Handedness
* Mean Homeruns variance by Height faceted by Handedness

I also included two bar charts to show the performance (Batting Average & Home Runs) summary by Handedness before the trend chart as it will give a clear idea about the performance summary to audience. A bar chart is usually used for the comparison of categorical data. Here Bar chart was selected as the chart type as I’m trying to compare the left and right hand player’s performance. The visualization can be found in index_2.html.



##Feedback
I interviewed 3 individuals in person, and asked for their feedback on the data visualization after prompting them with the background information and a small set of questions. Highlighted comments from them are listed below:

#####Interview #1
I have showed this graph to my colleague and he gave the following comments:

"The graph is clearly explaining the performance differences between left & Right handed players. Some improvements I see are:
* Y-axis of first chart is showing repeated values. Rounding it to 2 decimals will solve the issue
* The line graph shows close trends which is difficult to follow for some ranges where the mean values are very close.    Highlighting the Left Handers trend to emphasize the  better performance .
* Also adding title to the summary charts will help to convey the message effectively."


######Post-feedback Design-1
Incorportaed the suggessions to correct the error on Y-axis labels. Titles to bar chart conveyed the message clearly to audince. Adding the mouse over improved the clarity of teh trend. Also helped ina dding an animation into my chart.



#####Interview #2
Second person who reviewed the improved graph was another Nano-degree student in my organization and her comment was:

I loved the visualization which is clearly conveying the message. Color combinations are really nice. However one thing I noted is the color coding used to encode handedness in the bar chart and line chart are different. This will mislead the viewer. I would suggest to use the same color coding for Handedness for all the charts. 
Similar to bar charts add titles for your line charts also.

######Post-feedback Design-2
As per the feed back changed the color coding to use same color through the story for each handedness. This helped to clearly convey the message. There was  a chance that reader will unknowingly follow the barchart color coding for trend chart also. This suggession really helped not to misslead any readers.


#####Interview #3
Third person with whom I reviewed my graph with was a six sigma black belt of my team and here are the highlights from his comments: 

“This is an excellent visual for the given data set. However some minor improvements suggested are: 
* Use a standard title for the plots
* Give a small description about the chart and if possible a link to the data set 
* Remove grid lines from the graphs as there is a mouse over event
* First I didn’t notice the feature of highlighting the focused trend line. Please provide a note  at the bottom of the graph to move the mouse pointer to trend line."

######Post-feedback Design-3
I feel the aesthetics improved a lot with better title and graphs look cleaner without the grid lines. Providing a link to the data set will help interested readers to look and play around the dataset. Also there was a chance that some of the readers may miss the trend line mouse over effect. Adding the footer noter will make sure that all readers will notice with the effect.

#####Udacity Review
Here are the review comments from Udacity review:
* Filter out players with zero batting averages before building final plots.
* Consider making plot with just lines. Also, there are some strange spikes and drops, I think there are some outliers or missing data for particular height. Better way to use some trend line like in your exploratory data analysis.
* In comparison to previous version of this visualization code quality a little bit lower. There are some places where formatting can be improved. 

######Final Design

All the suggestions from the Udacity review are incorporated in my final design. Major changes are:
* Added a condition while loading the data to filter all the players with zero batting average. This change helped in showing the correct batting average and home run trends, especially for taller players. Mixing the zero values will show us misleading trend, i.e. averages lower for taller players because of small count of taller people, not because taller players have worse performance. 
* I removed the points on the trend line and also smoothened the trend line with the help of interpolation function. This helped in showing a better trend line than before.
* All the  suggestions provided in the code review  are incorporated to improve the code readability.


## Resources
* [dimple.js Documentation](http://dimplejs.org/) 
* [Data Visualization and D3.js(Udacity)](https://www.udacity.com/course/viewer#!/c-ud507-nd)
* [Various Stack Overflow posts:](http://stackoverflow.com/search?q=dimple.js) 

## Data
* [data/baseball_data.csv](https://github.com/anuachankunju/NanoDegree_DA_P5/blob/master/data/baseball_data.csv):  original downloaded dataset with calculated BMI column.
