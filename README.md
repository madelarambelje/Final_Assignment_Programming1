# Final_Assignment_Programming1
This repository is created for the Final Assignment of Programming1. The directory contains a data analyses about the relationship of COVID19 cases and Obese/Overweight


#### Dependencies
- Python 2.7.18
    - Bokeh  2.3.0
    - Pandas 1.2.2
    - Numpy  1.20.1
    - IPython 7.13.0
    - sklearn 0.24.1
    - Matplotlib 3.3.4
    - scipy 1.6.1
    - geopandas 0.8.2
    - json 2.0.9
   
### Final Assignment Programming1 DSLS

- State the region and the domain category that your data sets are about

The main data is downloaded from CBS and RIVM, less significant data is incorperated in the script and is from Arcgis.
These main data is uploaded in the github zip file. This contains a directory with the files needed.

- State the research question

Does obesity/overweight contribute to the number of corona cases, hospitalizations, deaths in municipalities in the provinces Groningen & Drenthe?

- Justify the chosen data storage and processing approach

The data is stored in csv files and can be downloaded from the following sources:

https://data.rivm.nl/covid-19/COVID-19_aantallen_gemeente_per_dag.csv

https://www.cbs.nl/-/media/_excel/2020/03/gemeenten-alfabetisch-2020.xlsx

https://www.volksgezondheidenzorg.info/sites/default/files/map/detail_data/smap2016vzinfo_obesitas.csv

https://www.volksgezondheidenzorg.info/sites/default/files/map/detail_data/smap2016vzinfo_overgewicht.csv

https://www.cbs.nl/-/media/_excel/2020/11/voorlopigebevolkingsgegevens20200101.xlsx

All of these files are stored in the zip file.


- Justify the chosen analysis approach

The data was loaded in to jupyter notebooks using pandas. 
Data from the provinces Groningen and Drenthe were extracted from the dataset. 
Obese and overweight data were merged with the COVID data. 
The COVID cases per municipality were normalized using the number of civilians. 
All of the obeserved cases (reported covid cases, hospitalizations, deceased) 
were divided by the number of civilians from the respective municipality and multiplied by 1e5. 
Scatter plots were plotted with this information. 95% confidence bands was calculated for > 30 samples to observe reliabilitly. 
In addition a regression with LSR was drawn trough all the point.

Maps of the municipality were made and filled based on percentages or normalized cases using bokeh and geopandas.
- Justify the chosen data visualization approach

Scatter plots are a good method for observing relationships between variable x and y. 

Interactive maps and coloring regions that contain a high number of percentage create a good view for regions that are and high in obese/overweight and high in number of corona cases.
The eye could easily observe this if you have these two maps next to each other.

Some correlation can be noticed from the graphs, e.g. the municipalities Oldambt and Pekela have a high percentage of obesity and also corona cases, hospitalizations and deaths. Municipality of Groningen has a lower percentage of obesity/overweight and here are lower death rates, corona cases, and hospitalizations.


