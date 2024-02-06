# python-api-challenge

# Module 6 Challenge

This project consists of two parts: [`WeatherPy`](https://github.com/myhre062/python-api-challenge/blob/main/WeatherPy/WeatherPy.ipynb) and [`VacationPy`](https://github.com/myhre062/python-api-challenge/blob/main/WeatherPy/VacationPy.ipynb). Both projects leverage Python requests, APIs, and JSON traversals to answer real-world data analysis questions.

## Instructions

1. Clone the repository to your local machine.

2. Obtain API keys for OpenWeatherMap and Geoapify and save them in a `api_keys.py` file.

3. Run Jupyter notebook and open either `WeatherPy.ipynb` or `VacationPy.ipynb`.

4. Execute the cells in the notebook to generate plots, dataframes, and interactive maps.

## Dependencies

To run these notebooks, you need to install several Python packages. Ensure you have the following packages installed:

- pandas

- matplotlib

- numpy

- requests

- citipy

- hvplot

Additionally, you will need API keys for OpenWeatherMap and Geoapify API access.

## WeatherPy

The `WeatherPy` notebook is focused on visualizing the weather of 500+ cities across the world of varying distance from the equator. This script utilizes the [OpenWeatherMap API](https://openweathermap.org/api) to perform a series of scatter plots to showcase the following relationships:

- Temperature (F) vs. Latitude

- Humidity (%) vs. Latitude

- Cloudiness (%) vs. Latitude

- Wind Speed (mph) vs. Latitude

The script also divides the world into northern and southern hemispheres to perform linear regression on each relationship. This step further investigates the weather patterns. A notable part of this analysis is the use of the `citipy` library to select cities based on latitude and longitude.  

### Key Features

- Generates a list of cities based on random latitude and longitude.

- Retrieves weather data from OpenWeatherMap API.

- Visualizes the data with Matplotlib to analyze the weather patterns.

- Performs linear regression and plots data with regression lines for northern and southern hemispheres.

## VacationPy

The `VacationPy` notebook uses weather data to help plan future vacations. It involves:

- Loading the CSV generated in `WeatherPy`.

- Using jupyter-gmaps and the Geoapify API to create a heat map that displays the humidity for every city from the part I of the homework.

- Narrowing down the DataFrame to find ideal weather conditions for a vacation. 

- Using Geoapify API to find the first hotel for each city located within 5000 meters of the coordinates.

- Plotting the hotels on top of the humidity heatmap with each pin containing the **Hotel Name**, **City**, and **Country**.

### Key Features

- Uses `hvplot.pandas` for plotting interactive maps with hover tool capabilities.

- Filters data to find ideal vacation spots based on weather conditions.

- Utilizes Geoapify API to find hotels near the selected cities.

- Plots an interactive map with the locations of the hotels, cities, and their respective weather data.

## Acknowledgments

- OpenWeatherMap API

- Geoapify API

## Limitations and Considerations

The `WeatherPy` and `VacationPy` projects provide insightful visualizations and vacation planning tools through the OpenWeatherMap and Geoapify APIs, yet they come with inherent limitations. The linear regression analysis assumes simple linear relationships, potentially oversimplifying the complex dynamics of weather patterns. Selection criteria for vacation spots are based on specific thresholds, which might not align with all user preferences. Despite these limitations, the projects offer valuable insights, demonstrating the potential of API integration and data visualization for real-world applications.