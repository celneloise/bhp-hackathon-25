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
