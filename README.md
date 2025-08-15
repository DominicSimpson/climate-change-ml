# Dominic Simpson - La Fosse Hackathon - Data Deep Dive

![Image](https://github.com/user-attachments/assets/e33472fc-3eb2-401f-b7a1-b443493c2e6a)

### Exposition:
For this hackaton project, "From Data to Insights to Predictions", and for my first Machine Learning (ML) project, my interest
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
This smaller dataset only lists climate data for fifteen countries over the period 2000-2024 - Argentina, Australia, Brazil, Canada, China, France, Germany, India, Indonesia, Mexico, Japan, Russia, South Africa, the UK, and the USA - thus making this project easier compared to if data on all of the world's countries were included.


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
  
Summary of cleaning and transforming data:

- I ensured via regex that the measurements in the column titles (°C, for example) were removed, and the titles converted to lowercase, with underscores added. This made for better formatted titles. I also dropped the Population column, due to not being essential to the project; in addition, the figures in the column were noticeably wrong.
- I ensured that columns with floats were formatted to two decimal places, to preserve precision from original calculations (in climate change studies, small differences can be meaningful when looking at long-term trends).
- I ordered the dataset by country and years (A-Z and 2000-2024 respectively).

ML:

I used a RandomForestRegressor as an interesting contrast to previously learning KNeighborsRegressor. The results of my tests on my data led to the following outputs:

- Mean Absolute Error: 7.74 °C
- Mean Squared Error: 83.40 °C^2
- Root Mean Squared Error: 9.13 °C
- R2: -0.14

Summary of Results and Predictions after looking at data:

- Hypothesis 1: Countries throughout the world have seen a general rise in temperatures overall.
  - The Data Visualization of the processed data shows that the combined average temperatures of the fifteen countries in the data has indeed risen overall throughout the last 25 years.

<img width="1158" height="607" alt="Image" src="https://github.com/user-attachments/assets/e8cdf4b6-8174-4d8b-8863-d7ba6abff8dd" />

  - The results of my ML appear to bear this out too when n_estimators = 200:

<img width="773" height="564" alt="Image" src="https://github.com/user-attachments/assets/dea44167-f1dc-486b-a447-471008d9764c" />

  - However, after spliting data into train/test sets, a more unclear picture emerges:

<img width="767" height="566" alt="Image" src="https://github.com/user-attachments/assets/4ef9156c-9caf-492f-b0a8-e0a5807bd5ea" />

  - Despite this, the data and the majority of ML predictions alike do ultimately show that the fifteen countries have seen an increase in temperatures.

- Hypothesis 2: Rising global temperatures can be correlated with the trend for increasing CO₂ emissions per capita - despite attempts by countries and organisations to bring down CO₂ levels.

  - This hypothesis is true when looking at the data visualization of the processed data:
 
<img width="1156" height="621" alt="Image" src="https://github.com/user-attachments/assets/e833dd94-3396-4b2e-8593-359c982efd37" />

 - However, the picture becomes much more complicated and unclear at the country level:

<img width="1155" height="573" alt="Image" src="https://github.com/user-attachments/assets/b737f681-998e-48f0-88d1-02e04cbdae73" />

- I did not have the time in this project to look at the final ML predictions for average temperature by individual country. This is something that I would like to have looked into a lot more.
- 


 
