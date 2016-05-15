# Data Visualisation Project Submission



## Summary
The visualisation examines loan data provided by Prosper, a peer-to-peer lending service. The graph focusses on returns generated by the service. Specifically it examines the estimated return assigned to the listing at the time it was created. The estimated return takes the estimated loss rate into account in its calculation.

## Design
I started out by examining the entire dataset in Tableau looking for interesting patterns in the data. The effective return generated through lending through this service I feel is an important variable, and one which I decided to focus on.

The resulting circle view graph in Tableau (see Intial_Tableau_Image.png) showed a decrease in returns over time however I felt this graph looked messy. Further, since there are almost 114,000 datapoints, when attempting to generate a scatterplot of this data using dimple, I was unable to load the graph.

I therefore summarised the data, looking at mean returns over time. There appeared to be no outliers in the data, based on the Tableau chart. I used the pandas and numpy libraries in Python to group the data by years, focussing on the effective returns and listing date.

My initial visualisation combines a scatterplot with a line chart so that each data point is highlighted using the scatterplot and the trend is highlighted with the line graph. I changed the y-axis tick format to give the returns in percentage, I felt this would be easier to understand. I also fixed the maximum and minimum values for the y-axis to zoom in on the data. Interaction within this graph is through the ability to hover over a data point in order to see the actual figures behind the data. 

Feedback is based on the initial visualisation (index1.html).

## Feedback

The main takeaway from the first person was that while the graph is very easy to understand, the first four datapoints are redundant and should be removed. The were also questions on what could have caused the decline in returns, my guess is that the effects of the financial crisis caused the diminished returns, with an increase in the rate of loans defaulting, the estimated loss rate is likely to have increased.

After removing the redundant datapoints, the remaining feedback was based on the index2.html visualisation.

Feedback from the next two people was focussed around a similar theme, that the graph was an oversimplified summary, and that the spread of returns should be given in order to display the range of returns that could be achieved. Including the maximum and minimum value for each year was a good middle ground between the overly busy scatter plot and the oversimplified mean returns graph. This would clearly display a reduced spread in returns over time, as well as giving a more complete picture of potential returns. 

Index_final.html gives the min, max and mean returns.

## Resources

The numpy and pandas libraries in Python were used to summarize the data.
I used the melt function to regroup the data so I could display the min, max and mean on one graph. Help for this was taken from the following blog:
http://connor-johnson.com/2014/08/28/tidyr-and-pandas-gather-and-melt/

Other resources included the following:

http://dimplejs.org/examples_index.html

https://github.com/PMSI-AlignAlytics/dimple/wiki/dimple.chart#addMeasureAxis


