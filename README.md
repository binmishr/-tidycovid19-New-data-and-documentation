# tidycovid19-New-data-and-documentation

The details of the codeset and plots are included in the attached Adobe Acrobat reader (.pdf) file in this repository. 
You need to download the same to view the contents. There are referrals to other contents in BLUE colour also to follow.

As the underlying data sources change their format and access methods often, I have no plans to publish the package on CRAN for the time being. So, to install the package, you need to have the {remotes} package installed. Then, you can install and attach {tidycovid19} along with some other packages that we will need below by:

library(tidycovid19)
library(tidyverse)
library(ggrepel)
library(gghighlight)
library(zoo)
