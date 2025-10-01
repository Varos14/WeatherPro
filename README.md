# 🌤️ Weather Pro - Advanced Weather Application

A comprehensive, modern weather application that provides detailed weather information, forecasts, air quality data, and interactive maps. Built with vanilla HTML, CSS, and JavaScript, featuring a professional interface and extensive functionality.

## ✨ Key Features

### 🎯 Core Weather Data
- **Current Weather**: Real-time temperature, conditions, and detailed metrics
- **Extended Forecasts**: Hourly (48h), daily (7-day), and extended (14-day) predictions
- **Weather Details**: Humidity, wind speed/direction, pressure, visibility, dew point, UV index
- **Sunrise/Sunset**: Accurate times with automatic location detection

### 🗺️ Advanced Features
- **Interactive Weather Maps**: Radar, satellite, temperature, precipitation, and wind overlays
- **Air Quality Index**: Real-time AQI with pollutant levels and health recommendations
- **Weather Alerts**: Severe weather warnings and customizable notifications
- **City Comparison**: Side-by-side weather comparison between multiple locations

### 🎨 User Experience
- **Dark/Light Themes**: Toggle between themes with dynamic weather-based backgrounds
- **Unit Conversion**: Seamless switching between Celsius/Fahrenheit, metric/imperial
- **Favorite Locations**: Save and quickly access your frequently checked cities
- **Search History**: Recent searches with intelligent autocomplete suggestions
- **Responsive Design**: Optimized for desktop, tablet, and mobile devices

### 🔧 Smart Features
- **Geolocation**: Automatic weather updates based on your current location
- **Coordinate Search**: Enter precise latitude/longitude for any location
- **Weather Notifications**: Browser notifications for severe weather and daily forecasts
- **Local Storage**: Persistent favorites, settings, and search history

## 🚀 Getting Started

### Prerequisites

- A modern web browser (Chrome, Firefox, Safari, Edge)
- An internet connection
- A free API key from OpenWeatherMap

### Setup Instructions

1. **Clone or Download** this repository to your local machine

2. **Get a Free API Key**:
   - Visit [OpenWeatherMap.org](https://openweathermap.org/api)
   - Click "Sign Up" to create a free account
   - Navigate to "API Keys" in your account dashboard
   - Copy your API key

3. **Configure the API Key**:
   - Open `script.js` in your code editor
   - Find line 7 in the CONFIG object: `API_KEY: 'YOUR_API_KEY_HERE'`
   - Replace `'YOUR_API_KEY_HERE'` with your actual API key:
     ```javascript
     API_KEY: 'your_actual_api_key_here'
     ```

4. **Launch the App**:
   - Open `index.html` in your web browser
   - Allow location access when prompted (optional)
   - Start checking the weather!

## 📱 How to Use

### Automatic Location Detection
- Click the "Use My Location" button
- Allow location access when prompted by your browser
- Weather data for your current location will be displayed automatically

### Advanced Search Options
- **City Search**: Type a city name to see intelligent search suggestions
- **Coordinates**: Click the coordinates button to search by exact latitude/longitude
- **Recent Searches**: Click on any item in your recent search history
- **Favorites**: Save favorite locations for one-click access

### Interactive Interface
- **Tab Navigation**: Switch between Current, Forecast, Map, Air Quality, and Compare tabs
- **Theme Toggle**: Switch between light and dark themes
- **Units Toggle**: Switch between metric and imperial units
- **Forecast Views**: Toggle between hourly, daily, and extended forecasts
- **Map Controls**: Change map layers and opacity for different weather visualizations

### Comprehensive Weather Data
- **Current Conditions**: Temperature, feels like, weather description, high/low
- **Detailed Metrics**: Humidity, pressure, visibility, wind speed/direction, dew point, UV index
- **Hourly Forecast**: 48-hour predictions with temperature and conditions
- **Daily Forecast**: 7-day outlook with high/low temperatures
- **Air Quality**: AQI level with pollutant measurements (PM2.5, PM10, NO₂, O₃, SO₂, CO)
- **Health Recommendations**: Activity suggestions based on air quality

## 🛠️ Technical Details

### Built With
- **HTML5**: Semantic markup with modern web components
- **CSS3**: Advanced styling with CSS Grid, Flexbox, CSS Variables, and animations
- **JavaScript (ES6+)**: Modules, async/await, localStorage, geolocation API, canvas API
- **External Libraries**:
  - **Font Awesome 6.0**: Comprehensive icon library
  - **Leaflet**: Interactive maps for weather visualization
  - **Chart.js**: Weather data charts and graphs

### API Integration
- **Current Weather API**: Real-time weather conditions
- **One Call API**: Hourly, daily, and extended forecasts with historical data
- **Geocoding API**: City name to coordinates conversion with search suggestions
- **Air Pollution API**: Air quality index and pollutant measurements
- **Weather Maps API**: Tile layers for radar, satellite, and weather overlays
- Comprehensive error handling with user-friendly messages
- Support for both metric and imperial units
- Rate limiting and caching for optimal performance

### Architecture
- **Modular Design**: Separated concerns with distinct modules for different features
- **State Management**: Centralized application state with localStorage persistence
- **Event-Driven**: Comprehensive event handling for user interactions
- **Responsive**: Mobile-first design with progressive enhancement
- **Performance**: Lazy loading, efficient DOM updates, and optimized API calls

### Browser Compatibility
- Chrome 60+ (full support)
- Firefox 55+ (full support)
- Safari 12+ (full support)
- Edge 79+ (full support)
- IE 11+ (basic functionality)

## 🎨 Customization

### Theme Customization
Edit CSS variables in `style.css` for comprehensive theme control:
```css
:root {
    --primary-color: #74b9ff;
    --secondary-color: #0984e3;
    --accent-color: #fdcb6e;
    --success-color: #00b894;
    --warning-color: #fdcb6e;
    --error-color: #e74c3c;
    --background-gradient: linear-gradient(135deg, #74b9ff 0%, #0984e3 100%);
    --card-background: rgba(255, 255, 255, 0.95);
}
```

### Adding Weather Data
1. Add new HTML elements in the appropriate tab sections
2. Update the corresponding display functions in `script.js`
3. Add styling in `style.css` following the existing patterns
4. Update API calls if additional data endpoints are needed

### Custom Weather Icons
Update the `getWeatherIconClass()` function to customize weather icons:
```javascript
function getWeatherIconClass(weatherMain, iconCode) {
    const iconMap = {
        'Clear': 'fas fa-sun',
        'Clouds': 'fas fa-cloud-sun',
        'Rain': 'fas fa-cloud-rain',
        // Add your custom mappings...
    };
    return iconMap[weatherMain] || 'fas fa-sun';
}
```

### Map Layer Customization
Add new weather map layers by updating the map controls:
```html
<select id="mapLayer">
    <option value="temp_new">Temperature</option>
    <option value="your_layer">Custom Layer</option>
</select>
```

## 🔧 Troubleshooting

### Common Issues

**"Please add your OpenWeatherMap API key" Error**
- Replace `'YOUR_API_KEY_HERE'` in the CONFIG object at the top of `script.js`
- Verify your API key is active (can take up to 10 minutes after creation)
- Ensure you have an active OpenWeatherMap account

**"City not found" Error**
- Check the spelling of the city name
- Try using the search suggestions that appear as you type
- Include country or state names for better results (e.g., "London, UK")
- Use the coordinates search for precise locations

**Location Access Denied**
- Use the city search or coordinates feature instead
- Check your browser's location permissions in settings
- Try refreshing the page and allowing location access
- On mobile, ensure location services are enabled

**Weather Maps Not Loading**
- Ensure your API key is valid and active
- Check that Leaflet library is loading properly
- Verify your internet connection for map tiles

**Notifications Not Working**
- Allow notifications in your browser settings
- Check that the app has notification permissions
- Ensure you've enabled notifications in the app settings

### Browser Console Errors
Press F12 to open developer tools and check the Console tab for detailed error messages.

## 📊 API Usage & Limits

- **Free Tier**: 1,000 API calls per day (sufficient for personal use)
- **Rate Limit**: 60 calls per minute
- **Data Updates**: Current weather (every 10 minutes), Forecasts (every 3 hours)
- **Coverage**: 200,000+ cities worldwide plus coordinate-based requests
- **APIs Used**:
  - Current Weather Data
  - One Call API (forecasts, historical data)
  - Geocoding API (city search)
  - Air Pollution API
  - Weather Maps API

## 🤝 Contributing

Contributions are welcome! The app now includes most essential modern weather features. Here are some advanced enhancement ideas:

### Completed Features ✓
- ✓ Extended weather forecasts (hourly, daily, 14-day)
- ✓ Interactive weather maps with multiple layers
- ✓ Air quality monitoring and health recommendations
- ✓ Weather alerts and browser notifications
- ✓ Multiple favorite locations with quick access
- ✓ Dark/light theme with dynamic weather backgrounds
- ✓ Comprehensive unit conversion (metric/imperial)
- ✓ Advanced search with autocomplete and coordinates
- ✓ Recent search history and persistent settings
- ✓ Responsive design for all device sizes

### Future Enhancement Ideas
- Weather radar animations
- Severe weather tracking and alerts
- Weather widgets for external integration
- Historical weather data visualization
- Weather-based activity recommendations
- Social sharing of weather conditions
- Offline data caching for PWA functionality
- Weather camera integrations
- Climate change data and trends

## 📝 License

This project is open source and available under the [MIT License](LICENSE).

## 🙏 Acknowledgments

- **[OpenWeatherMap](https://openweathermap.org/)** - Comprehensive weather data APIs
- **[Font Awesome](https://fontawesome.com/)** - Beautiful icon library
- **[Leaflet](https://leafletjs.com/)** - Interactive mapping library
- **[Chart.js](https://www.chartjs.org/)** - Data visualization charts
- **OpenStreetMap Contributors** - Map tile data
- The weather enthusiast community for inspiration and feedback

## 📊 App Statistics

- **Lines of Code**: ~1,400+ (HTML, CSS, JavaScript)
- **Features**: 25+ major features implemented
- **API Endpoints**: 5 different OpenWeatherMap APIs
- **Supported Locations**: 200,000+ cities worldwide
- **Responsive Breakpoints**: 4 different screen sizes
- **Theme Options**: Light/Dark with dynamic weather backgrounds
- **Data Points**: 20+ weather and air quality metrics

## 🎆 Version History

- **v2.0** - Complete rewrite with advanced features, forecasts, maps, air quality
- **v1.0** - Basic weather app with current conditions

---

<div align="center">

**Weather Pro** - *Your comprehensive weather companion*

Made with ❤️ by developers who love beautiful, functional weather apps

*"The weather affects everyone - make it accessible to all"*

</div>
