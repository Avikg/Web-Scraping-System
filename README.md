# Web-Scraping-System
Problem 1: Collecting and Storing structured JSON data
Your task is to collect weather data from an online API and store it in a local SQLite database
1. Use the requests or urllib3 library in Python to make API calls to the OpenWeatherMap
API (https://openweathermap.org/api ). First, you will need to sign up for a free API key.
The API allows you to access current weather data for any city in the world (it simply means
you need to include the API key in your url before sending to requests)
2. The API returns data in JSON format given a latitude and longitude. Extract the following
information from the API response:
○ City name
○ Current temperature (in Kelvin)
○ Weather description
○ Humidity (%)
○ Wind speed (meter/sec)
3. Create a SQLite database named ‘Weather.db’ and a table named ‘city_weather’ with the
following columns:
○ City
○ Temperature
○ Description
○ Humidity
○ WindSpeed
4. Insert the extracted data into the ‘city_weather’ table (note that you need to create the table
only if it does not already exist)
5. Test your system with three to five different cities of your choice, included in a test function.
   
Problem 2: Collecting, storing and processing unstructured data
Your task is to collect information about the different summer olympics from its Wikipedia page and
process the data using Python’s urllib3 / requests (to get data) and BeautifulSoup library (for
parsing/processing), and store the collected data in a SQLite database.
TASK:
1. Collect the main page of Summer Olympics Wikipedia for this task, the page is here:
https://en.wikipedia.org/wiki/Summer_Olympic_Games . Note that you might need to use
headers for fetching this page.
2. Now create a database Create a SQLite database named ‘OlympicsData.db’ and a table
named ‘SummerOlympics’ with the following columns:
○ Name (e.g. “2012 Summer Olympics”, in title of respective wikipedia pages)
○ WikipediaURL
○ Year (the year when its conducted)
○ HostCity (the city where its hosted)
○ ParticipatingNations (List of the participating nations)
○ Athletes (number of athletes)
○ Sports (list of sports)
○ Rank_1_nation
○ Rank_2_nation
○ Rank_3_nation
3. Parse the html from step 1 and extract the individual summer olympics wiki page urls for
random 2 olympics from the last 50 years, i.e., from 1968 to 2020. (hint: try to parse the
“List of Summer Olympic Games” table to get the urls and use random.sample for
random sampling)
4. For each of the pages of your two selected summer olympics, extract the data (with the help
of BeautifulSoup) mentioned in step 2 and insert in the database.
5. Then using the database print answers to the following questions:
○ What are the years you chose?
○ What is the average number of countries participating in the two olympics?
○ Print the overlap (i.e., common nations) within <Rank_1_nation, Rank_2_nation and
Rank_3_nation> for your chosen two years.
