# Power BI and R Demo (Using R and Power BI to Analyze the Trade Balance at the Country Level)

## Abstract
Power BI is a self-service business intelligence tool that is gaining popularity. Microsoft added the ability to use R scripts as a data source and the ability to use R scripts to create custom visualizations in late 2015. In this repo I have an example of using R in Power BI both as a data source and as a way to create a custom visualization.

I used yearly trade balance data by country that was obtained from census.gov to build a Power BI dashboard. A R script was used to combine the data from the yearly trade balance files into one dataset then loaded into Power BI. I used the stringr, dplyr, tidyr, and lubridate packages to create the script. Typically Power Query is used for that task but the complexity and variety of the data format of each file made it easier to do the task using R.

I also created a custom boxplot visualization using a R script that used the ggplot2 and dplyr packages. The boxplot visualization was more advanced then what could be created using the custom Power BI boxplot because the Power BI's version was not design to accomodate the additional layers and annotations that I added to the boxplot chart. R's ggplot2 package makes it much easier to add the extra layers and annotations.

##### R Script
I included the R file that contains the R script that was used to create the data source and the boxplot visualization. I wrote the scripts in R Studio. When I got the scripts functional I copied and pasted them into Power BI Desktop. The name of the file used to import the data into Power BI is "DataMungingScript.R" and the name of the file used to create the boxplot visualization is "Boxplot.R".

##### Power BI File
I included a copy of the *.pbix file that was used in the presentation. The name of the *.pbix file is "Demo_TradeBalance.pbix". It includes the Power Query scripts, DAX code, embeded R Scripts, and visualizations. 

##### Data Sources
I used trade balance files from the census.gov. Each report contained trade balance data for the given year at the country level for the time period between 2000 and 2014. The files are located in the "Data" folder.

## Extra information

#### R
- Make sure you have stringr, dplyr, ggplot2, lubridate, and tidyr packages loaded in your environment
- Make sure you have a nice IDE to play with the R script if you want to test it for yourself. I recommend you use R Studio.

#### Power BI
- Make sure you go through the instructions provided to setup Power BI to be able to use R as a data source and R to create custom visualizations. Information on how to do so can be found [here](https://powerbi.microsoft.com/en-us/documentation/powerbi-desktop-r-visuals/).
- Download the "chicklet slicer" and "scroller" custom visualizations for Power BI. Those visualizations can be found at [link]("https://app.powerbi.com/visuals/").

#### Dashboard Explanation


## Considerations
Many of the R features are in preview. I was told by personnel at Microsoft in April 2016 that the all of the R features that are currently in Power BI should be in GA soon. I was also told that they will provide a iist of packages that will work on PowerBI.com.
