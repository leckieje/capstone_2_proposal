# capstone_2_proposal

1. Protest or Riot?

  * One idea is to use the New York Times API to get articles and article tags about civil unrest events in the United States. I would then combine that data with an API pull from The Armed Conflict Location & Event Data Project of its data from the United States during some time period (at least several years). The goal would be to try and predict based on the features in the ACLED dataset and data gleaned from the Times API how the times would classify the event, as a protest or a riot. 
  
  * The approach would be to build a predictive model (current thought is a logististic regression) using features form the ACLED dataset including 'event_date', 'year', 'event_type', 'sub_event_type', 'actor1', 'assoc_actor_1', 'inter1', 'actor2', 'assoc_actor_2', 'inter2', 'interaction', 'region', 'location', 'latitude', 'longitude', 'geo_precision', 'source', and 'fatalities'. Target could either be the Times tags used to classify the article as a 'riot' or a 'protest' or maybe a textual/sentiment anlysis of the Times article (?? I see we cover some NLP methods before then). I would also think about expandinng the definition of 'riot' and 'protest' depending on how much data I can get. For instance one tag I have seen. is 'looting', which could be included in the riot category. In either case I could begin my search with the formal description "Demonstrations, Protests, and Riots" 
  
  * One method for combining the datasets would be to narrow the list of civil unrest events to those where ACLED cites The New York Times as its source, this way I can ensure a link between the Times covereage and the ACLED database. After a quick search over the last year of ACLED data, I found 353 instances of an event credited to the Times. My hope is that given a date, location and the knowledge the event appeared in the Times will be enough to merge the datasets properly. 

[The New York Times API](https://developer.nytimes.com/)

[The Armed Conflict Location & Event Data Project](https://acleddata.com/data-export-tool/)


2. Police Misconduct Settlements



[Police Misconduct Settlements](https://github.com/fivethirtyeight/police-settlements)

[NYC Police Complaints](https://www1.nyc.gov/site/ccrb/policy/data-transparency-initiative-complaints.page#outcome)


3. Predicting Test Scores Based on Census Data 


[Regents (Public) 2014,15,17,18,19](https://data.cityofnewyork.us/Education/2014-15-to-2017-19-NYC-Regents-Exam-Results-Public/bnea-fu3k)
[Regents All 2014-2017](https://data.cityofnewyork.us/Education/2014-2017-Regents/cbrh-qrk4)
[2013-2018 School Math Results](https://data.cityofnewyork.us/Education/2013-2018-School-Math-Results/m27t-ht3h)
[2013-2019 Match Test Results Charter-Schools](https://data.cityofnewyork.us/Education/2013-2019-Math-Test-Results-Charter-School/3xsw-bpuy)
[2013-2019 English Language Arts Test Results Charter-School](https://data.cityofnewyork.us/Education/2013-2019-English-Language-Arts-ELA-Test-Results-C/sgjd-xi99)
[2013-2019 ELA Test Results Sshool - SWD/Ethnicity/Gender/Economic Status/ELL](https://data.cityofnewyork.us/Education/2013-2019-English-Language-Arts-ELA-Test-Results-S/gu76-8i7h)
[2013-2019 Math Test Results Sshool - SWD/Ethnicity/Gender/Economic Status/ELL](https://data.cityofnewyork.us/Education/2013-2019-Math-Test-Results-School-SWD-Ethnicity-G/74ah-8ukf)





