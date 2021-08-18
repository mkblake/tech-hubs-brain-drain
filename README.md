# Tech Hubs and Brain Drain - Across the United States

## Project Summary
This capstone project maps the emergence of technology hubs across the United States from 2000 to 2017, and investigates the relationship between the growth of tech hubs and the phenomenon known as “brain drain” across the United States. 

## Motivation
As a native Nebaskan, I am familiar with the phenomenon known as brain drain, wherein highly educated residents leave their home state to pursue opportunities elsewhere. As a Nashville resident since 2010, I have also witnessed the city’s enormous growth over the past decade. In recent years, Nashville has seen [impressive job growth](https://mtsunews.com/state-of-middle-tennessee-tech-report-2020/) in the technology sector. [Oracle bringing 8,500 jobs](https://www.marketwatch.com/story/oracle-plans-1-2-billion-campus-in-nashville-creating-8-500-jobs-01618437488) to Nashville in the next decade will likely solidify Nashville as a tech hub for years to come. Are tech hubs and brain drain related? How have cities and states across the country fared in the last 20 years? 


## Background Reading

[How Smaller Cities Are Trying to Plug America's Brain Drain](https://www.wired.com/story/how-smaller-cities-trying-plug-brain-drain/) - Wired

[Losing Our Minds: Brain Drain Across the United States](https://www.jec.senate.gov/public/index.cfm/republicans/2019/4/losing-our-minds-brain-drain-across-the-united-states) - United States Congress, Joint Economic Committee, Social Capital Project

[The Case for Growth Centers: How to Spread Tech Innovation Across America](https://www.brookings.edu/research/growth-centers-how-to-spread-tech-innovation-across-america/) - The Brookings Institution


## Definitions
**Tech Hub**: A metropolitan statistical area (MSA) that met at least one of the following conditions in 2017:
* Total count of technology jobs  - Top 10 in the U.S.
* Jobs per 1,000 - 76 and above (statistical outliers)
* Location Quotient - 1.7 and above (statistical outliers)


**Brain Gain** occurs when states "are keeping and receiving a greater share of [highly educated] adults than they used to." - [Losing Our Minds](https://www.jec.senate.gov/public/index.cfm/republicans/2019/4/losing-our-minds-brain-drain-across-the-united-states)

**Brain Drain** occurs when states are "hemorrahging their homegrown talent and failing to attract out-of-staters who are highly educated." - [Losing Our Minds](https://www.jec.senate.gov/public/index.cfm/republicans/2019/4/losing-our-minds-brain-drain-across-the-united-states)

**Highly Educated** indicates an adult between the ages of 31 and 40 who resides in the top third of the national education distribution. 

## Data Questions
* Is it possible for a tech hub to emerge in a state despite documented brain drain in that state?
* Is is possible to observe the emergence of a tech hub in one state and a brain drain in neighboring states?
* Do states that have tech hubs experience less brain drain overall?


## Data Sources
[Occupational Employment and Wage Statistics (OEWS) Reports](https://www.bls.gov/oes/) - Bureau of Labor Statistics, United States Department of Labor
- State-level data
- Metropolitan Statistical Area (MSA) level data

[Losing Our Minds: Brain Drain across the United States](https://www.jec.senate.gov/public/index.cfm/republicans/2019/4/losing-our-minds-brain-drain-across-the-united-states) - Social Capital Project, United States Congress Joint Economic Committee  


## Methodology
I downloaded .csv source files from my two data sources. I cleaned the OEWS files in Jupyter notebooks, using Python. I selected columns relevant to my project, renamed column headers as necessary, and selected rows relevant to my project, based on the technology occupational codes for that year. (See Excel file, "Technology Job Codes by Year" in this repo.) This resulted in one dataframe for each year, 2000, 2010, 2017. I appended these three dataframes together, produced a .csv file, converted it to an Excel file, added the Brain Drain data as an additional sheet, and used Excel to connect my data source to Tableau.


## Key Insights