Data Visualization with Python
===============================

by IBM

# Week 2

## Key Concepts
* Learn about area plots, and how to create them with Matplotlib.
* Learn about histograms, and how to create them with Matplotlib.
* Learn about bar charts, and how to create them with Matplotlib.
* Learn about pie charts, and how to create them with Matplotlib.
* Learn about box plots, and how to create them with Matplotlib.
* Learn about scatter plots and bubble plots, and how to create them with Matplotlib.

#### Title: Basic Visualization Tools

##### Area Plots

* An **area plot** also known as an **area chart** or graph is a type of plot that depicts accumulated totals using numbers or percentages over time
* It is **based** on the **line plot** and is commonly used when trying to compare two or more quantities
* **Note** that Matplotlib plots the indices of a dataframe on the horizontal axis
	* If this is a problem with your data frame then you can
		* Fix this, we need to take the **transpose** of the dataframe

##### Histograms

* A **histogram** is a way of representing the frequency distribution of a numeric dataset
* The way it works is it partitions the spread of the numeric data into **bins**, assigns each datapoint in the dataset to a bin, and then counts the number of datapoints that have been assigned to each bin
	* Vertical axis is actually the frequency or the number of datapoints in each bin
	* For example, 
		* let's say the range of the numeric values in the dataset is 34,129
		* the first step in creating the histogram is **partitioning** the **horizontal** axis in, say, **ten bins** of equal width, and then we construct the histogram by **counting** how many **datapoints have a value that is between the limits of the first bin**, the second bin, the third bin, and so on
		* Say the number of datapoints having a value between 0 and 3,413 is 175
			* Then we draw a bar of that height for this bin. 
		* We repeat the same thing for all the other bins, and if no datapoints fall into a bin then that bin would have a bar of height **0**

##### Bar Charts

* Unlike a histogram, a **bar chart** also known as a **bar graph** is a type of plot where the length of **each bar** is **proportional** to the **value** of the item that it represents
* It is commonly used to compare the values of a variable at a given point in time
* For example
	* Say we're interested in visualizing in a discrete fashion how immigration from Iceland to Canada looked like from 1980 to 2013
	* One way to do that is by building a bar chart where the height of the bar represents the total immigration from Iceland to Canada in a particular year


#### Title: Specialized Visualization Tools

##### Pie Charts

> Bar charts are much better when it comes to representing the data in a consistent way and getting the message across

* A **pie chart** is a circular statistical graphic divided into slices to illustrate numerical proportion
* There are some very vocal opponents to the use of pie charts under any circumstances. Most argue that pie charts fail to accurately display data with any consistency
* A **pie chart** is a circualr graphic that displays numeric proportions by dividing a circle (or pie) into proportional slices. You are most likely already familiar with pie charts as it is widely used in business and media. We can create pie charts in Matplotlib by passing in the kind=pie keyword.
* **Article** : Flaws of PIE CHARTS
	* https://www.surveygizmo.com/resources/blog/pie-chart-or-bar-graph/

##### Box Plots

> Check Slide Notes folder for Image of dimensions

* A **box plot** is a way of statistically representing the distribution of given data through **five** main **dimensions**
	* The first dimension is **minimum**, which is the smallest number in the sorted data
	* The second dimension is **first quartile**, which is the point 25% of the way through the sorted data
		*  In other words, a quarter of the datapoints are less than this value
	* The third dimension is **median**, which is the median of the sorted data
	* The fourth dimension is **third quartile**, which is the point 75% of the way through the sorted data
		* In other words, three-quarters of the data points are less than this value
	* The final dimension is **maximum**, which is the highest number in the sorted data


##### Scatter Plots

* A **scatter plot** is a type of plot that displays values pertaining to typically two variables against each other
* Usually it is a dependent variable to be plotted against an **independent variable** in order to determine if any **correlation** between the **two variables** exists
* Unlike the other data visualization tools where only passing the kind parameter was enough to generate the plot, with scatter plots we also need to pass the variable to be plotted on the horizontal axis as the x-parameter, and the variable to be plotted on the vertical axis as the y-parameter
* A scatter plot (2D) is a useful method of comparing variables against each other
* Scatter plots look similar to line plots in that they both map independent and dependent variables on a 2D graph

##### Bubble Plots

* A **bubble plot** is a variation of the **scatter plot** that displays **three dimensions** of data (x, y, z)
* The datapoints are replaced with bubbles, and the size of the bubble is determined by the third variable **z**, also known as the **weight**
* In **maplotlib**, we can pass in an array or scalar to the keyword **s** to **plot()**, that contains the weight of each point.


