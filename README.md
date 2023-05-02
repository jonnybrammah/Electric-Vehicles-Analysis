# Electric-Vehicles-Analysis

<p align="center">
<img src="https://www.generalkinematics.com/wp-content/uploads/2018/04/New-GK-2018-Size-2.png">
</p>

Image Taken from [General Kinematics](https://www.generalkinematics.com/blog/electric-vehicles-and-the-effect-on-the-metal-market/).

## Project Description

The goal of this project was to visualize data surrounding Electric Vehicles. This included data about sales of electric vehicles (both battery and plug-in hybrid) in different countries per year, as well as number of charging points in different countries per year. Data about the tax rebate incentives in the state of California were then analyzed to see how the number of rebate dollars claimed per years has changed, and to what extent this varies by county. Data cleaning and analysis was completed in python in a jupyter notebook using the pandas library and data visualization was completed using the plotly library.

Questions to be answered can be found in the table of contents, below:

### Table of Contents

1. [<b>Electric Vehicle Sales and Charging Points Globally and in USA</b>](https://github.com/jonnybrammah/Electric-Vehicles-Analysis/blob/main/README.md#electric-vehicle-sales-and-charging-points-globally-and-in-usa)
    1. [<b>Electric Car Sales Data in USA over time</b>](https://github.com/jonnybrammah/Electric-Vehicles-Analysis/blob/main/README.md#electric-car-sales-data-in-usa-over-time)
    2. [<b>Electric Car Sales Data per Country (2021)</b>](https://github.com/jonnybrammah/Electric-Vehicles-Analysis/blob/main/README.md#electric-car-sales-data-per-country)
    3. [<b>Charging Points in USA over time</b>](https://github.com/jonnybrammah/Electric-Vehicles-Analysis/blob/main/README.md#charging-points-in-usa-over-time)
2. [<b>California Tax Rebates for Electric Vehicles</b>](https://github.com/jonnybrammah/Electric-Vehicles-Analysis/blob/main/README.md#california-tax-rebates-for-electric-vehicles)
3. [<b>Next Steps and Future Analysis</b>](https://github.com/jonnybrammah/Electric-Vehicles-Analysis/blob/main/README.md#next-steps-and-future-analysis)
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

This data tells a very different story. Both China and the USA and other European countries show very few sales per 1000 residents when compared to Denmark, Sweden, Iceland, and Norway. The data shown without these countries to reduce the scale can be seen here, showing China and the USA having similar sales in 2021 per 1000 residents:

<p align="center">
<img src="https://raw.githubusercontent.com/jonnybrammah/Electric-Vehicles-Analysis/main/Output/EV_Sales_by_Country_per_1000_2021(Exc_Northern_Europe).png">
</p>

The reasons for Norway's enormous peak of EV sales per 1000 residents are relatively straightforward. One is that the government heavily incentivizes the purchase of electric vehicles and has for almost two decades (by, for example, removing the 25% sales tax on them, or allowing these vehicles to use bus lanes). Another is that so much of Norway's electricity comes from renewable resources, which makes the switch to EVs even more environmentally sensible than in countries where electricity is still largely generated by fossil fuels ([Forbes](https://www.forbes.com/sites/davidnikel/2019/06/18/electric-cars-why-little-norway-leads-the-world-in-ev-usage/?sh=4951572413e3)).

#### Charging Points in USA over time

The data for the publicly available charging points in the USA (separated into both slow and fast charging points) were also plotted, resulting in this graph:

<p align="center">
<img src= "https://github.com/jonnybrammah/Electric-Vehicles-Analysis/blob/main/Output/Charging_Points_By_Year_By_Type.png?raw=true">
</p>

This shows that the number of charging points is increasing throughout the USA year-on-year. The number of publicly available slow charging points has increased relatively quickly over the last decade, whereas fast charging points have lagged as their technology has developed, but started to take off around 2018. This is likely to change as more states in the US put resources towards building more charging stations. Current federal policy is to have half of new vehicles sold in 2030 to be zero-emissions vehicles and one aspect of achieving this will be improving charging infrastructure. With this in mind, more than $10 billion is aimed to be invested in EV charging instructure. A significant portion of this will be focused in areas with poor access to chargers currently, an issue that will be discussed glancingly in the next section ([World Economic Forum](https://www.weforum.org/agenda/2022/11/ev-charging-stations-across-the-us-mapped/)).

-----

### California Tax Rebates for Electric Vehicles
For this section, data was collected from the [California Clean Vehicle Rebate Project](https://cleanvehiclerebate.org/en/rebate-statistics) in the form of a csv file. This data included information on tax rebates provided by the state of California to purchasers of electric vehicles, grouped by county.

The data was cleaned and, in order to analyze this data per capita, merged with data taken from the US Census for the population of each California County in 2022.

The following graph shows the number of rebate dollars given to people in each California county per capita:

<p align="center">
<img src="https://raw.githubusercontent.com/jonnybrammah/Electric-Vehicles-Analysis/main/Output/Rebate_Dollars_per_County_by_County.png">
</p>

It is clear from this graph that many of the tallest bars, representing highest per capita total rebates, can be found in the Bay Area (Santa Clara, Alameda, Marin, San Mateo, etc.). This likely makes some intuitive sense since incomes are likely to be high in many of these counties and so the liklihood of people buying new vehicles increases. These counties are also more densely populated that some of the more rural counties displayed on the graph, and so the liklihood of living close to charging infrastructure also increases. As discussed above, public charging capabilities are not as common in rural areas, and so this also decreases the chances of buying an electric vehicle in these counties.

To test the hypothesis regarding incomes in a county vs the rebate dollars awarded to residents of that county, more data was taken from the US Census to examine the median income in all California Counties. This was also merged with the existing dataframes and median income in a county vs rebate dollars per capita in that county was plotted in the graph below:

<p align="center">
<img src="https://raw.githubusercontent.com/jonnybrammah/Electric-Vehicles-Analysis/main/Output/Rebate_Dollars_per_Capita_by_median_income.png">
</p>

This graph clearly supports the hypothesis that people living in counties with higher median incomes are more likely to claim rebate dollars. The correlation can be clearly seen by the line of best fit, and the r-value of this graph is 0.78 indicating a strong correlation. As suggested above, this is likely due to the increased chances of buying any new car, particularly the more expensive new electric vehicles.

-----

### Limitations and Steps for Future Analysis

One significant limitation in this analysis is the fact that data taken from the International Energy Agency only goes up to 2021, and with changes happening quickly in the Electric Vehicle market (plus government incentives changing) these data may be more out-of-date than they appear. More up-to-date data is always a boon for analyses like these.

Some potential steps for future analysis would be to delve deeper into the relationship between incomes and liklihood of purchasing an electric vehicle. This could be done by expanding this analysis to federal tax incentives for electric vehicles. Similarly, another useful analysis could be analyzing the liklihood of purchasing an electric vehicle and the number charging stations normalized by area in a county. Both of these might help with considerations of increasing the use of electric vehicles across a wider range of income brackets or in rural communities, as opposed to suburban and urban, higher-income communities as the data indicates is the case right now.

