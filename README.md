# Weather & Air Quality App

A location-aware web application that retrieves and displays current weather and air-quality information using JavaScript, browser geolocation, and external APIs.

The application detects the user's geographic coordinates and uses them to retrieve local temperature, sunrise and sunset times, Air Quality Index (AQI), PM2.5, and PM10 measurements.

## Features

* **Location detection** — Uses the browser's Geolocation API to determine latitude and longitude, with the Google Geolocation API available as a fallback.
* **Current weather** — Retrieves local temperature plus sunrise and sunset times.
* **Air-quality information** — Displays U.S. AQI, PM2.5, and PM10 measurements.
* **AQI interpretation** — Converts numerical AQI values into descriptive categories for easier interpretation.
* **Responsive interface** — Designed for use on desktop and mobile browsers.

## How It Works

The application follows a simple location-to-data workflow:

1. The browser attempts to obtain the user's latitude and longitude through geolocation.
2. If browser-based location detection is unavailable, the application can use the Google Geolocation API as a fallback.
3. The coordinates are passed to the Open-Meteo Weather API to retrieve local weather information.
4. The same location is used to query the Open-Meteo Air Quality API.
5. JavaScript processes the API responses and displays the resulting weather and air-quality information in the browser.

This approach allows the application to provide location-specific information without requiring the user to manually enter a city or ZIP code.

## Technologies

* HTML5
* CSS3
* Vanilla JavaScript
* `XMLHttpRequest`
* Browser Geolocation
* Google Geolocation API
* Open-Meteo Weather API
* Open-Meteo Air Quality API
* Git/GitHub

## API Integration

### Open-Meteo Weather API

The application uses the Open-Meteo Weather API to retrieve weather information for the detected coordinates, including:

* Current temperature
* Sunrise time
* Sunset time

### Open-Meteo Air Quality API

The Air Quality API provides location-specific environmental measurements, including:

* U.S. Air Quality Index (AQI)
* PM2.5
* PM10

The application interprets the returned AQI value and presents the corresponding air-quality category to the user.

### Google Geolocation API

The Google Geolocation API provides an alternative method of obtaining geographic coordinates when browser-based geolocation is unavailable.

Using a fallback illustrates one of the practical considerations involved in building location-aware web applications: a service may need more than one method for obtaining required data when browser behavior, permissions, or other conditions vary.

## Setup

### Prerequisites

You will need:

* A modern web browser
* An internet connection for API requests
* A Google Cloud API key with the Geolocation API enabled if you want to use the Google fallback

### Installation

Clone the repository:

```bash
git clone https://github.com/powerbar/weather-air-quality-app.git
```

Open the project directory and locate `index.html`.

If using the Google Geolocation fallback, replace the API-key placeholder in the JavaScript with your Google API key:

```javascript
const GOOGLE_API_KEY = "YOUR_ACTUAL_KEY";
```

Then open `index.html` in a web browser.

> **Security note:** Do not commit a private API key to a public GitHub repository. For a production application, API credentials should be handled using an appropriate secure configuration method rather than being embedded directly in client-side source code.

## Using the Application

When the application opens:

1. Allow location access if the browser requests permission.
2. The application obtains your latitude and longitude.
3. Weather and air-quality data are requested for that location.
4. The results are displayed in the browser.

The interface displays:

* Latitude and longitude
* Temperature in °F
* Sunrise and sunset times
* U.S. Air Quality Index and category
* PM2.5 level
* PM10 level

## Air Quality Index Categories

| AQI     | Category                       |
| ------- | ------------------------------ |
| 0–50    | Good                           |
| 51–100  | Moderate                       |
| 101–150 | Unhealthy for Sensitive Groups |
| 151–200 | Unhealthy                      |
| 201–300 | Very Unhealthy                 |
| 301+    | Hazardous                      |

Presenting the AQI category alongside the numerical value makes the API output easier for users to interpret.

## Browser Compatibility and Limitations

The application works best in Firefox and Chrome.

Known limitations include:

* Safari may encounter geolocation issues in some cases.
* The application requires an active internet connection because weather and air-quality information comes from external APIs.
* Google Geolocation API requests are subject to Google Cloud usage limits and quotas.
* Location access depends on browser permissions and browser behavior.

## Possible Enhancements

Potential improvements include:

* Seven-day weather forecasts
* Weather-condition descriptions such as sunny, cloudy, or rainy
* Support for multiple locations
* Saved favorite locations
* Weather alerts

Additional improvements could also focus on error handling and the presentation of API failures or unavailable location data.

## Project Background

I developed this application as a JavaScript 1 course project at Mission College in November 2025. The project provided hands-on experience with JavaScript, browser geolocation, asynchronous API requests, external data sources, and presenting location-specific information in a web interface.

The project also provided practical experience documenting a small web application for other users and developers.

## Acknowledgments

* Open-Meteo — Weather and air-quality APIs
* Google Cloud — Geolocation API
* Mission College — JavaScript 1

## Author

**Hsiu-Hsien Chen**

GitHub repository:
https://github.com/powerbar/weather-air-quality-app

## License

This project is open source and available for educational purposes.
