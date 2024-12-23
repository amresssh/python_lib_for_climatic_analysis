# Kutumbh: A Python Library for Architectural Data Analysis

**Kutumbh** is a Python library designed for architects and planners to perform advanced climatic data analysis and create custom visualizations with ease.

## Features
- **Climatic Data Analysis**: Analyze temperature, humidity, wind patterns, and radiation for specific locations in India.
- **Custom Visualizations**: Create tailored graphs and heatmaps for architectural applications.
- **Ease of Use**: Streamlined for non-programmers with user-friendly commands.

## Installation
Install Kutumbh via pip:
```bash
 pip install kutumbh
```
## Usage Guide
Here’s how you can start using Kutumbh:

### **1. Import the Library**
```bash
import kutumbh
```
### **2. Load Weather Data**
Download an .epw weather file from Climate.OneBuilding.org and specify its path:
```bash
epw_file = 'path_to_your.epw'
```
### **3. Perform Climatic Analysis**
Below are examples of the key features of the Kutumbh library:

#### **a) Generate a Seasonal Summary**
Get an overview of the climatic conditions, such as the number of days per season, dry bulb temperatures, relative humidity, and global radiation.
```bash
kutumbh.seasons_summary(epw_file)
```
#### **b) Create a Dry Bulb Temperature Density Plot**
Visualize the density of dry bulb temperatures for specific months.
```bash
kutumbh.temperature_density_plot(epw_file, months=[3, 4, 5])
```
#### **c) Analyze Wind Patterns**
Analyze wind direction and speed, along with corresponding temperature, for specific times of the day (e.g., morning, noon, evening, or night):
```bash
kutumbh.plot_timely_wind_data(epw_file, 'Morning')
```
#### **d) Radiation Analysis on Walls**
Visualize the radiation falling on specific walls for given coordinates (latitude, longitude) and wall orientation (in degrees):
```bash
kutumbh.radiations_on_walls(22.43, 75.505, epw_file, 270)
```
#### **e) Generate a Dry Bulb Temperature Heatmap**
View a heatmap of average hourly dry bulb temperatures:
```bash
kutumbh.dry_bulb_temp_heatmap(epw_file)
```
#### **f) Illuminance Analysis Combined with Sky Cover**
Visualize lighting conditions with combined average sky cover for designing outdoor spaces:
```bash
kutumbh.plot_monthly_illuminance_box_and_mean_sky_cover(epw_file)
```
#### **g) Humidity and Temperature Combined Analysis**
Combine humidity and temperature data to analyze heat stress:
```bash
kutumbh.temp_combined_with_humidity(epw_file, months in list format eg. [1,2])
```
### **4. Outputs**
Each function will generate visualizations or data tables that can be used for architectural design insights.

For more advanced use cases and detailed documentation, see the Usage Examples.

