Data Visualization with Python
===============================

by IBM

# Week 1

## Key Concepts
* Learn about data visualization and some of the best practices to keep in mind when creating plots and visuals.
* Learn about the history and the architecture of Matplotlib.
* Learn about basic plotting with Matplotlib.
* Learn about the dataset on immigration to Canada, which will be used extensively throughout the course.
* Briefly learn how to read csv files into a pandas dataframe and process and manipulate the data in the dataframe.
* Learn how to generate line plots using Matplotlib.

#
#### Title: Introduction to Data Visualization Tools

##### Introduction to Data Visualization

* Data visualization is a way to show a complex data in a form that is graphical and easy to understand
* This can be especially useful when one is trying to explore the data and getting acquainted with it
* Since a picture is worth a thousand words, then plots and graphs can be very effective in conveying a clear description of the data especially when disclosing findings to an audience or sharing the data with other peer data scientists
* They can be very valuable when it comes to supporting any recommendations you make to clients, managers, or other decision-makers in your field
* Darkhorse Analytics is a company that spun out of a research lab at the University of Alberta in 2008 and done fascinating work on data visualization. Darkhorse Analytics specializes in quantitative consulting in several areas including data visualization and geo spatial analysis
	* Creating a visual revolves around three key points
		* less is more effective
		* it is more attractive
		* it is more impactive
	* In other words, any feature or design you incorporate in your plot to make it more attractive or pleasing should support the message that the plot is meant to get across and not distract from it

> Bar graphs and charts on the other hand are argued to be far superior ways to quickly get a message across

##### Introduction to Matplotlib

* ***History***
	* Matplotlib is one of the most widely used, if not the most popular data visualization library in Python
	* It was created by **John Hunter**, who was a neurobiologist and was part of a research team that was working on analyzing **Electrocorticography signals**, **ECoG** for short
	* Matplotlib was originally developed as an ECoG visualization tool, and just like MATLAB
	* Matplotlib was equipped with a scripting interface for quick and easy generation of graphics, represented by pyplot
* ***Architecture***
	* It has 3 main layers
		* the back-end layer
		* the artist layer
			* where much of the heavy lifting happens and is usually the appropriate programming paradigm when writing a web application server, or a UI application, or perhaps a script to be shared with other developers
		* the scripting layer
			* which is the appropriate layer for everyday purposes and is considered a lighter scripting interface to simplify common tasks and for a quick and easy generation of graphics and plots
* **Back-end layer**
	* It has 3 built-in abstract interface classes
		1. FigureCanvas
			* matplotlib.backend_bases.FigureCanvas
			* Encompasses the area onto which the figure is drawn
		1. Renderer
			* matplotlib.backend_bases.Renderer
			* Knows how to draw on the FigureCanvas
		1. Event
			* matplotlib.backend_bases.Event
			* Handles users input such as keyboard strokes and mouse clicks
* **Artist layer**
	* It is composed of one main object - Artist
	* The artist is the object that knows how to take the Renderer and use it to put ink on the canvas
	* Everything you see on a Matplotlib figure is an artist instance. The title, the lines, the tick labels, the images, and so on, all correspond to an individual artist
	* There are two types of Artist objects
		* **Primitive**
			* Line2D, Rectangle, Circle, and Text
		* **Composite**
			* Axis, Ticks, Axes, and Figure
	* The top-level Matplotlib object that contains and manages all of the elements in a given graphic is the **Figure artist**
	* The most important composite artist is the **axes** because it is where most of the Matplotlib API plotting methods are defined, including methods to 
		* create
		* manipulate the ticks
		* the axis lines
		* the grid or the plot background
	* Each composite artist may contain other composite artists as well as primitive artists
		* Example - figure artist for example would contain an axis artist as well as a rectangle or text artists
* **Scripting layer**
	* Scripting layer, it was developed for scientists who are not professional programmers
	* Matplotlib's scripting layer is essentially the Matplotlib.pyplot interface, which automates the process of defining a canvas and defining a figure artist instance and connecting them
	* Comprised mainly of pyplot, a scripting interface that is lighter than the Artist Layer.


##### Basic Plotting with Matplotlib

> Jupyter Notebook is, it's an open source web application that allows you to create and share documents that contain live code visualizations and some explanatory text as well
> Jupyter has some specialized support for Matplotlib and so if you start a Jupyter notebook, all you have to do is import Matplotlib and you're ready to go

* Matplotlib is a well-established data visualization library that is well supported in different environments such as in 
	* Python scripts
	* iPython shell
	* web application servers
	* in graphical user interface toolkits
	* Jupyter notebook
* You can literally create almost all of the conventional visualization tools such as histograms, bar charts, box plots and many others using one function only: the **plot function**
* Magic function starts with %matplotlib, and to enforce plots to be rendered within the browser, you pass in inline as the backend
* Matplotlib has a number of different backends available
* One limitation of this backend is that you cannot modify a figure once it's rendered
* With the notebook backend in place, if a plt function is called, it checks if an active figure exists, and any functions you call will be applied to this active figure
	* If a figure does not exist, it renders a new figure
* **Pandas** also has a built-in implementation of Matplotlib
	* Syntax
		* df['column_name'].plot(kind='hist')
		* df.plot(kind='line')


##### Line Plots

> A **line chart** or **line plot** is a type of plot which displays information as a series of data points called **markers** connected by straight line segments.
It is a basic type of chart common in many fields.
Use line plot when you have a continuous data set.
These are best suited for trend-based visualizations of data over a period of time.

* It is a plot in the form of a series of data points connected by straight line segments
* It is one of the most basic type of chart and is common in many fields not just data science
* The more important question is when to use line plots
	* The best use case for a line plot is when you have a continuous dataset and you're interested in visualizing the data over a period of time
	* Example, say we're interested in the trend of immigrants from Haiti to Canada. We can generate a line plot and the resulting figure will depict the trend of Haitian immigrants to Canada from 1980 to 2013
		* Based on this line plot, we can then research for justifications of obvious anomalies or changes
