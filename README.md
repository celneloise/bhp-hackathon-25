# Ship Mooring Safety & Efficiency System

This software is designed to improve **safety** and **efficiency** in the **ship loading process**. The system focuses on **mooring line tensions** and uses **wind** and **tide/current forecasts** to dynamically calculate and adjust the tension needed for each mooring hook to ensure the safety of the crew.

## Features

### 1. **Stability & Efficiency**
- **Wind & Tide/Current Forecast**: The app collects real-time **weather forecasts** (wind and tide/current) from public APIs. 
- Based on these forecasts, it calculates the optimal amount of **tension adjustment** required for each hook, ensuring stability during the loading process.

### 2. **Safety Features**
- **Bollard Numbering**: The app allows the crew to work with bollards numbered 1 through 10.
- **Tension Limit Thresholds**: If any mooring hook reaches its **tension threshold**, the app sends a **warning**. This helps prevent hooks from breaking and ensures that tension is managed safely across the ship.
  
- **Real-time Alerts**: 
  - If a hook is nearing its **tension limit**, the app triggers an **alert** (vibration, flashing lights, or alarm sounds) to notify nearby staff to evacuate or adjust tension.
  - For example, if **Bollard 3** reaches a high tension threshold, people working on **Bollards 2, 3, and 4** are notified to evacuate to the remaining safe bollards.

## Steps to Install
1. Clone the Repository
Clone the repository to your local machine:
```
git clone https://github.com/<your-username>/ship-mooring-safety.git
cd ship-mooring-safety
```

2. Create a Virtual Environment (Optional but Recommended)
Create and activate a Python virtual environment to keep dependencies isolated:
```
python -m venv venv
source venv/bin/activate  # On Windows use: venv\Scripts\activate
```

3. Install Dependencies
Install the required Python libraries listed in requirements.txt:
```
pip install -r requirements.txt
```

4. Set Up API Keys
To access wind and tide data, you need API keys for the respective APIs (e.g., OpenWeather API for weather data).
Create a .env file in the root directory of the project.
Add your API keys (e.g., OPENWEATHER_API_KEY for OpenWeather API) to the .env file:
```
OPENWEATHER_API_KEY=your-api-key-here
```

5. Run the Application
Once everything is set up, you can start using the application.
If you're working with a Jupyter notebook (main.ipynb), run the notebook directly:
```
jupyter notebook main.ipynb
```
Alternatively, if the application has a command-line interface, you may run the Python script directly (e.g., python app.py).

## Usage
### Collecting Forecast Data
The system fetches wind and tide forecasts from public APIs. This data is then processed to calculate the mooring line tension needed for each hook.

### Tension Adjustment Calculation
Based on the weather data, the system computes the tension threshold for each hook and monitors whether any hook exceeds the limit.

### Alert System
If the tension in any hook exceeds its threshold, the system will trigger warnings (e.g., flashing lights, vibrations, or alarms) to ensure the safety of nearby staff.

### User Interface
Staff members will interact with the application to receive real-time notifications and adjust the mooring lines accordingly.

## Code Explanation
Web Scraping: The code uses web scraping to collect real-time data about wind and tide from public APIs.
Tension Calculation: The tension needed for each mooring hook is calculated based on the weather forecast, considering factors such as wind speed, tide direction, and ship loading conditions.
Safety Alerts: The system continuously monitors the tension levels. If any hook approaches its tension threshold, safety alerts are triggered for the crew.

## Files Overview
main.ipynb: Jupyter notebook that contains the main logic for fetching data, calculating tension, and generating alerts.
mooring_fake_data.json: Sample data used for testing the mooring tension calculation.
requirements.txt: Lists the Python libraries required to run the project.
README.md: This documentation.
.gitignore: Ensures sensitive files, like .env, are not uploaded to version control.

## Requirements (requirements.txt)
The requirements.txt file contains all the libraries used in this project. It should look like this:
```
requests
beautifulsoup4
python-dotenv
```
To install these dependencies, use the following command:
```
pip install -r requirements.txt
```
