# UFO

# Deliverable 2: UFO Sightings

## Overview of Project:

Dana created a webpage and interactive table which shows data on UFO sightings. She'd like to expand her search criteria options to provide a more in-depth analysis of UFO sightings by allowing users to filter for multiple criteria at the same time. The filters included searching by date, city, state, country and shape.

## Results:

The app.js file starts out by importing the dataset from data.js and I went ahead and cleared out any existing data. Next I looped through each object in the data and appended a row and cells for each value in the row which was later filled by the values of each cell. 

The index.html file was used from my classwork which had all the constructs of the webpage which would display the data. I added the new syntax for the Filter Search table which would take the user's inputs for dates, city, state, country and UFO shape. 

Back on app.js, I created a variable to keep track of all the filters as an object. The function updateFilters() was used to update the filters. I then again saved the element, value and id of the filter that was changed as a variable. If the filter value was entered, I then added that filterID and value to the filters list. Otherwise the filter would be cleared from the filters object.

The function was afterwards called to apply all filters and rebuild the table. Function filterTable was used to filter the table when the data is entered. The filtered data was then set to tableData. Afterwards I used 
Object.entries(filters).forEach(([key, value]) = { 
filteredData=filteredData.filter(row=>row[key]===value);
});
to loop through all of the filters and keep any data that matches the filter values. Finally, the table was rebuilt using the filtered data. Also, an event to listen for changes to each filter was also attached. Finally the table will be built when the page loads. 

Now that the JavaScript and HTML coding is complete, let's look at the webpage:

![Screen Shot 2022-05-12 at 2 13 16 PM](https://user-images.githubusercontent.com/95712234/168141444-26310e02-a25d-46ba-a223-34ec811e4181.png)


In order to conduct a search, one may enter the required info in the 'date', 'city', 'state', 'country' and/or 'shape' search boxes to filter the  UFO sightings data. Upon entering the desired criteria and pressing 'enter', the webpage will produce the filtered results. In order to refresh the page, one may click the 'UFO Sightings' button located in the top left corner of the webpage.


## Summary:

I found working on this assignment intriguing and it gave me a better understanding of JavaScript and HTML. In my opinion, a drawback to the design was that an average user would not realize that the site has the means to 'refresh' the table. I would change two items on this webpage to make it more user-friendly. First I would change the location of the 'UFO Sightings' button to below the criteria input boxes as it it not very obvious to a user. Secondly I would make the button stand out more visually as a 'Refresh button' to help the user navigate the site better.


