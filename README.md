# tidycovid19-New-data-and-documentation

The details of the codeset and plots are included in the attached Adobe Acrobat reader (.pdf) file in this repository. 
You need to download the same to view the contents. There are referrals to other contents in BLUE colour also to follow.

As the underlying data sources change their format and access methods often, I have no plans to publish the package on CRAN for the time being. So, to install the package, you need to have the {remotes} package installed. Then, you can install and attach {tidycovid19} along with some other packages that we will need below by:

library(tidycovid19)
library(tidyverse)
library(ggrepel)
library(gghighlight)
library(zoo)

Currently, the package offers the following functions to download data:

    download_jhu_csse_covid19_data(): Downloads and tidies Covid-19 data from the Johns Hopkins University . This data has developed to a standard resource for researchers and the general audience interested in assessing the global spreading of the virus. The data is provided at country and sub-country levels.
    download_ecdc_covid19_data(): Downloads and tidies Covid-19 case data provided by the European Centre for Disease Prevention and Control. The data is updated weekly and contains the latest available public data on the number of new Covid-19 cases reported per week and per country.
    NEW: download_owid_data(): Downloads and tidies data collected by the ‘Our World in Data’ team. This team systematically collects data on hospitalizations, testing and vaccinations from multiple national sources.
    download_acaps_npi_data(): Downloads and tidies the Government measures dataset provided by the Assessment Capacities Project (ACAPS). These data allow researchers to study the effect of non-pharmaceutical interventions on the development of the virus.
    download_oxford_npi_data(): Downloads and tidies data from the Oxford Covid-19 Government Response Tracker, an alternative data source for governmental interventions. Currently, I do not include the financial measures of this data set and also do not include its data in the merged data file (see below) as I view the ACAPS data to be better suited (this blog post details why).
    download_apple_mtr_data(): Downloads Mobility Trends Reports provided by Apple related to Covid-19. The data is provided at country and sub-country levels.
    download_google_cmr_data(): Downloads Google COVID-19 Community Mobility Reports data. As of April 17, Google provides a nice and clean CSV file containing country-day and region-day data. This makes the PDF scraping code that used to be part of this package obsolete. If you are interested in it for didactic reasons, you can still find it in the git hstory. This data is available at the country, regional and U.S. county level.
    download_google_trends_data(): Downloads and tidies Google Trends data on the search volume for the term “coronavirus” (Thank you to Yan Ouaknine for bringing up that idea!). This data can be used to assess the public attention to Covid-19 across countries and over time within a given country. The data is available at the country, regional and city level but availability varies across countries as Google Trends provides only more granular data for regions with high search volumes.
    download_wbank_data(): Downloads and tidies additional country level information provided by the World Bank using the {wbstats} package. These data allow researchers to calculate per capita measures of the virus spread and to assess the association of macro-economic variables with the development of the virus.
    download_merged_data(): Downloads all data sources and creates a merged country-day panel.

