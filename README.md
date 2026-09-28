# Hybrid Solar Calculator

A Python desktop application that calculates and estimates the energy generation, usage, and financial savings of a hybrid solar panel system. The app uses geographical coordinates (latitude and longitude) to fetch monthly solar insolation data from the NASA POWER API and computes the efficiency and cost savings based on your annual energy usage.

## Features
- **NASA API Integration:** Automatically fetches monthly solar insolation data for the given location and year.
- **Energy Estimation:** Calculates estimated monthly solar energy generation and your monthly energy usage based on typical usage coefficients.
- **Financial Savings:** Calculates estimated money saved per month based on local electricity prices.
- **Data Export:** Exports all calculated data (usage, generated power, price per month, saved money, and efficiency) to CSV files.
- **Data Visualization:** Generates clear graphs for all metrics using Seaborn and Matplotlib.
- **User-Friendly GUI:** Built with Tkinter for easy input of location, system capacity, yearly usage, and electricity pricing.

## Requirements
- Python 3.x
- `pandas`
- `requests`
- `seaborn`
- `matplotlib`
- `tkinter` (usually included with standard Python installations)

## Installation & Usage
1. Clone the repository.
2. Install the required dependencies:
   ```bash
   pip install pandas requests seaborn matplotlib
   ```
3. Run the application:
   ```bash
   python main.py
   ```
4. Enter your latitude, longitude, yearly energy usage, solar panel rated power, year for insolation data, and the price per kW/h in the GUI to see the results.

## Project Structure
- `main.py`: The entry point that coordinates the logic, GUI, and data processing.
- `main_window.py`: The Tkinter GUI that handles user inputs.
- `insolation_api.py`: Fetches solar data from the NASA POWER API.
- `system.py` & `hybrid_system.py`: Core logic for calculating energy usage, generation, and financial savings.
- `csv_save.py`: Handles saving the computed data to CSV files.
- `seaborn_plotter.py`: Generates visual plots for the data.
