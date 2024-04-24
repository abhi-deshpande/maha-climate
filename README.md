# Maha Climate - a climate data analysis project

Welcome to the Maha Climate Project..! This is a Power BI data analytics project, focusing on climate analysis of Maharashtra State, India, from where I belong. While learning data analytics, I came across different domains where it can be applied and one of them is Climate. In this project, analysis of daily rainfall and temperatures has been performed in order to discover climate changes, if any.

You can see the dashboard [here.](https://app.powerbi.com/view?r=eyJrIjoiZTE1YTU5M2MtMzEzOS00MGQ2LTk4MTctYzU1NTg0NjQ5ZDY2IiwidCI6IjRjZTg1NWFkLTMzYjctNGQ5Yy1iNGJhLTU5ZWNhMjYyZGE5OSJ9&pageName=ReportSection)

# What is Climate Data Analysis ?

Climate Data Analysis particularly focuses on analysing long term (like 30/50/100 years..!!) data about atmospheric parameters and discovering trends in changing atmospheric behaviour. The data about atmosphere can be be collected on ground via different measuring instruments, or it can be collected via satellites using remote sensing capabilities. Different instruments and satellites collect different types of information about atmosphere, which can have different levels of significance according to the objectives of the data collection. 

This collected data is then analysed by using statistical methods and then correlated with the principles of atmospheric physics in order to predict what atmospheric events would probably occur in the long run. This process helps to understand what environmental and ecological impacts would occur and establish their risk levels to the biological entities. In short, it's an exploratory data analysis of the climate change.

This is certainly different from a regular weather forecast, because a weather forecast focuses on short term dramatic changes in the atmosphere, and prediction of events in short term, like a cyclone, a heat wave or rainfall.

For this particular project, the focus will be on the data collected on ground. Several types of atmospheric data are collected on ground, from which, analysis of 3 major parameters will be performed, viz. - realised daily rainfall, realised daily maximum temperature and realised daily minimum temperature.

# Seasons in Maharashtra

Maharashtra State is situated in the mid-west zone of the Indian Peninsula. Mainly 4 major types of seasons can be experienced here, based on geographical and atmospheric properties. They are -

1. **January to February** - *Winter*
2. **March to May** - *Pre-Monsoons/Summer*
3. **June to September** - *Southwest Monsoons*
4. **October to December** - *Post-Monsoons*

Considering these seasons and their characteristics, some expected climate behaviour is considered and then attempt to create visuals was made which might be helpful to show deviations in that behaviour.

# Mechanism of Monsoons

It would not be possible here to discuss all the detailed atmospheric conditions that lead to formation, onset and departure of Monsoons over Maharashtra State. Therefore, good quality references will be provided at the end of this README. Although, some overview of the steps can be taken -

1. **Differential Heating** : During Pre-Monsoons season, the Indian subcontinent and oceanic regions heat up differently, which drives the whole Monsoons Mechanism.
2. **Inter-Tropical Convergence Zone (ITCZ)** : ITCZ is the broad trough of low pressure in equatorial latitudes. This ITCZ shifts either to north or south, with the apparent movement of the sun.
3. **Wind Patterns Changes** : Changing wind patterns lead to develop Monsoons.
4. **Low pressure on land** : During Pre-Monsoons/Summer, land heats up a lot, causing low pressure.
5. **High pressure on ocean** : As Indian Ocean cools down due to evaporative cooling in Summer, high pressure is developed over it.
6. Air starts moving from high pressure to low pressure zones.
7. This moving air brings up a lot of moisture with it, that's caused due to evaporation on oceans.
8. Winds start to flow from Southwest of the Indian subcontinent, branching into two and moving over Arabian Sea and Bay of Bengal.
9. As the air rises over the land surface and moves towards north, it cools, condenses and causes rainfall.

Now, understanding these processes is not directly necessary for the analysis, but is crucial to see how climate change is affecting these processes, and what could result through that change.

# Objectives of the Analysis 

The objectives for this analysis are as follows - 

1. **Perform exploratory analysis of the climate data for Maharashtra State.**
2. **Discover the characteristics and trends in Monsoons across the state.**
3. **Find long period rainfall behaviour and categorise it in categories defined by IMD.**
4. **Analyse trends in temperatures and Non-Monsoons Rainfall.**

# Procedures

Following procedures were needed to be performed to achieve this work -

### 1. Data Collection 

Data collection is a crucial processes in analysis workflow. The data for this project was collected from India Meteorological Department, Pune from their dedicated Python library known as ***imdlib***. This library has all the necessary functions to handle high resolution gridded data, and is able to export the data for given longitudes and latitudes. As large amount of processing power was required to prepare a dataset from IMD's gridded data, it was not possible to easily process it on local computer. Therefore, the library was installed on Google's Collaboratory (Colab) with a default free compute instance. Daily rainfall and temperature data was thus collected, for past 51 years (1973 to 2023).

### 2. Data Cleaning and Preparation of Dataset

Extensive amount of work was done in this step, in order to design a proper data model. As the data required to be directly relatable to districts and subdivisions, seperate .*CSV* files for each set of longitudes-latitudes were collected from the library. After carefully labeling each of them with district and subdivisions, they were combined to form a single large .*CSV*. This file was further edited and improved using Microsoft Excel. Any additionally required columns were added. Thus, the final dataset was designed.

### 3. Importing in Power BI and further modifications

The dataset was imported in Power BI and was further processed to establish data relationships and model. A simple star schema was achieved and new calculated columns were added as required. After adding measures and deciding basic visuals, the work for dashboard started.

### 4. Dashboard Preparation

The dashboard was prepared in two phases - functional designing and aesthetic designing. In functional designing, logical components for each page were prepared. In aesthetic designing, graphical improvement was done.

### 5. Exploration

In this final step, potential findings were sought by using the finished dashboard.

# Findings

The dashboard is designed in such a way that a lot of findings can be seen, but some key ones are listed here -

1. **Rainfall -**
	1. Overall rainfall trend was found to be *rising*, including Monsoons. On the other hand, Non-Monsoons rainfall trend was found to be *stable*.
	2. **Sindhudurg** received highest overall rainfall. **Dhule** received lowest overall rainfall. **Raigad** received highest monsoons. **Ahilya Nagar** received lowest monsoons.
	3. **2019** was the year with highest rainfall. **2015** was the year with lowest rainfall.
	4. From LPAs of these 51 years, normal monsoons can be considered as **100±16%** according to IMD's described normal calculation method. Anything below that is 'Below Normal'. Anything above that is 'Above Normal'. Since last two decades, Occurrences of 'Above Normal' rainfall have *risen*.
	5. Pre-Monsoons/Summer rainfall has *risen* consistently. **Ratnagiri, Kolhapur, Sangli, Satara and Chandrapur** have received highest Pre-Monsoons.
	6. **Southwest districts** received highest summer rainfall. On the contrary, **northeast districts** received highest winter rainfall. This pattern may be an indicator of *warmer winters due to El Niño*. But overall winter rainfall trend was also found to be decreasing in the last decade, which *may* be an indicator of **decreasing El Niño effect**.
	7. Among subdivisions, **Konkan** received the most rainfall. **Marathwada** received lowest rainfall.

2. **Temperatures -**
	1. According to the analysis of average maximum and minimum temperatures, it can be seen that both of them show a *rising trend*, hence overall warming of the atmosphere.
	2. **Southwest districts** were observed to have warmer winters. **Northeast districts** were observed to have colder winters.
	3. Post-Monsoons temperatures were distributed more *evenly* in the whole state with a fewer districts more warmer.
	4. Almost half of the summer time can be considered as **heat wave**. This is serious issue, and since last two decades, an **overall growth of 6%** can be seen in heat wave occurrences.
	5. **Wardha** district was seen to be most warmer overall. **Ahilya Nagar** was seen to be most colder, as per the LPAs.
	6. **Marathwada** was the subdivision, showing both highest and lowest LPAs in 51 years.
	7. **Konkan** subdivision seem to be warming lately, in the Post-Monsoons season. On the other hand **Vidarbha** seem to be cooling early. Thus, seemingly Western Maharashtra is more humid, and Eastern Maharashtra is more dry.

These were ***some*** of the insights that can be seen in the dashboard. There are lot more than these. To see them, you may locally download the dashboard yourself or [try it online.](https://app.powerbi.com/view?r=eyJrIjoiZTE1YTU5M2MtMzEzOS00MGQ2LTk4MTctYzU1NTg0NjQ5ZDY2IiwidCI6IjRjZTg1NWFkLTMzYjctNGQ5Yy1iNGJhLTU5ZWNhMjYyZGE5OSJ9&pageName=ReportSection)

# List of potential KPIs

Some of the potential KPIs related to this particular climate analysis are listed below -

1. Average Realised Rainfall
2. Average Realised Maximum Temperature
3. Average Realised Minimum Temperature
4. Long Period Average (LPA) Rainfall
5. Long Period Average (LPA) Maximum Temperature
6. Long Period Average (LPA) Minimum Temperature
7. Highest Monsoons Year
8. Lowest Monsoons Year
9. Highest Non-Monsoons Year
10. Lowest Non-Monsoons Year
11. Lowest Recorded Monsoons
12. Highest Recorded Monsoons
13. Total Rainfall
14. Yearly Monsoon Index
15. Rainfall Intensity Distribution
16. Rainfall Category
17. Maximum Daily Rainfall

# Conclusions and References

From the data analysis for climate data, it can be seen that -

1. Indeed, there is a climate change seen over Maharashtra State, mainly due to rising overall temperatures.
2. Rising temperatures have increased low pressure tendencies and overall rainfall, and there is a drastic contrast seen between Konkan and Marathwada, in terms of rainfall distribution.
3. Summer rainfall has risen and post-monsoons rainfall has a slight decreasing trend. This may be an indicator that monsoons are approaching the state earlier than before, and are staying a bit longer.
4. More contrast in heating and cooling of land was seen between west and east Maharashtra, resulting areas with high normal rainfalls to receive more intense ones. On the other hand, areas with less normal rainfall are observing more draughts.
5. Overall, climate is going to be intense in upcoming decade, in terms of all seasons.

## References for monsoons mechanism -

1. ["Indian Monsoon" by Dr. K. K. Mishra](https://www.jncpasighat.edu.in/file/ppt/geo/indian_monsoons.pdf)
2. [Monsoons by Dr. Krishnanand](https://www.youtube.com/watch?v=7QUz_CTAomc)
3. [Monsoons by P. Mahesh](https://youtu.be/8-udGGC58ns?si=qlLkKiGg6lEKfdVn)

## References for IMD Terms -

1. [IMD Glossary](https://www.imdpune.gov.in/Reports/glossary.pdf)
2. [Frequently asked questions article by IMD](https://web.archive.org/web/20180219114557/http://imd.gov.in:80/section/nhac/wxfaq.pdf)
3. [IMD Monsoons FAQ](https://mausam.imd.gov.in/imd_latest/monsoonfaq.pdf)

## Data Sources -

1. [Climate Research and Services, Pune, IMD Pune](https://www.imdpune.gov.in/lrfindex.php)
2. [imdlib](https://imdlib.readthedocs.io/en/latest/)
3. Rajeevan, M., Jyoti Bhate, A.K.Jaswal, 2008 : [Analysis of variability and trends of extreme rainfall events over India using 104 years of gridded daily rainfall data,](https://www.imdpune.gov.in/cmpg/Griddata/Analysis%20of%20variability%20and%20trends%20of%20extreme%20rainfall%20events%20over%20India.pdf) Geophysical Res. Lttrs, Vol.35, L18707, doi:10.1029/2008GL035143.
4. https://github.com/abhatia08/india_shp_2020 (For shape files)

# Licensing

This work is distributed under [CC BY-NC-SA 4.0.](https://creativecommons.org/licenses/by-nc-sa/4.0/deed.en) Data sources may have their own terms of use and is it better to communicate with IMD for any sort of commercial use of their data. Refer to data source references above.


