
# SkyCast: 5-Day Weather Forecast Web App

SkyCast is a web application that provides a 5-day weather forecast for a selected city using OpenWeatherMap's API. This app offers a streamlined interface for viewing minimum and maximum temperature trends, impending weather alerts, cloud coverage, wind speeds, and sunrise/sunset times. Users can choose the display unit (Celsius or Fahrenheit) and visualize the data through line or bar graphs.

## Table of Contents
1. [Features](#features)
2. [Setup and Installation](#setup-and-installation)
3. [Usage](#usage)
4. [Code Overview](#code-overview)
5. [Acknowledgments](#acknowledgments)

---

### Features

- **City Selection:** Users can enter the name of a city to view its forecast.
- **Temperature Units:** Choose between Celsius and Fahrenheit.
- **Graph Types:** Select between line and bar graphs for visualizing temperature trends.
- **Weather Alerts:** Get alerts for impending weather events like fog, rain, storms, etc.
- **Cloud Coverage and Wind Speed:** Current cloud coverage and wind speed display.
- **Sunrise and Sunset Times:** Shows sunrise and sunset times in the local timezone of the selected city.

### Setup and Installation

1. **Clone the Repository:**
    ```bash
    git clone https://github.com/username/SkyCast.git
    cd SkyCast
    ```

2. **Install Required Libraries:**
    Ensure you have Python 3 installed. Then, install the necessary packages:
    ```bash
    pip install streamlit pyowm pytz plotly matplotlib
    ```

3. **API Key for OpenWeatherMap:**
    - Sign up on [OpenWeatherMap](https://home.openweathermap.org/users/sign_up) to get your API key.
    - Replace the value of `API_key` in the code with your actual API key.

4. **Run the Application:**
    ```bash
    streamlit run app.py
    ```

### Usage

1. Enter the city name in the **City Name** input box.
2. Select your preferred **Temperature Unit** and **Graph Type** from the sidebar.
3. Click the **SUBMIT** button to load the forecast data and display alerts.
4. The app will display temperature trends, weather alerts, cloud coverage, wind speed, and sunrise/sunset times.

### Code Overview

1. **User Interface:** Created with Streamlit, featuring custom markdown and style settings for a dynamic background.
2. **Temperature Data:** `get_temperature()` retrieves 5-day minimum and maximum temperatures.
3. **Plotting Graphs:** Both line and bar graphs are available for temperature trends, using Plotly.
4. **Additional Weather Updates:** Includes alerts for weather events, cloud coverage, wind speed, and sunrise/sunset times using the OpenWeatherMap API.
5. **Helper Functions:**
    - `draw_bar_chart()` and `draw_line_chart()` handle bar and line graph rendering.
    - `other_weather_updates()`, `cloud_and_wind()`, and `sunrise_and_sunset()` provide additional weather details.

### Acknowledgments

- **API:** OpenWeatherMap for providing weather data.
- **Libraries:** Streamlit, Plotly, PyOWM, Pytz, Matplotlib.


