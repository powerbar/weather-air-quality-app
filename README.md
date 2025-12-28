# Weather & Air Quality App

A web application that displays current weather conditions and air quality data based on your geographic location.

## Features

- 📍 **Geolocation Detection**: Uses browser geolocation with Google Geolocation API fallback
- 🌡️ **Weather Data**: Displays current temperature, sunrise, and sunset times
- 🌫️ **Air Quality**: Shows US AQI, PM2.5, and PM10 levels with color-coded categories
- 📱 **Responsive Design**: Works on desktop and mobile devices

## Technologies Used

- HTML5
- CSS3
- JavaScript (Vanilla JS with XMLHttpRequest)
- Google Geolocation API (as fallback, when API enabled)
- Open-Meteo Weather API
- Open-Meteo Air Quality API

## APIs Used

1. **Google Geolocation API** - Fallback location detection when browser geolocation is denied
2. **Open-Meteo Weather API** - Free weather forecast data
3. **Open-Meteo Air Quality API** - Free air quality measurements

## Setup Instructions

### Prerequisites

- A Google Cloud API key with Geolocation API enabled
- A modern web browser (Firefox or Chrome recommended)

### Installation

1. Clone this repository:
```bash
   git clone https://github.com/YOUR-USERNAME/weather-air-quality-app.git
```

2. Open the HTML file in a text editor

3. Replace `YOUR_API_KEY_HERE` on line 64 with your actual Google API key:
```javascript
   const GOOGLE_API_KEY = "YOUR_ACTUAL_KEY";
```

4. Open `index.html` in your web browser

## Usage

1. Open the application in your browser
2. Allow location access when prompted
3. View your current:
   - Latitude and Longitude
   - Temperature (°F)
   - Sunrise and Sunset times
   - Air Quality Index with category
   - PM2.5 and PM10 levels

## Browser Compatibility

✅ **Best Performance**: Firefox, Chrome  
⚠️ **Limited Support**: Safari (may have geolocation issues)

## Screenshots

*(You can add screenshots here later)*

## Air Quality Index Categories

| AQI Range | Category | Color |
|-----------|----------|-------|
| 0-50 | Good | Green |
| 51-100 | Moderate | Gold |
| 101-150 | Unhealthy for Sensitive Groups | Orange |
| 151-200 | Unhealthy | Red |
| 201-300 | Very Unhealthy | Purple |
| 301+ | Hazardous | Maroon |

## Known Issues

- Safari browser may fail to detect location in some cases
- Requires active internet connection for API calls
- Google Geolocation API has usage limits (check your quota)

## Future Enhancements

- [ ] Add 7-day weather forecast
- [ ] Display weather conditions (cloudy, sunny, rainy)
- [ ] Add multiple location support
- [ ] Save favorite locations
- [ ] Add weather alerts

## Course Information

**Course**: JavaScript 1  
**Project**: Week 11X - Geolocation and Weather  
**Author**: Hsiu-hsien Chen  
**Date**: November 5, 2025

## License

This project is open source and available for educational purposes.

## Acknowledgments

- Open-Meteo for providing free weather and air quality APIs
- Google Cloud for Geolocation API
- Mission College JavaScript 1 course
```

---

## Step 5: Enable GitHub Pages (Optional - to access via URL)

1. Go to your repository **Settings**
2. Scroll down to **"Pages"** in the left sidebar
3. Under **"Source"**, select **"main"** branch
4. Click **"Save"**
5. Wait a few minutes, then your site will be live at:
```
   https://powerbar.github.io/weather-air-quality-app/
