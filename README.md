# Electric-Vehicles-Analysis

<p align="center">
<img src="https://www.generalkinematics.com/wp-content/uploads/2018/04/New-GK-2018-Size-2.png">
</p>

Image Taken from [General Kinematics](https://www.generalkinematics.com/blog/electric-vehicles-and-the-effect-on-the-metal-market/).

## Project Description

The goal of this project was to visualize data surrounding Electric Vehicles. This included data about sales of electric vehicles (both battery and plug-in hybrid) in different countries per year, as well as number of charging points in different countries per year. Data about the tax rebate incentives in the state of California were then analyzed to see how the number of rebate dollars claimed per years has changed, and to what extent this varies by county. Data cleaning and analysis was completed in python in a jupyter notebook using the pandas library and data visualization was completed using the plotly library.

Questions to be answered can be found in the table of contents, below:

-----

### Table of Contents

1. [<b>Electric Vehicle Sales and Charging Points Globally and in USA</b>](https://github.com/jonnybrammah/Electric-Vehicles-Analysis/blob/main/README.md#electric-vehicle-sales-and-charging-points-globally-and-in-usa)
    1. [<b>Electric Car Sales Data in USA over time</b>](https://github.com/jonnybrammah/Electric-Vehicles-Analysis/blob/main/README.md#electric-car-sales-data-in-usa-over-time)
    2. [<b>Electric Car Sales Data per Country (2021)</b>](https://github.com/jonnybrammah/Electric-Vehicles-Analysis/blob/main/README.md#electric-car-sales-data-per-country)
    3. [<b>Charging Points in USA over time</b>](https://github.com/jonnybrammah/Electric-Vehicles-Analysis/blob/main/README.md#charging-points-in-usa-over-time)
    4. [<b>Charging Points Data per Country (2021)</b>](https://github.com/jonnybrammah/Electric-Vehicles-Analysis/blob/main/README.md#charging-points-data-per-country)
2. [<b>California Tax Rebates for Electric Vehicles</b>](https://github.com/jonnybrammah/Electric-Vehicles-Analysis/blob/main/README.md#california-tax-rebates-for-electric-vehicles)
-----

### Electric Vehicle Sales and Charging Points Globally and in USA
Data was collected from [International Energy Agency](https://www.iea.org/reports/electric-vehicles) in the form of a csv file. This data included sales data of Electric Vehicles per year for a list of countries from 2010, broken down into both fully electric battery-powered vehicles (BEVs) and plug-in hybrid vechicles (PHEVs). The dataset also included the number of publicly available Electric Vehicle charging points in the list of countries per year since 2017, broken down into slow and fast charging stations. Data was also taken from the [World Bank Website](https://data.worldbank.org/indicator/SP.POP.TOTL) in order to normalize this data by population.

-----
  
#### Electric Car Sales Data in USA over time:
  
The data was filtered to show only car sales in the USA and plotted against time. This graph is shown below:
  
<p align="center">
<img src="https://raw.githubusercontent.com/jonnybrammah/Electric-Vehicles-Analysis/main/Output/Electric_Cars_Sold_Over_Time_USA_by_type.png">
</p>

This graph shows an increase in the number of both types of electric vehicles being sold in the USA with sales of both PHEVs and BEVs remaining similar up until 2017. At this point, BEV sales increase dramatically and PHEV sales decrease until an uptick after 2020. This change is potentially due to changing attitudes towards both types of EVs, with PHEV's previously being considered a "convenient stepping stone" to fully electric vehicles without drivers having to worry about range ([FleetEurope](https://www.fleeteurope.com/en/new-energies/europe/analysis/why-bev-sales-are-racing-ahead-phevs?a=JMA06&t%5B0%5D=EVs&t%5B1%5D=PHEVs&t%5B2%5D=Car&curl=1)). However, with BEV ranges increasing and the increased availability of charging stations (more below), manufacturers may have switched to fully electrifying vehicles. This change in sales numbers is also likely related to changes in government incentives, globally, towards BEVs over PHEVs. 


#### Electric Car Sales Data per Country (2021)

The data was then filtered to show sales of both types of EVs in the listed countries for the most recent year in the dataset (2021). This data was then plotted as a series of bar charts for easy comparison. 
The following bar chart includes all countries within the data set:
  
<p align="center">
<img src="https://raw.githubusercontent.com/jonnybrammah/Electric-Vehicles-Analysis/main/Output/EV_Sales_by_Country_2021.png">
</p>

There are two notable points from this graph. One is that clearly China is substantially outperforming all other countries in the dataset by sales of electric vehicles. Another is that the sales of BEVs in most countries are higher than the sales of PHEVs, showing the conclusion stated in the section of USA's EV sales over time seems to be a global trend.

This conclusion becomes more apparent when China (which is dwarfing other countries) is removed from the graph so that all other countries can be seen more clearly:

<p align="center">
<img src="https://raw.githubusercontent.com/jonnybrammah/Electric-Vehicles-Analysis/main/Output/EV_Sales_by_Country_2021(Exc_China).png">
</p>

However, both of these graphs do not take into account the relative sizes of countries, and so population data was taken from the World Bank website to normalize these data by population. The results of this graph can be seen below:

<p align="center">
<img src="https://raw.githubusercontent.com/jonnybrammah/Electric-Vehicles-Analysis/main/Output/EV_Sales_per_1000_by_Country_2021.png">
</p>

This data tells a very different story. Both China and the USA and other European countries show very few sales per 1000 residents when compared to Deenmark, Sweden, Iceland, and Norway.



#### Charging Points in USA over time



#### Charging Points Data per Country (2021)

-----

### California Tax Rebates for Electric Vehicles

