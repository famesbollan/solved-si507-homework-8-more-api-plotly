Download Link: https://assignmentchef.com/product/solved-si507-homework-8-more-api-plotly
<br>
<strong>Homework Objectives:</strong>

<ul>

 <li>Be able to read API documentation and find the necessary API endpoints to perform the task.</li>

 <li>Understand the basic use of Plotly Mapbox graph and be able to map simple data onto a Plotly map</li>

</ul>




<strong>Supporting Material:</strong>

<ul>

 <li>Foursquare API for venues search<a href="https://developer.foursquare.com/docs/api/venues/search">https://developer.foursquare.com/docs/api/venues/search</a></li>

 <li>Plotly with Mapbox (to show street level map)</li>

</ul>

<a href="https://plot.ly/python/scattermapbox/">https://plot.ly/python/scattermapbox/</a>




<strong>Starter Files:</strong>

<ul>

 <li><a href="https://www.dropbox.com/s/mbdi8e89pwqwxof/hw8.py?dl=0">py</a></li>

 <li><a href="https://www.dropbox.com/s/cuc8lc1a5cal4t4/secret.py?dl=0">py</a></li>

</ul>




<strong>Part 1: Get photos for places in a city using Foursqure APIs (10 pts)</strong>



Here’s what your program should do: when you run it, it should ask the user for what city the user wants to do a search. After the user enters the city, it should ask what kind of places the user wants to search for. This should be a location type, such as “museum,” “coffee shop,” “park” and so on. Your program should then access the Foursquare API to get a list of “venues” that the user searched for near the location that the user entered. Limit the result set to 25. For each venue in the result set, you should then do a search using Foursquare’s Venue Photos API to get a photo for that place Your program should then print the name of the venue, its address, followed by the photo ID that was returned by the Venue Photos API.




So, the run of the program would look something like this:




$ python3 hw8.py

In what city do you want to search: Ann Arbor

What kind of place are you looking for: coffee shop

Venue: Comet Coffee

Address: 16 Nickels Arcade, Ann Arbor, MI 48104

Photo id: 51e4151c498e60b5d17bc721




Venue: Lab

Address: 505 E Liberty St # 300, Ann Arbor, MI 48104

Photo id: 53d5894151c498e60b5d17df







You should be using cache for this assignment.

<strong>Part 2: Map onto Plotly (10 points)</strong>




For the second part, use the data you got from the photo search to construct the full URL for the the image you got from the Venue Photos API. Your program should then display each venue in your result list on a plotly map. When you hover over a venue marker, it should pop up the text label with the venue’s name and the URL of the image for that place.




We will be using <a href="https://plot.ly/python/scattermapbox/">Plotly with Mapbox</a> for this part. Mapbox is a map data provider that can make our map created on Plotly show details like streets. (Notice that for your project 2 you can use either the standard plotly map or a mapbox map.) You will need a mapbox_access_token to use Mapbox with Plotly, which has been provided for you in secret.py. Map your filtered photos from part1 using Plotly, with photo’s title and url in the text. Your plotly map should look something like this: