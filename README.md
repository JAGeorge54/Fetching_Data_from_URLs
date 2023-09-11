# Fetching_Data_from_URLs
Module 9 Codio Assignment
1. Fetching Data From Multiple Sources Asynchronously
A web page pulls data from multiple sources using asynchronous calls. The web page will use the data when it is received, but not necessarily in the order that it was requested. An example of this is a website that shows multiple pictures on the main page. The page may load those pictures asynchronously and show them as the data is received. If this is the case, then the pictures will show up at different times depending on how fast the request goes out and the response comes back.
As shown in the videos this week, an asynchronous fetch is a request from one website to another for data. Using the await keyword, you can wait for a response to come back before continuing to execute your code.
The following code may be used as an example on how to fetch data from a URL while using the await keyword:
Another way to wait for a response to come back before continuing to execute your code is with a promise (p is the promise in the below example):
For more information on promises feel free to read all about them on MDN - https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise
In this activity, there are two steps
First, you will fetch all the weather data from the OpenWeather API
Second, you will identify the specific weather data to show based on a given city name
Step 1 - Your first step in this activity is to fetch data from the OpenWeather API
You will use the following URLs. But first, replace YOUR-API-KEY-HERE with the API key you generated on OpenWeather.
https://api.openweathermap.org/data/2.5/weather?q=London,uk&APPID=YOUR-API-KEY-HERE
https://api.openweathermap.org/data/2.5/weather?q=Houston&APPID=YOUR-API-KEY-HERE
https://api.openweathermap.org/data/2.5/weather?q=Lisbon&APPID=YOUR-API-KEY-HERE
https://api.openweathermap.org/data/2.5/weather?q=Budapest&APPID=YOUR-API-KEY-HERE
To accomplish this task, you need to:
Call the makeRequest function to asynchronously fetch the data from the URLs and return the data.
Store the data in the provided Array[] variable named dataArray, which is a parameter in the fetchData function, using the Array.push method.
Run logic to check which data are for the city Lisbon
Call the addLisbonDataToDocument function described in the second half of this task with your Lisbon data and the dataArray that you filled up.
The structure of the array should look like this:
[data1, data2, data3, data4];
where each data variable holds the result from each of the four URLs provided.
The code for fetching, storing, and printing the fetched data should all reside within the fetchData function in the provided fetchUrls.js JavaScript file.
An example response from one of these URLs will result in the following data:
Note that the URL appears to be getting weather data related to a certain city which is specified in the URL. In the URL, this parameter is sent as q=[cityname], such as London, Budapest, Houston, or Lisbon. In the response, you can also see a field called “name” where that city should match whatever was sent in the URL.
Hints:
Use the await keyword for both sending the request out to URL and fetching the data response as shown in the fetch example above.
Be sure to parse the received data as text, just like the example, in order to proceed with the second step of this exercise.