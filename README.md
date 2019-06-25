[![License: CC BY-NC 4.0](https://img.shields.io/badge/License-CC%20BY--NC%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc/4.0/)

---
# Master's in Intelligence Interactive Systems (UPF)
# Thesis code release
### Master's thesis title: Evaluating potential biases in commercial people search engines
---

# Description

Different webdrivers have been designed to scrape, collect and, finally, store peoples' profiles from different commercial people search engines. A webdriver is an automaton system that is able to open a web browser window and simulate the human behaviour by taking actions such as clicking and scrolling in order to scrape the HTML source code and get the content of the different DOM elements regardless of the presence of embedded Javascript code. 

The data sources that have been analysed are Linkedin and Viadeo in Spain, France and United Kingdom, and Top Doctors in Spain, Colombia and Mexico. In the case of Linkedin and Viadeo, which are focused on job candidate search, the profiles have been obtained by perfoming queries in the search bars of the sites using a list of job tiles as query terms. On the other hand, since Top Doctors is a platform showing leading professionals related to the e-Health world the words used in this occasion are medical specialities. The data collected apart from the source, country and query perfomed, have been all the personal details and CV information available in the profiles, another personal characteristics that were not present and have been estimated or inferred from the full name of the peoole such as the age, gender or ethnicity and, most importantly, the ranking position or order in which every person was retrieved after the query. The ranking position will be very useful to determine if it exists any kind of discrimination or bias when showing these people. All this information been joined and collected in JSON format that is later indexed in a Elasticsearch index. The relevant profiles' information
can be found in .csv format [here](https://github.com/sgalinma/tfm-miis-data-release/).
Afterwards, data have been cleaned and filtered to proceed with the data analysis process. The object of study has been the general gender proportion per job title or medical speciality, data source and country in the Top 10 and Top 20 first positions of the ranking, as well as the fairness evaluation of the rankings respect to different protected groups. This second validation can be perfomed through the usage of the [FA\*IR algorithm](https://github.com/fair-search/fairsearch-fair-python) which will measure if the ranking is fair in a probabilistic way. 


\* Note: The implemented webdriver worked in late February 2019. Since the automaton system is scrapping data in real time from the websites, it is possible that in few time the code becomes obsolete due to changes in the HTML source of the platforms.
