# Weather & Travel Analysis

# Overview
This challenge utilized the [citipy Python library](https://pypi.python.org/pypi/citipy) and [OpenWeatherMap API](https://openweathermap.org/api) to analyze weather information, aiding in the planning of future vacations near the equator.

# Technologies
* Pandas
* Matplotlib
* Numpy
* Scipy

# WeatherPy
I employed the OpenWewatherMap API to retrieve weather data for cities listed in the starter code, creating a DataFrame of the results.
<img width="760" alt="Screenshot 2023-12-19 at 3 59 18 PM" src="https://github.com/samkimmmm/python-api-challenge/assets/135805393/148c06ec-1a7a-4297-a347-bd57aeeccf6a">

## Create Plots
I generated scatter plots showcasing relationships between latitude and various weather parameters:
* Latitude vs. Temperature
![image](https://github.com/samkimmmm/python-api-challenge/assets/135805393/58a1ae27-c49d-4f62-92b8-1774d97ad450)
* Latitude vs. Humidity
![image](https://github.com/samkimmmm/python-api-challenge/assets/135805393/c074d782-0c72-401f-b4a3-c8a52bfc4103)
* Latitude vs. Cloudiness
![image](https://github.com/samkimmmm/python-api-challenge/assets/135805393/77078381-1fd8-4ae6-a5e4-61c8fd0c6740)
* Latitude vs. Wind Speed
![image](https://github.com/samkimmmm/python-api-challenge/assets/135805393/bda0dacc-d314-4f90-85d5-cd1e8029217d)

## Linear Regression
Linear regressions were computed for each relationship, with separate plots for the Northern and Southern Hemispheres. Scatter plots include regression models, formulas, and r values.
## Northern Hemisphere: Temperature vs. Latitude
![image](https://github.com/samkimmmm/python-api-challenge/assets/135805393/9b9f65c5-e33a-4bde-83ce-b55304a4fc5b)
## Southern Hemisphere: Temperature vs. Latitude
![image](https://github.com/samkimmmm/python-api-challenge/assets/135805393/edb24cba-6a30-45d6-a40b-99f0ee271375)
## Northern Hemisphere: Humidity vs. Latitude
![image](https://github.com/samkimmmm/python-api-challenge/assets/135805393/a4e405e4-f19a-4e55-b15c-0bf39571d5df)
## Southern Hemisphere: Humidity vs. Latitude
![image](https://github.com/samkimmmm/python-api-challenge/assets/135805393/0cd991da-a559-4071-914a-6aeb9cd5ddb3)
## Northern Hemisphere: Cloudiness vs. Latitude
![image](https://github.com/samkimmmm/python-api-challenge/assets/135805393/5e350002-a742-48fe-b400-b743d15fa0d3)
## Southern Hemisphere: Cloudiness vs. Latitude
![image](https://github.com/samkimmmm/python-api-challenge/assets/135805393/8c4f239f-3c19-42df-ac4f-ba0771566a3a)
## Northern Hemisphere: Wind Speed vs. Latitude
![image](https://github.com/samkimmmm/python-api-challenge/assets/135805393/d9fc34f3-a2ae-40b1-b8d9-fb6c773431cd)
## Southern hemisphere: Wind Speed vs. Latitude
![image](https://github.com/samkimmmm/python-api-challenge/assets/135805393/12b3786a-e83b-4e96-9de8-9d8090decce4)

# VacationPy
The Geoapify API and the geoViews Python library were used to create map visualizations.

## Creating the map
Each point on the map represents a city from the "city_data_df" DataFrame, with the size of each point relative to its humidity rating.
<img width="1281" alt="Screenshot 2023-12-20 at 3 21 11 PM" src="https://github.com/samkimmmm/python-api-challenge/assets/135805393/fe534d43-826a-42f0-96c7-a7d704104271">

* A new DataFrame called "hotel_df" was created by narrowing down the "city_data_df" DataFrame to an ideal humidity level (10).
<img width="817" alt="Screenshot 2023-12-20 at 3 24 31 PM" src="https://github.com/samkimmmm/python-api-challenge/assets/135805393/19dc4b5e-b470-4a21-932d-75f07b8daa43">

* The Geoapify API was employed to find the first hotel within 10,000 meters of the coordinates for each city, and the hotel names were saved in the "hotel_df" DataFrame under a new column "Hotel Name".
* <img width="517" alt="Screenshot 2023-12-20 at 3 25 14 PM" src="https://github.com/samkimmmm/python-api-challenge/assets/135805393/d7b4259a-3fe3-427a-aad7-99ececff5cd7">
