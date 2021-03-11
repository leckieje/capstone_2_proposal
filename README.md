# capstone_2_proposal

### 1. Protest or Riot?

  * This proposal looks to use the New York Times API to get articles and article tags about civil unrest events in the United States. I would then combine that data with an API pull from The Armed Conflict Location & Event Data Project of its data from the United States during some time period (at least several years). The goal would be to try and predict based on the features in the ACLED dataset and data gleaned from the Times API how the times would classify the event, as a protest or a riot. 
  
  * The approach would be to build a predictive model (current thought is a logistic regression, but possibly a random forest) using features form the ACLED dataset including 'event_date', 'year', 'event_type', 'sub_event_type', 'actor1', 'assoc_actor_1', 'inter1', 'actor2', 'assoc_actor_2', 'inter2', 'interaction', 'region', 'location', 'latitude', 'longitude', 'geo_precision', 'source', and 'fatalities'. Target could either be the Times tags used to classify the article as a 'riot' or a 'protest' or maybe a textual/sentiment analysis of the Times article (?? I see we cover some NLP methods before then). I would also think about expanding the definition of 'riot' and 'protest' depending on how much data I can get. For instance, one tag I have seen. is 'looting', which could be included in the riot category. In either case I could begin my search with the formal description "Demonstrations, Protests, and Riots" 
  
  * One method for combining the datasets would be to narrow the list of civil unrest events to those where ACLED cites The New York Times as its source, this way I can ensure a link between the Times coverage and the ACLED database. After a quick search over the last year of ACLED data, I found 353 instances of an event credited to the Times. My hope is that given a date, location and the knowledge the event appeared in the Times will be enough to merge the datasets properly. 

[The New York Times API](https://developer.nytimes.com/)

[The Armed Conflict Location & Event Data Project](https://acleddata.com/data-export-tool/)


### 2. Electric Car Ownership Churn

  * This proposal looks to predict churn in electric car ownership -- i.e. those who bought an electric vehicle only to stop driving that vehicle in favor of a traditional gas powered vehicle -- in California.

    * Framing the problem: fleet turn over, NYT, March 10, 2021, [Electric Cars Are Coming. How Long Until They Rule the Road?](https://www.nytimes.com/interactive/2021/03/10/climate/electric-vehicle-fleet-turnover.html?action=click&module=Top%20Stories&pgtype=Homepage)
  
  * The data would likely come from three datasets:
  
    * [This dataset](https://data.mendeley.com/datasets/tb9yrptydn/2) of electric passenger cars with their specifications consists of 53 electric cars (each variant of a model – which differs in terms of battery capacity, engine power, etc. – is treated as separate) and 22 variables (25 variables, including make, model and “car name” merging these two previous). Not all the models would be applicable in this case as the dataset was compiled using only cars that could be purchased in Poland as new at authorized dealers. 

    * This study on ["Discontinuance among California's electric vehicle buyers"](https://zenodo.org/record/4586675#.YEomf5NKjlx) that contains the compiled responses of Californian drivers who chose to abandon their electric vehicle, and the reasons behind the decision.

    * Lastly, data on electric vehicle infrastructure from the [Alternative Fuels Data Center](https://afdc.energy.gov/stations/#/find/nearest) could be used to develop additional features that influenced the car owner's decisions.

* Full disclosure: I just came across the first two datasets in a newsletter this morning, so more research needs to be done to determine an appropriate way to merge these databases, iif possible. I did briefly look at the dataset of Polish car models, and many, although not all, are from manufacturers also common in California (BMW, Hyundai, Tesla, etc.).


### 3. Predicting Test Scores Based on Census Data 

  * This proposal's goal is to predict school level test scores based on data included in the test score data sets as well as socioeconomic and demographic census data. 

  * The approach would be to combine testing data from New York City schools, both public and charter, for math, English, and the Regent's exam with Census data on neighborhood level income, labor and other demographic information to train a random forest capable of predicting which of the four levels of outcomes (not meeting standards, partially meeting standards, meeting standards, meeting standards with distinction) each school falls into. 

  * Some work/research would still need to be done to figure out the appropriate method for combining the test and Census data. Below are several options for test score data sets. 

[Regents (Public) 2014,15,17,18,19](https://data.cityofnewyork.us/Education/2014-15-to-2017-19-NYC-Regents-Exam-Results-Public/bnea-fu3k)

[Regents All 2014-2017](https://data.cityofnewyork.us/Education/2014-2017-Regents/cbrh-qrk4)

[2013-2018 School Math Results](https://data.cityofnewyork.us/Education/2013-2018-School-Math-Results/m27t-ht3h)

[2013-2019 Match Test Results Charter-Schools](https://data.cityofnewyork.us/Education/2013-2019-Math-Test-Results-Charter-School/3xsw-bpuy)

[2013-2019 English Language Arts Test Results Charter-School](https://data.cityofnewyork.us/Education/2013-2019-English-Language-Arts-ELA-Test-Results-C/sgjd-xi99)

[2013-2019 ELA Test Results School - SWD/Ethnicity/Gender/Economic Status/ELL](https://data.cityofnewyork.us/Education/2013-2019-English-Language-Arts-ELA-Test-Results-S/gu76-8i7h)

[2013-2019 Math Test Results School - SWD/Ethnicity/Gender/Economic Status/ELL](https://data.cityofnewyork.us/Education/2013-2019-Math-Test-Results-School-SWD-Ethnicity-G/74ah-8ukf)


### Backup Datassets:

*Police Misconduct Settlements*

[FiveThirtyEight](https://fivethirtyeight.com/features/police-misconduct-costs-cities-millions-every-year-but-thats-where-the-accountability-ends/) recently published a story on settlements reached in police misconduct cases. This proposal would try and find other data sources that could be combined with the settlement file from New York City to create a linear regression capable of predicting settlement amounts and ranking features linked with payout amounts. The relevant columns of the data set include claim type, incident date, location (street/ street address), attorney, settlement date, settlement amount. 

More research would need to be done to find a suitable pair dataset to expand the features. Below I suggest using Census data, and that idea interests me here as well. How to connect the settlement data locations and the Census data is another challenge that would need to be overcome. 

[Police Misconduct Settlements](https://github.com/fivethirtyeight/police-settlements)

---

[Medical Malpractice Payments](https://www.npdb.hrsa.gov/resources/publicData.jsp)

The NPDB Public Use Data File contains selected variables from medical malpractice payment and adverse licensure, clinical privileges, professional society membership, and Drug Enforcement Administration (DEA) reports (adverse actions) received by the NPDB concerning physicians, dentists, and other licensed health care practitioners. It also includes reports of Medicare and Medicaid exclusion actions taken by the Department of HHS Office of Inspector General.

  * 53 columns listed [here](https://www.npdb.hrsa.gov/resources/puf/pufFormatSpecifications.jsp)

---

[Rat Sightings in NYC](https://data.cityofnewyork.us/Social-Services/Rat-Sightings/3q43-55fe)
