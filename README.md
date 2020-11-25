# COVIDQuadrant
Snowflake SQL and Tableau TWB at the County Level for COVID 19 and Quadrant Analysis

### Full Blog and Walkthough here
https://bigdatadave.com/2020/11/22/tableau-snowflake-covid-19-by-county-quadrants-maps/

### Tableau & Snowflake: COVID-19 by County Quadrants & Maps
With the COVID-19 crisis worsening in America right now, I was curious which areas of the country are being affected more than others? I have been producing loads of SQL over the JHU data set provided by Starschema to the Snowflake Data Marketplace. I thought if I could enhance the JHU data at the county (FIPS) level with population, I could normalize Cases and Deaths per 100k population by County in the United States. Once I had this data in hand, I could produce a map showing a quadrant of counties by Case and Death rates. The quadrant would show counties amongst their peers of Cases and Deaths above and below the mean.

![COVID Quadrant Map](https://bigdatadave.files.wordpress.com/2020/11/screen-shot-2020-11-22-at-2.39.16-pm.png?w=1024)
*US Map as of 21-Nov-2020*<br/>
*QI (Red – High Deaths, High Cases) | QII (Orange – High Deaths Low Cases)*<br/>
*QIII (Blue – Low Deaths, Low Cases) | QIV (Teal – Low Deaths, High Cases)*<br/>

### Utah?
*“Utah: Utah is reporting county data somewhat differently than many other states. The larger-population counties are reporting confirmed cases and deaths at the county level. However, the smaller counties are banded together into county groups. This is in an effort to protect identities of individuals.”*

### Starschema’s COVID-19 and SafeGraph’s US Census Data & Neighborhood Insights Data Set
Starschema’s COVID-19 data set (https://starschema.com/covid-19-data-set) and Safegraph’s US Census Data & Neighborhood Insights data set (https://www.safegraph.com/open-census-data) are both on Snowflake’s Data Marketplace. I highly recommend both data sets to drive a deeper understanding of our collective pandemic context. The best part is they are both free to play with, free! I love me some free data…let’s geek out with charts!

Getting and querying data from the Snowflake Data Marketplace is dead simple and built on a very powerful premise. After 3 clicks of the mouse, I have data that is ready for analysis and always in sync with Starschema’s or Safegraph’s latest updates. This means I have instant access to a single-source of truth on COVID-19 cases as reported by public health authorities around the world along with key population metrics to enhance my analysis.

Feel free to play with the finished product here: https://public.tableau.com/views/COVID-19QuadrantMaps/CountyCasesvsDeathRatesMap?:language=en&:display_count=y&publish=yes&:origin=viz_share_link
