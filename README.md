# weather-app

# Weather App

A simple and elegant weather application that allows users to check current weather conditions for any city around the world.

## Features

- **Real-time Weather Data**: Get up-to-date weather information through the OpenWeatherMap API
- **City Search**: Look up weather data for any city globally
- **Visual Weather Indicators**: Weather conditions displayed with appropriate icons
- **Key Metrics**: View temperature, humidity, and wind speed at a glance
- **Error Handling**: Clear feedback when a city cannot be found
- **Responsive Design**: Works well on both desktop and mobile devices

## How It Works

The application uses the OpenWeatherMap API to fetch current weather data. Users can:

1. Enter a city name in the search box
2. Click the search button or press Enter to submit
3. View the resulting weather information, including:
   - Current temperature (in Celsius)
   - City name
   - Weather condition icon
   - Humidity percentage
   - Wind speed (km/h)

## Technical Implementation

### HTML Structure

- Clean, card-based layout for weather information
- Search interface with text input and button
- Dedicated sections for displaying weather data and error messages

### JavaScript Functionality

- Asynchronous API calls using `fetch` and `async/await`
- Dynamic content updates based on API responses
- Error handling for invalid city names or failed requests
- Event listeners for both button clicks and keyboard input

### API Integration

- Uses OpenWeatherMap's weather data API
- Metric units for temperature and wind speed
- Weather condition mapping for appropriate icon display

## Setup and Usage

1. Clone the repository
2. Open `index.html` in your browser
3. Enter a city name and press Enter or click the search button
4. View the current weather conditions for that location

## Dependencies

- OpenWeatherMap API (requires an API key)
- Weather icons (included in the images folder)

## Future Enhancements

- Weather forecast for upcoming days
- Unit conversion (Celsius/Fahrenheit)
- Geolocation to automatically detect user's city
- Additional weather metrics (feels like, pressure, visibility)
- Saving favorite locations
