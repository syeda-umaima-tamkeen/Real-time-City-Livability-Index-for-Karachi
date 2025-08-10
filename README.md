# **PROJECT BY: SYEDA UMAIMA TAMKEEN**  

# **Project Title:** Karachi Livability Index Analysis and Visualization  

# **Summary:**  
In this project, I developed a composite **Livability Index** for Karachi using environmental and weather-related features to evaluate daily living conditions. The objective was to combine air quality, temperature comfort, and humidity comfort into a single index ranging from 0 to 100, where 100 represents the most livable conditions. The analysis also involved data visualization to track livability trends over time and identify periods of low environmental comfort.  

# **Key Steps:**  

**1. Data Loading and Preparation:**  
- Imported the processed dataset (`karachi_daily_features.csv`) containing daily environmental and weather data.  
- Parsed the `date` column as a datetime object for time-series analysis.  

**2. Feature Engineering – Score Calculation:**  
- **Air Quality Score:** Calculated as `100 - PM2.5 Index (0-100)` to give higher scores for cleaner air.  
- **Temperature Comfort Score:** Penalized deviations from the ideal 25°C by subtracting `3 × deviation` from 100.  
- **Humidity Comfort Score:** Penalized deviations from the ideal 50% humidity by subtracting `2 × deviation` from 100.  

**3. Livability Index Computation:**  
- Combined scores with weights:  
  - 50% Air Quality Score  
  - 30% Temperature Comfort Score  
  - 20% Humidity Comfort Score  
- Rounded results to one decimal place.  
- Saved the computed index into a new CSV file `karachi_livability_index.csv`.  

**4. Data Visualization – Time Series Plot:**  
- Created a **line plot** showing Karachi’s Livability Index over time.  
- Added a **horizontal threshold line** at 50 to represent the “Moderate” livability level.  
- Used distinct colors and legends for clarity.  

**5. Interpretation:**  
- Observed seasonal patterns in livability scores, with noticeable dips during periods of poor air quality or extreme weather.  
- The majority of scores remained above the 50-point threshold, indicating moderate to high livability conditions most of the year.  

# **Results:**  

**Livability Index Components:**  
- **Air Quality Score:** Directly reflected fluctuations in PM2.5 levels.  
- **Temperature Score:** Penalized extreme heat waves or cold spells.  
- **Humidity Score:** Penalized high-humidity days common during monsoon season.  

**Visualization Insights:**  
- High livability scores (above 75) occurred during periods of clean air and moderate temperatures.  
- Scores dropped significantly when PM2.5 pollution increased or during temperature extremes.  

# **Conclusion:**  
The Karachi Livability Index successfully combines multiple environmental factors into a single, interpretable score. The index allows for easy visualization of trends and can help city planners, researchers, and policymakers identify periods of reduced livability.  
Future work could involve integrating additional parameters like wind speed, rainfall, and noise levels to refine the index. Incorporating predictive modeling could also forecast future livability trends based on historical weather and pollution patterns.  

