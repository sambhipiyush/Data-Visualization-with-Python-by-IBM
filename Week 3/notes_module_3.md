Data Visualization with Python
===============================

by IBM

# Week 3

## Key Concepts
* Learn about advanced visualization tools such as waffle charts and word clouds, and how to create them.
* Learn about seaborn, which is another visualization library, and how to use it to generate attractive regression plots.
* Learn about Folium, which is another visualization library, designed especially for visualizing geospatial data.
* Learn how to use Folium to create maps of different regions of the world and how to superimpose markers on top of a map.
* Learn how to use Folium to create choropleth maps.

#### Title: Advanced Visualization Tools

##### Waffle Charts

* A waffle chart is a great way to visualize data in relation to a whole or to highlight progress against a given threshold
	* For **example**, say immigration from Scandinavia to Canada is comprised only of immigration from Denmark, Norway, and Sweden, and we're interested in visualizing the contribution of each of these countries to the Scandinavian immigration to Canada
	* The main idea here is for a given waffle chart whose desired height and width are defined, the contribution of each country is transformed into a number of tiles that is proportional to the country's contribution to the total, so that 
		* more the contribution the more the tiles, resulting in what resembles a waffle when combined
* Matplotlib does not have a built-in function to create waffle charts

##### Word Clouds

* A word cloud is simply a depiction of the importance of different words in the body of text
* A word cloud works in a simple way; the more a specific word appears in a source of textual data the bigger and bolder it appears in the world cloud
* Example - given some text data on recruitment
	* This cloud tells us that words such as recruitment, talent, candidates, and so on, are the words that really stand out in these text documents
	* Assuming that we didn't know anything about the content of these documents, a word cloud can be very useful to assign a topic to some unknown textual data

##### Seaborn and Regression Plots

* Seaborn is another data visualization library, it is actually based on Matplotlib
* It was built primarily to provide a high-level interface for drawing attractive statistical graphics, such as regression plots, box plots, and so on
* Seaborn makes creating plots very efficient
	* Therefore with Seaborn you can generate plots with code that is 5 times less than with Matplotlib


#### Title: Visualizing Geospatial Data

##### Introduction to Folium

> What is really interesting about the maps created by Folium is that they are interactive, so you can zoom in and out after the map is rendered, which is a super useful feature

* **Folium** is a powerful data visualization library in Python that was built primarily to **help** people **visualize geospatial data**
* With Folium, you can create a map of any location in the world as long as you know its **latitude** and **longitude** values
* You can also create a map and superimpose markers as well as clusters of markers on top of the map for cool and very interesting visualizations
* You can also create maps of different styles such as **street level map**, **stamen map**, and a couple others
* The default map style is the open street map, which shows a street view of an area when you're zoomed in and shows the borders of the world countries when you're zoomed all the way out
* Another amazing feature of Folium is that you can create different map styles using the tiles parameter
* Map Styles
	* **Stamen Toner Map**
		* This style is great for visualizing and exploring river meanders and coastal zones
	* **Stamen Terrain Map**
		* This style is great for visualizing hill shading and natural vegetation colors

##### Choropleth Maps

* A choropleth map is a thematic map in which areas are shaded or patterned in proportion to the measurement of the statistical variable being displayed on the map, such as population density or per capita income
* The higher the measurement the darker the color
* In order to create a choropleth map of a region of interest, Folium requires a **Geo JSON** file that **includes geospatial data** of the region
* For a choropleth map of the world, we would need a **Geo JSON** file that lists each country along with any geospatial data to define its borders and boundaries



