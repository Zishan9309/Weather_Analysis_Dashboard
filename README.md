# 🌤️ Weather Analysis Dashboard — Power BI

A real-time weather analytics dashboard built entirely in Power BI, powered by live data fetched directly from the **WeatherAPI.com REST API** — no Python, no CSV, no intermediate pipeline. The dashboard delivers a clean 7-day weather forecast with key meteorological metrics, making it a practical tool for weather monitoring and analysis.

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=flat&logo=powerbi&logoColor=black)
![REST API](https://img.shields.io/badge/REST%20API-005571?style=flat&logo=fastapi&logoColor=white)
![DAX](https://img.shields.io/badge/DAX-F2C811?style=flat&logo=powerbi&logoColor=black)
![WeatherAPI](https://img.shields.io/badge/WeatherAPI.com-00BFFF?style=flat&logoColor=white)
![Last Commit](https://img.shields.io/github/last-commit/zishan9309/weather-analysis-dashboard)
![Repo Size](https://img.shields.io/github/repo-size/zishan9309/weather-analysis-dashboard)

---

## 📌 Problem Statement

Weather data is widely available but rarely presented in a way that's immediately actionable. Most dashboards either rely on static CSVs or require a backend pipeline to process API data before visualization. This project solves that by:

- Connecting Power BI **directly to a live REST API** (no code, no intermediary)
- Pulling current + 7-day forecast data in real time
- Presenting all key weather parameters in a single, interactive dashboard

---

## 🚀 Key Features

| Feature | Description |
|---|---|
| 🌡️ Temperature & Humidity | Current readings + 7-day trend line charts |
| 🌬️ Wind Speed | Daily wind speed visualization with directional context |
| ☀️ UV Index | UV level tracking with safe/moderate/high categorization |
| 🌧️ Precipitation | Rainfall probability and amount across the forecast window |
| 📅 7-Day Forecast Cards | Day-by-day weather summary with condition icons |
| 🔄 Live Data Refresh | Direct API connection — data updates on dashboard refresh |

---

## 🛠️ Tech Stack

| Tool | Usage |
|---|---|
| **Power BI Desktop** | Dashboard design, data modeling, visualization |
| **WeatherAPI.com** | Live REST API — current weather + 7-day forecast endpoint |
| **Power Query (M Language)** | API connection, JSON response parsing, data transformation |
| **DAX** | Calculated measures for UV categorization, trend analysis |

---

## 🔗 How the API Integration Works

1. **API Endpoint used:**
```
http://api.weatherapi.com/v1/forecast.json?key=YOUR_API_KEY&q=CITY&days=7
```

2. **Power BI connection:**
   - `Get Data` → `Web` → paste the API URL with your key
   - Power Query parses the JSON response automatically
   - Nested forecast arrays expanded into flat tables using `Expand Column`

3. **Data model:**
   - `Current` table — real-time conditions (temp, humidity, wind, UV)
   - `Forecast` table — 7 rows, one per forecast day (min/max temp, rain chance, condition)

---

## 📊 Dashboard Preview

**Overview — Current Conditions + 7-Day Forecast**
![Overview](./screenshots/01_overview.png)

**Temperature & Humidity Trends**
![Temperature Trends](./screenshots/02_temperature_humidity.png)

**Wind Speed & Precipitation**
![Wind & Rain](./screenshots/03_wind_precipitation.png)

**UV Index & Forecast Cards**
![UV & Forecast](./screenshots/04_uv_forecast_cards.png)

---

## 📁 Repository Structure

```
weather-analysis-dashboard/
├── README.md
├── Weather_Analysis_Dashboard.pbix     # Power BI dashboard file
└── screenshots/
    ├── 01_overview.png
    ├── 02_temperature_humidity.png
    ├── 03_wind_precipitation.png
    └── 04_uv_forecast_cards.png
```

---

## 🚀 How to Use

1. Clone the repo:
```bash
git clone https://github.com/zishan9309/weather-analysis-dashboard.git
```

2. Sign up at [WeatherAPI.com](https://www.weatherapi.com/) and get a free API key.

3. Open `Weather_Analysis_Dashboard.pbix` in Power BI Desktop.

4. In Power Query Editor → find the API URL source → replace `YOUR_API_KEY` with your key and set your city.

5. Click **Refresh** — dashboard loads with live data for your city.

---

## 💡 What Makes This Project Stand Out

- **No Python, No CSV** — most fresher dashboards use static datasets. This fetches live API data directly inside Power BI using Power Query's Web connector
- **JSON Parsing in Power Query** — demonstrates real-world data wrangling (nested JSON → flat table) without writing a single line of Python
- **End-to-end ownership** — API integration → data transformation → DAX measures → visualization, all in one tool

---

## 📌 Resume Bullet Points

```
• Integrated live WeatherAPI.com REST API directly into Power BI to fetch
  real-time and 7-day forecast data — no Python or intermediate pipeline required

• Built an interactive dashboard visualizing temperature, humidity, wind speed,
  UV index, and precipitation using DAX measures and dynamic visuals

• Parsed nested JSON API response using Power Query (M Language),
  transforming raw API data into structured forecast and current-conditions tables

• Designed 7-day forecast cards enabling day-by-day weather comparison
  for end-to-end BI skill demonstration — from API ingestion to final dashboard
```

---

## 👤 Author

**Zishan Khan**
[LinkedIn](https://linkedin.com/in/zishan-khan-a310a3259) · [GitHub](https://github.com/zishan9309)
