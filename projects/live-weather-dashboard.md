---
layout: default
title: Live Weather Dashboard
permalink: /projects/live-weather-dashboard/
---

[← Back to portfolio]({{ site.baseurl }}/)

# Live Weather Dashboard

A beginner-friendly live weather dashboard built with Python and Streamlit. It retrieves forecast information from the Open-Meteo API and presents readable metrics, charts and a seven-day outlook.

## Project goals
- Search for a city and retrieve its forecast.
- Show current conditions in a quick-to-read layout.
- Explore hourly temperature and precipitation probability.
- Compare the forecast across the next seven days.

## Tools
Python · Streamlit · Pandas · Plotly · Requests · Open-Meteo API

## How it works
1. **Geocoding:** the city search sends a city name to Open-Meteo and retrieves matching coordinates.
2. **Weather request:** latitude and longitude are passed to the forecast endpoint.
3. **Data preparation:** the API response is organised into current, hourly and daily data.
4. **Display:** Streamlit renders metrics and tables, while Plotly draws interactive charts.
5. **Caching:** API responses are cached for 15 minutes to reduce repeated requests.

## Code walkthrough
- `api_get(...)` sends HTTP requests and uses a timeout.
- `find_city(...)` looks up city coordinates and caches repeated searches.
- `get_weather(...)` requests current conditions and forecast arrays.
- `describe_weather(...)` converts weather codes into human-readable descriptions.
- The page uses metric cards, an hourly temperature line chart, a precipitation chart and a seven-day forecast table.
- The refresh control clears the cache so fresh data can be requested.

## Limitations and next steps
This is a learning project, not a severe-weather warning service. Forecast accuracy depends on the upstream provider and location data. Future improvements could include unit toggles, saved favourite cities and clearer error messages.

**Note:** Streamlit apps do not run directly on GitHub Pages; the repository link provides the source code.
