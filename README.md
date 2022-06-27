# UofM-Data-Viz-Analytics-Boot-Camp
# Ron Hankey - University of Minnesota Data Visualization and Analytics Boot Camp
#                   Assignment: Challenge 11 - UFOs
#                           Student: Ron Hankey
#                           Date: June 15, 2022

# Module 11 - UFO Sightings with JavaScript

## Overview of Project
In this challenge provide a more in-depth analysis of UFO sightings by allowing users to filter for multiple criteria at the same time. In addition to the date, you’ll add table filters for the city, state, country, and shape.

## Analysis Using Javascript
* Filter UFO sightings on multiple criteria
* A written report on the UFO analysis (README.md)
In order to run the application you need to start a simple web server in Python. 
1. In Anaconda, open the command prompt, change the directory to where the application exists (D:\Data_Visualization_and_Analytics_Boot_Camp\11_Challenge)
2. Start the simple webserver from the Anaconda command prompt: python -m http.server
3. Open the application: http://localhost:8000/index.html

**Deliverable 1** 
* The list element that creates the button is removed, and there are five list elements for filtering 
	in the index.html file:

![Filtering](https://github.com/lykkelig/UFOs/blob/main/static/images/UFO_Web_Page_Selection.png)

* The event listener is modified to detect changes to each filter in the app.js file.
*   	// 4a. Save the element that was changed as a variable.
*   	let changedElement = d3.select(this);

* The updateFilters() function saves the element, value, and the id of the filter that was changed:
		*See in app.js: function updateFilters() for complete code*
* The filterTable() function loops through all of the filters and keeps any data that matches the filter values.
		*See in app.js: function filterTable(obj)* 
![Entries](https://github.com/lykkelig/UFOs/blob/main/static/images/Entries.png)

* The webpage filters the table correctly based on user input: 
![Filtering](https://github.com/lykkelig/UFOs/blob/main/static/images/Filter_Search.png)

## Summary  (Deliverable 2) 
* Finished WebPage: ![UFO](https://github.com/lykkelig/UFOs/blob/main/static/images/UFO_Web_Page.png)
* Drawback: There are no drop down elements to aid in the selection process.

* The application is rather simple, it loads a table of UFO sightings that are located on the local host. A more robust application would use a database on a cloud platform that would keep the UFO sighting data updated. Although a simple application, it has it's uses allowing a user with no network or Internet connections to query UFO sightings with 5 different filters. 