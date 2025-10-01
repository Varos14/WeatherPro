# Weather App - WeatherAPI.com Setup Guide

## Overview
Your weather app has been successfully updated to use **WeatherAPI.com** instead of OpenWeatherMap. WeatherAPI.com offers a generous free tier with 1 million API calls per month and no credit card required for signup.

## API Features Available
✅ **Current Weather** - Real-time weather data  
✅ **3-Day Forecast** - Detailed hourly and daily forecasts (free tier)  
✅ **Air Quality Data** - PM2.5, PM10, NO2, O3, SO2, CO levels  
✅ **Astronomy Data** - Sunrise, sunset, moonrise, moonset  
✅ **Location Search** - City name autocomplete and suggestions  
✅ **Historical Weather** - Past weather data (paid tiers)  

## Getting Your Free API Key

### Step 1: Sign Up
1. Visit [WeatherAPI.com](https://www.weatherapi.com/)
2. Click "Get API Key Free" or "Sign Up"
3. Fill in your details (no credit card required)
4. Verify your email address

### Step 2: Get Your API Key
1. Log into your WeatherAPI.com dashboard
2. Go to the "API Keys" section
3. Copy your API key (it looks like: `a1b2c3d4e5f6g7h8i9j0k1l2m3n4o5p6`)

### Step 3: Add API Key to Your App
1. Open the `index.html` file
2. Find line 1899 where it says:
   ```javascript
   API_KEY: 'YOUR_WEATHERAPI_KEY_HERE',
   ```
3. Replace `'YOUR_WEATHERAPI_KEY_HERE'` with your actual API key:
   ```javascript
   API_KEY: 'your-actual-api-key-here',
   ```
4. Save the file

## Testing Your Setup

1. Open `index.html` in your web browser
2. Try searching for a city (e.g., "London", "New York", "Tokyo")
3. The app should load weather data successfully

## What Changed from OpenWeatherMap

### ✅ Improved Features
- **Better free tier**: 1M calls/month vs 1000/day
- **No credit card required** for signup
- **More accurate data** in many regions
- **Built-in air quality** data (no separate API calls needed)
- **Better location search** with autocomplete

### 🔄 API Differences
- **Forecast**: Limited to 3 days on free tier (vs 5 days with OpenWeather)
- **Data structure**: Different JSON response format (handled automatically)
- **Units**: Provides both metric and imperial in same response
- **Map tiles**: Switched to OpenStreetMap (free alternative)

## Free Tier Limitations
- **1 million calls per month** (approximately 1,370 calls per day)
- **3-day forecast** (vs unlimited days on paid plans)
- **Current weather + forecast** only (historical data requires paid plan)
- **Standard support** (priority support on paid plans)

## Pricing (Optional Upgrades)
- **Free**: $0/month - 1M calls
- **Developer**: $4/month - 3M calls + 14-day forecast
- **Professional**: $35/month - 10M calls + historical data
- **Enterprise**: Custom pricing for high-volume usage

## Troubleshooting

### Error: "Please add your WeatherAPI.com API key"
- Make sure you've replaced `YOUR_WEATHERAPI_KEY_HERE` with your actual API key
- Check that there are no extra quotes or spaces around your API key

### Error: "City not found" 
- Try different search terms (e.g., "New York, NY" instead of just "NYC")
- Check your internet connection
- Verify your API key is correct

### No data appearing
- Open browser developer tools (F12) and check the Console tab for errors
- Verify your API key is active in your WeatherAPI.com dashboard
- Check if you've exceeded your monthly quota

### Air Quality not showing
- Air quality data might not be available for all locations
- It's included automatically with weather data, no additional setup needed

## Support
- **WeatherAPI.com Documentation**: https://www.weatherapi.com/docs/
- **API Status**: https://www.weatherapi.com/api-status.aspx
- **Contact**: support@weatherapi.com

## API Endpoints Used
```
Current Weather: https://api.weatherapi.com/v1/current.json
Forecast: https://api.weatherapi.com/v1/forecast.json
Search/Autocomplete: https://api.weatherapi.com/v1/search.json
Astronomy: https://api.weatherapi.com/v1/astronomy.json
```

## Rate Limiting
WeatherAPI.com has generous rate limits:
- **Free tier**: 1M calls/month
- **No per-minute restrictions** on free tier
- **Automatic rate limiting** prevents overuse

Your weather app is now ready to use with WeatherAPI.com! 🌤️