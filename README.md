# Dominic Simpson - La Fosse Hackathon - Data Deep Dive

### Exposition:
For this hackaton project, "From Data to Insights to Predictions", and for my first Machine Learning project, my interest
in climate change has led me to choose the following dataset from Kaggle: https://www.kaggle.com/datasets/bhadramohit/climate-change-dataset/data



- Title: Climate Change Dataset - "Dataset of Temperature, Emissions, and Environmental Trends (2000-2024)"
- File: climate_change_dataset.csv
- File Size: 53.21kB - 90kB (depending on encoding)
- Number of Rows: 1000
- Number of Columns: 10
- Column names:
  - Year
  - Country
  - Avg Temperature (°C)
  - CO2 Emissions (Tons/Capita)
  - Sea Level Rise (mm)
  - Rainfall (mm)
  - Population
  - Renewable Energy (%)
  - Extreme Weather Events
  - Forest Area (%)

Climate change is a subject that interests me, but I wanted a smaller dataset than the large World Bank datasets on climate change that also appear on Kaggle, for example.
This smaller dataset only lists climate data for fifteen countries - Argentina, Australia, Brazil, Canada, China, France, Germany, India, Indonesia, Mexico, Japan, 
Russia, South Africa, the UK, and the USA - thus making this project easier.


Analysis Questions:

- Does the data show that the combined average temperatures of the thirteen countries in the data has risen overall throughout the last 25 years (approx)?
- Can rising global temperatures be correlated with rising CO₂ emissions per capita?
- Has there been an inexorable increase in sea level rise throughout the world?
- Has there been an increase in extreme weather over the 25 year period?
- Can relationships be established between a countries' renewal energy program and forest area (both %), on the other, and average temperature, sea level rise, and extreme weather events on the other?

Hypotheses:

- Countries throughout the world have seen a general rise in temperatures overall.
- Rising global temperatures can be correlated with the trend for increasing CO₂ emissions per capita - despite attempts by countries and organisations to bring down CO₂ levels.

Which column will be my target variable for Machine Learning

- Avg Temperature (°C)
