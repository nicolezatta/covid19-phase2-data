# COVID19-Italy-phase2-enriched-dataset

## Description
This repository contains compiled and curated datasets on COVID-19 epidemiology at the regional level in Italy, in the date range November 2020-May 2021. The repository is designed to enable data analysis on the effects of different kinds of restrictions against the spreading of the infection as well as on the efficacy of the estimators used to predict when such restrictions should be applied. This repository is explicitly designed to give access to this data to non-Italian speakers.

The repository was the outcome of the Computational Physics Laboratory Course taught in March-May 2021 at the Physics Department of the University of Milan (teachers: Marco Cosentino Lagomarsino, Marco Gherardi; Data Challenge Supervisors: Federico Bassetti, Fabrizio Capuani, Pietro Cicuta, Jacopo Grilli). For more information about the course, see [this preprint](https://arxiv.org/abs/2104.09394) about the 2020 edition.

## Authors 
Marco Cosentino Lagomarsino* (University of Milan and IFOM Foundation, Milan)
Matteo Citterio (University of Milan)
Marco Gherardi  (University of Milan)
Dave Parmegiani (University of Milan)
Nicole Zattarin** (University of Milan)

\* marco.cosentino-lagomarsino@ifom.eu 

\*\* nicole.zattarin@gmail.com 

## Repository organization
The repository is divided into the following folders:

- daily\_region\_data/ (a full dataset with different kinds of standard epidemiological data, extracted from the Italian Civil Protection GitHub)
- region\_colors/ (compiled datasets regarding the restrictions imposed by the Italian government in the considered time period)
- reports\_ISS/ (compiled datasets with risk indicators from the Italian National Institute of Health---ISS---weekly reports)
- mortality/  (deaths per province per month, from the Italian Statistics Institute---ISTAT)
- population\_stats/ (population statistics by Italian provinces and regions)
- results/ (a report of some results we obtained with these datasets, and corresponding figures)

## Datasets
### Introduction
From November 2020, the spread of the COVID-19 pandemic in Italy made it necessary to introduce restrictions, in order to reduce the impact of this disease on public health.

### 1. Daily region data
The dataset available in the [daily\_region\_data](https://github.com/nicolezatta/COVID19-Italy-phase2-enriched-dataset/tree/main/daily_region_data) folder focuses on the daily evolution of epidemiological data during the so called "phase 2" of COVID-19 pandemic (November 2020-May 2021). We provide daily evolution of parameters such as registered new cases, deaths, and hospitalizations. This kind of data allows one to study the spread of the pandemic through time-series: you can see an example of this in [RESULTS.md](https://github.com/nicolezatta/covid19-phase2-data-Italy/tree/main/results/RESULTS.md).

For a full description of the dataset see: [DAILY_DATA.md](https://github.com/nicolezatta/covid19-phase2-data-Italy/tree/main/daily_region_data/DAILY_DATA.md).

### 2. Restrictions
The [region\_colors](https://github.com/nicolezatta/COVID19-Italy-phase2-enriched-dataset/tree/main/region_colors) folder contains data on the regional restrictions imposed by the government over the period from 2020-11-06 to 2021-05-16. We provide two different datasets that are solely focused on such restrictions, and keep track of the restriction color in each region every day.

For a full description of the datasets see: [REGIONS_RESTRICTIONS.md](https://github.com/nicolezatta/covid19-phase2-data-Italy/tree/main/region_colors/REGIONS_RESTRICTIONS.md).

***Description of the restriction regimes***

We will now provide a description of the restrictions imposed by the Italian government during the "phase 2" period that extends from November 2020 to May 2021. Such restrictions were applied in an attempt of containing the spread of the COVID-19 epidemic.

In October 2020, the Ministry of Health and the ISS published a “toolbox” for Public Health Authorities responding to the SARS-CoV-2 outbreak in Italy, based on the 8 WHO Strategic Pillars for COVID-19 response. The aim of this project was to prepare a strategy for the autumn-winter season, as described in the following document:
"[Prevention and response to COVID-19: evolution of strategy and planning in the transition phase for the autumn-winter season](https://github.com/nicolezatta/covid19-phase2-data-Italy/tree/main/COVID%2019_%20strategy_ISS_MoH.pdf)".

A compartmental strategy was adopted, differentiating the imposed restrictions in each region according to stress on the healthcare system, number of new cases, intensive care occupancy and many other indicators (the list of which can be found in the [INDICATORS.md](https://github.com/nicolezatta/covid19-phase2-data-Italy/tree/main/reports_ISS/INDICATORS.md) file in the [reports\_ISS](https://github.com/nicolezatta/COVID19-Italy-phase2-enriched-dataset/tree/main/reports_ISS) folder).

The names of the different imposed regimes (or "zones") are, in ascending order of restraint, "white", "yellow", "orange" and "red". The "white zone" corresponds to a level of restraint close to "normality", with open restaurants and shops, and no limitations of movement across the entire region; on the opposite side of the spectrum, in the "red zone" the majority of shops are closed and commercial activities are heavily reduced, on top of travels between cities being forbidden (except for emergencies). Moreover, such restrictions have been subject to change over time, and updated information about the restrictions can be found on the [site](http://www.salute.gov.it/portale/nuovocoronavirus/dettaglioFaqNuovoCoronavirus.jsp?lingua=english&id=230#11) of the Italian Ministry of Health.

![](results/images/zones_restrictions.png)

We describe below the restrictions in every zone referring to the period covered by our datasets. Starting from May 2021, when we are assembling this repository, the restrictions are being gradually released.

- _White zone restrictions_: Curfew is applied from 11.30pm to 5am. Outside of curfews, people are allowed to move freely across neighboring regions that are also white zones. School attendance is re-established when possible, while public transports may carry passengers up to half of their capacity. Restaurants are open until 11 pm while bars are only allowed to stay open until 9 pm. Shopping malls and stores are open. Museums are allowed to reopen on weekends. Gyms, theaters, cinemas and cultural centers may reopen gradually under such restrictions, but that didn't happen in the time period considered in this repository.

- _Yellow zone restrictions_: Curfew is applied from 11pm to 5am. Outside of curfews, movements are allowed only within the same region. Travelling to other regions was allowed from November to mid-December 2020, but since then moving between yellow regions had been forbidden until the 26th of April 2021. School attendance is guaranteed for elementary and middle schools, and at 50% capacity for high schools. Public transports may carry passengers at half capacity. Restaurants can be open until 6pm, while delivery/takeaway is allowed until 11pm. In restaurants, it is only allowed to sit with a maximum of four people per table, unless the people sitting at the same table live together. Shopping malls are closed on weekends, while theaters and cinemas are closed. Gyms, theaters, cinemas and cultural centers may reopen gradually, but that didn't happen in the time period considered in this repository.

- _Orange zone restrictions_: Curfew is applied the same as in the yellow zone, but outside of it movements are only allowed within the same municipality. In towns with less than 5000 inhabitants it is possible to travel within a distance of 30km from the town. School attendance and public transport is regulated the same as in the yellow zone. Restaurants are open until 11pm only for delivery/takeaway. All other restrictions are the same of the yellow zone.

- _Red zone restrictions_: Curfew is applied from 10pm to 5am, but even outside of curfews movements within the same municipality are only allowed for work, study or health related reasons. Outdoors physical activity is allowed only if it is individual and in the vicinity of the own home. Schools attendance is guaranteed just up to 1st grade of middle school; high school students must stay home, as well as university students. Restaurants, bars and cafes are closed. Takeaway is only allowed until 10pm, but food delivery is allowed without restriction. Shops are closed, except for grocery stores, pharmacies, newsstands and other shops that sell essential goods.

### 3. Indicators for risk assessment
The [reports\_ISS](https://github.com/nicolezatta/COVID19-Italy-phase2-enriched-dataset/tree/main/reports_ISS) folder provides a compiled dataset for each weekly report published by the ISS, which is the Italian authority in the health field. Every week the ISS provides a report with all the indicators that are necessary to describe the pandemic situation in every region, in order to decide the right policy to apply locally. These reports are available just in Italian and as PDF documents, and they are all collected [here](https://www.iss.it/monitoraggio-settimanale).

These parameters refer to quantities such as the reproduction index Rt, hospitalizations and contact tracing capability. They played a key role in guiding the Italian Government to formulate policies. The indicators should describe the evolution of the pandemic, the ability of the Italian health-care system to face the consequences, and the degree of spreading of the disease. 

For a more detailed description of the datasets see the document: [INDICATORS.md](https://github.com/nicolezatta/covid19-phase2-data-Italy/tree/main/reports_ISS/INDICATORS.md).

### 4. Deaths
The [deaths.csv](https://github.com/nicolezatta/COVID19-Italy-phase2-enriched-dataset/tree/main/mortality/deaths_S2.csv) file in the [mortality](https://github.com/nicolezatta/COVID19-Italy-phase2-enriched-dataset/tree/main/mortality) folder contains a comparison between the mean deaths in 2015-2019 and 2020 deaths, taken from the Italian Institute of Statistics (ISTAT). The deaths are aggregated per province per month. This dataset is organized as follows (see also the file header):

- CodProv (Province ISTAT code); 
- Province name;
- Deaths per month in the period 2015-2019 (whole year);
- Deaths per month in 2020 (whole year);
- Deaths per month identified as covid cases (for the second semester of 2020).

### 5. Population statistics
The [population_stats](https://github.com/nicolezatta/covid19-phase2-data-Italy/tree/main/population_stats) folder provides two useful datasets referring to Italian provinces and regions, and can also be used to map provinces to their respective regions:

- [provinces_population.csv](https://github.com/nicolezatta/covid19-phase2-data-Italy/tree/main/population_stats/provinces_population.csv) provides a description of provinces' code and name, their population and the percentage over the total Italian population.
- [regions_population.csv](https://github.com/nicolezatta/covid19-phase2-data-Italy/tree/main/population_stats/regions_population.csv) refers to regions and provides data about the population amount, surface, density of inhabitants, number of towns and number of provinces in the region.

Note that the two provinces P.A.Trento and P.A.Bolzano together make the whole region Trentino-Alto-Adige; the [regions_population.csv](https://github.com/nicolezatta/covid19-phase2-data-Italy/tree/main/population_stats/regions_population.csv) file provides data referring to Trentino-Alto-Adige.

## Sources
- [Gazzetta Ufficiale della Repubblica Italiana](https://www.gazzettaufficiale.it/home)
- [ISS](https://www.iss.it/web/iss-en)
- [ISTAT](https://www.istat.it/en/archivio/240106)
- [Presidenza del Consiglio dei Ministri - Dipartimento della Protezione Civile](https://github.com/pcm-dpc)
