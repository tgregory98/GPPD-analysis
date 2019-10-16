# **GPPD-analysis**
**Some simple data analysis using SQL (SQLite), Jupyter Notebooks and Matplotlib. I used the Global Power Plant Database, an open database coordinated by the World Resources Institute and Google Earth Outreach, and GDP (current US$) database from World Bank.**

My focus is to evaluate how green (in terms of power plants only) the [top 10 economies of Europe](https://europe.businesschief.com/leadership/2285/Top-10-economies-in-Europe) are, and to then ask why this might be. I designed this project **only** for the programming skills, and not for the statistics involved. Topics included:

- Basic SQL; CREATE TABLE, DROP TABLE, SELECT, WHERE, ORDER BY, AS.
- Intermediate SQL; GROUP BY, INNER JOIN, CAST, CASE, aggregate functions, subqueries.
- Automating workflows using batch scripts, to run SQLite command line initialisation tasks.
- Jupyter Notebooks for designing the project.
- Visualisation using the Matplotlib library.

**The easiest way of viewing this project is via the [.md notebook file](https://github.com/tgregory98/GPPD-analysis/tree/master/code/notebook/notebook.md). If you want to try it out for youtself, follow the "How-to (Windows)" section below.**

## Project outline
The train of thought behind this project.
#### 1. Initial setup

Automating the importing of the .csv files into database.db via the SQLite command line, by writing init.bat.

#### 2. Overall and regional primary fuel analysis

This gives us a big picture view of the data.

#### 3. Green energy metric (arbitrary) and analysis

An arbitrary metric is calculated to represent how green each of these 10 countries are in terms of their power plants. Then this metric is compared against GDP figures to see if there's correlation.

## How-to (Windows)

1. Download global_power_plant_database.csv and GDP.csv from the links at the end of the README.

2. Create a folder in the same directory as README.md and call it "data".

3. Put these .csv files inside the new "data" folder.

4. Make sure that both .csv files have correctly formatted headers. (I had to remove the first 4 rows from the GDP .csv).

5. Start by running init.bat to import global_power_plant_database.csv as power_table, and GDP.csv as GDP_table.

6. Navigate to the same directory as README.md with `cd` then run the following to open the database in the SQLite command line:
```
C:/sqlite/sqlite3.exe data/database.db
```
Now the SQLite command line can be used for testing purposes. Useful commands might be `.tables` or `.schema`. Now you can also open the [IPython Notebook](https://github.com/tgregory98/GPPD-analysis/blob/master/code/notebook.ipynb) in Jupyter and run the queries for yourself.

## Licences and citations

All the data used in this project follows a [Creative Commons-Attribution 4.0 (CC BY 4.0) license](https://creativecommons.org/licenses/by/4.0/), just as the original sources do. All credit for the original power plant data goes to the [World Resources Institute](https://www.wri.org/) as part of the [Global Power Plant Database](http://datasets.wri.org/dataset/globalpowerplantdatabase). All credit for the origin GDP data goes to the [The World Bank Group](https://data.worldbank.org) as part of the [GDP (current US$) database](https://data.worldbank.org/indicator/ny.gdp.mktp.cd) The original data has been modified in the form of the addition of new attributes. No raw data files have been included in this repo. Here you will only see the results of queries that have been run. The citations for the databases follow below:

> Global Energy Observatory, Google, KTH Royal Institute of Technology in Stockholm, Enipedia, World Resources Institute. 2019. Global Power Plant Database v1.2.0. Published on Resource Watch (http://resourcewatch.org/) and Google Earth Engine (https://earthengine.google.com/). Accessed through Resource Watch, 15/10/2019. www.resourcewatch.org.

> World Bank. "GDP (current US$)". World Bank national accounts data, and OECD National Accounts data files. The World Bank Group. Accessed 15/10/2019. https://data.worldbank.org/indicator/NY.GDP.MKTP.CD.

Just like the [Global Power Plant Database repo](https://github.com/wri/global-power-plant-database), all code is available under a [MIT license](https://opensource.org/licenses/MIT). All code is contained within the [`code`](https://github.com/tgregory98/GPPD-analysis/tree/master/code) folder.

As a final note, as instructed by the [Creative Commons-Attribution 4.0 (CC BY 4.0) license](https://creativecommons.org/licenses/by/4.0/), no additional restrictions have been added to any part of the data or code. I have simply kept the same restrictions as the [Global Power Plant Database repo](https://github.com/wri/global-power-plant-database) at the date of access, October 2019.
