# Tech Hubs and Brain Drain - Across the United States

## Project Summary
This capstone project maps the emergence of technology hubs across the United States from 2000 to 2017, and investigates the relationship between the growth of tech hubs and the phenomenon known as “brain drain” across the United States. 

## Motivation
As a native Nebaskan, I am familiar with the phenomenon known as brain drain, wherein highly educated residents leave their home state to pursue opportunities elsewhere. As a Nashville resident since 2010, I have also witnessed the city’s enormous growth over the past decade. In recent years, Nashville has seen [impressive job growth](https://mtsunews.com/state-of-middle-tennessee-tech-report-2020/) in the technology sector. [Oracle bringing 8,500 jobs](https://www.marketwatch.com/story/oracle-plans-1-2-billion-campus-in-nashville-creating-8-500-jobs-01618437488) to Nashville in the next decade will likely solidify Nashville as a tech hub for years to come. Are tech hubs and brain drain related? How have cities and states across the country fared in the last 20 years? 


## Background Reading

[How Smaller Cities Are Trying to Plug America's Brain Drain](https://www.wired.com/story/how-smaller-cities-trying-plug-brain-drain/) - Wired

[Losing Our Minds: Brain Drain Across the United States](https://www.jec.senate.gov/public/index.cfm/republicans/2019/4/losing-our-minds-brain-drain-across-the-united-states) - United States Congress, Joint Economic Committee, Social Capital Project

[The Case for Growth Centers: How to Spread Tech Innovation Across America](https://www.brookings.edu/research/growth-centers-how-to-spread-tech-innovation-across-america/) - The Brookings Institution

[State of Middle Tennessee Tech Report 2020](https://www.middletntechjobs.com/state-of-middle-tennessee-tech-2020/) - Dr. Amy Harris, associate professor of information systems and analytics, MTSU, in partnership with the Greater Nashville Technology Council


## Definitions
**Tech Hub**: A metropolitan statistical area (MSA) that met at least one of the following conditions in 2017:

* Total count of technology jobs  - Top 10 in the U.S.
* Jobs per 1,000 - 76 and above (statistical outliers)

**Brain Gain** occurs when states "are keeping and receiving a greater share of [highly educated] adults than they used to." - [Losing Our Minds](https://www.jec.senate.gov/public/index.cfm/republicans/2019/4/losing-our-minds-brain-drain-across-the-united-states). This measure is calculated by subtracting the percentage of a state's highly educated entrants from that state's percentage of highly educated leavers. If there are fewer leavers than entrants, the resulting number will be negative, indicating brain gain.

**Brain Drain** occurs when states are "hemorrahging their homegrown talent and failing to attract out-of-staters who are highly educated." - [Losing Our Minds](https://www.jec.senate.gov/public/index.cfm/republicans/2019/4/losing-our-minds-brain-drain-across-the-united-states). This measure is calculated by subtracting the percentage of a state's highly educated entrants from that state's percentage of highly educated leavers. If there are more leavers than entrants, the resulting number will be positive, indicating brain drain.

**Highly Educated** describes an adult between the ages of 31 and 40 who resides in the top third of the national education distribution. 

**Jobs per 1,000** is a measure indicating the number of technology jobs per 1,000 jobs in the given area. It helps to answer the question, "Do technology jobs make up a large proportion of jobs in our area?" 

## Data Questions
* Is it possible for a tech hub to emerge in a state despite documented brain drain in that state?
* Is is possible to observe the emergence of a tech hub in one state and a brain drain in neighboring states?
* Do states that have tech hubs experience less brain drain overall?


## Data Sources
[Occupational Employment and Wage Statistics (OEWS) Reports](https://www.bls.gov/oes/) - Bureau of Labor Statistics, United States Department of Labor. This datasource provides detailed estimates of how many jobs in a particular occupation exist in an area; this information is available by state & by MSA.


[Losing Our Minds: Brain Drain across the United States](https://www.jec.senate.gov/public/index.cfm/republicans/2019/4/losing-our-minds-brain-drain-across-the-united-states) - Social Capital Project, United States Congress Joint Economic Committee  


## Methodology
I downloaded .csv source files from my two data sources. I cleaned the OEWS files in Jupyter notebooks, using Python. I selected columns relevant to my project, did some string cleaning and renamed column headers to create consistent column names across all years, and selected rows relevant to my project, based on the technology occupational codes for that year. (See Excel file, "Technology Job Codes by Year" in this repo.) This resulted in one clean dataframe for each year, 2000, 2010, 2017. I appended these three dataframes together, produced a .csv file, converted it to an Excel file, added the Brain Drain data as an additional sheet, and used Excel to connect my data source to Tableau.


## Key Insights
### 19 Tech Hubs...
- Atlanta-Sandy Springs-Roswell, GA
- Austin-Round Rock, TX
- Boston-Cambridge-Newton, MA
- Boulder, CO
- California-Lexington Park, MD
- Chicago-Naperville-Arlington Heights, IL
- Dallas-Plano-Irving, TX
- Durham-Chapel Hill, NC
- Framingham, MA
- Huntsville, AL
- Los Angeles-Long Beach-Glendale, CA
- Lowell-Billerica-Chelmsford, MA
- New York-Jersey City-White Plains, NY-NJ
- San Francisco-Redwood City-South San Francisco, CA
- San Jose-Sunnyvale-Santa Clara, CA
- Seattle-Bellevue-Everett, WA
- Silver Spring-Frederick-Rockville, MD
- Trenton, NJ
- Washington-Arlington-Alexandria, DC

### Across 12 States...
- Alabama
- California
- Colorado
- Illinois
- Georgia
- Maryland
- Massachussetts
- New York
- North Carolina
- New Jersey
- North Carolina
- Washington

## Key Insights: Data Question 1
* Is it possible for a tech hub to emerge in a state despite documented brain drain in that state?

Yes! It is possible for a tech hub to grow in job volume despite active brain drain occurring across the state during the same time period, as evidenced by Huntsville, AL. 

Two more tech hubs grew in job volume while their state lost some ground in their brain gain measure: Framingham, MA and Lowell-Billerica-Chelmsford, MA. 

However, all three of these hubs had a decrease in jobs per 1,000 between 2010 and 2017.

Another pattern than emerged was the growth of tech hubs (as measured by an increased in both job volume and jobs per 1,000) in states that were losing ground in brain gain during that same period. These tech hubs were Atlanta-Sandy Springs-Roswell, GA, Boston-Cambridge-Newton, MA, Boulder, CO, Chicago-Naperville=Arlington Heights, IL, Durham-Chapel Hill, NC, New York-Jersey City-White Plains, NY-NJ.

The remaining tech hubs resided in states experiencing active brain gain between 2010 and 2017, or it was Washington, D.C., which did not have a brain drain measure.


## Key Insights: Data Question 2
* Is is possible to observe the emergence of a tech hub in one state and a brain drain in neighboring states?

Yes! Atlanta-Sandy Springs-Roswell, GA and Austin-Round Rock, TX are prime examples of this phenomenon. Both experienced tech job volume growth from 2000 to 2017, and tech jobs per 1,000 growth from 2010 to 2017, while one or more adjacent states experienced brain drain. 

## Key Insights: Data Question 3
* Do states that have tech hubs experience less brain drain overall?

Yes! We can definitely observe a pattern here. Out of the 19 tech hubs identified in this study, only one was located in a state with positive brain drain measures.

## Additional Key Insights

In 2017,  Nashville was not yet a tech hub by the definition established above. In fact, the Nashville MSA was only about half as “techy” as the Austin, TX MSA in 2017.

The presence of military bases and/or defense contractor employers can contribute to the presence of a tech hub in a given area, as evidenced by California-Lexington Park, MD, home of Naval Air Systems Command. 
