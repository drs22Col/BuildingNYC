# BuildingNYC

![Add image](https://raw.githubusercontent.com/kkkddder/BuildingNYC/master/Images_ReadMe/TitleShot.png)

Hurricane Sandy hit the Staten Island neighborhood of Oakwood Beach particularly hard, battering the shore-side homes and taking the lives of 43 residents on October 29, 2012. For decades the neighborhood had been plagued with flooding problems, and now poor planning had finally led to devastating results. 

How did the neighborhood try to rebuild? Our website, called "Razing New York," recounts a story of transformation. While other parts of New York were assigned to a city-run rebuilding program beset with problems, Oakwood Beach was offered a buy out plan as part of a wetlands reseeding program run by the state under Governor Cuomo. When and which homes were demolished, what areas were most affected, and what was the impact of location and lot values? "Razing New York" offers many interactive features, embedded in a larger narrative context, that reveal hidden patterns in the seachange that has since occurred in that neighborhood.

For the survivors of Sandy, Oakwood represents a dramatic success story where the state finally stepped in with a plan that the majority of residents were thrilled to receive, though it left some steadfast owners who refused buy outs isolated in a transformed landscape.  

PROCESS 

We started by broadly considering the effects of Hurricane Sandy in NYC, and examined a report about the resilience of city buildings to Sandy and future hurricanes, NYC_SIRR_Buildings.pdf. Of the buildings that received red tags after Sandy, most  were two floors or less and had combustible frames (made of wood rather than steel). The report also discussed the risk to areas of NYC from future surges, potentially exacerbated by climate change.

We realized that PLUTO was a good source of data if we were going to explore this topic, or a related one, because it contains ownership info, addresses, building class, number of floors, assessed value, year the building was built and years it was altered. Later we noticed that PLUTO also included a category called Special Coastal Risk, and a Flood Insurance Indicator, which we also thought might be useful. We also realized we could integrate live images of the buildings on the lots at addresses listed in PLUTO through Google Earth, so that seemed very promising in terms of visualization potential.  

The next step was to gather PLUTO data from 2009 to 2017, starting a few years before Sandy hit in 2012. Originally we were looking at Staten Island and Queens: we identified severely flood areas in those two boroughs because we knew they were hit with a lot of damage. Initial data exploration and charts compared the years 2012 vs 2017, and severely flooded areas vs all of NYC, for Assessed Total Value, Built Year per Lot, Land use Per lot, etc for 10,000 lots. 

![Add image](https://raw.githubusercontent.com/kkkddder/BuildingNYC/master/Images_ReadMe/LandValue.png)

![Add image](https://raw.githubusercontent.com/kkkddder/BuildingNYC/master/Images_ReadMe/LandUse.png)

![Add image](https://raw.githubusercontent.com/kkkddder/BuildingNYC/master/Images_ReadMe/YearBuilt.png)


We pulled out owner information for Queens and Staten Island. And we identified the following data:

NYC open data - Damage By Sandy By Age
https://data.cityofnewyork.us/Housing-Development/Damage-By-Sandy-By-Age-Of-Building/mgjt-zuui

Land Use
NYC open data - Damage By Sandy By Land Use
https://data.cityofnewyork.us/Housing-Development/Damage-By-Sandy-By-Land-Use/tgvi-w9ww/data

We made maps from FEMA damage assessments after Hurricane Sandy, with red outlines to indicate the blockgroups where the most severe damage occurred:

![Add image](https://raw.githubusercontent.com/kkkddder/BuildingNYC/master/Images_ReadMe/MapExplore1.png)

![Add image](https://raw.githubusercontent.com/kkkddder/BuildingNYC/master/Images_ReadMe/MapExplore2.png)

![Add image](https://raw.githubusercontent.com/kkkddder/BuildingNYC/master/Images_ReadMe/MapExplore3.png)

![Add image](https://raw.githubusercontent.com/kkkddder/BuildingNYC/master/Images_ReadMe/MapExplore4.png)

We also made charts to examine population and racial characteristics, as well as the relation between year built and number of floors for relevant Staten Island and Queens areas, but we later moved in a different direction. Our initial data explorations can be found here: https://kkkddder.github.io/BuildingNYC/Ass1.html

Further research narrowed down the geographical area of interest. We learned that there were two main programs that served the victims of Sandy. One was city-run and called Build it Back, and was focused on rebuilding and sometimes elevating damaged houses through contractors usually managed by the city. This federally funded program had some successes but was also plagued by problems. Immigrants in the affected areas did not know about the program at first, there were not enough resources devoted to the program, and contractors had a hard time making homes storm-proof within the allotted budget, among other things. Several years later, there were still issues. When DeBlasio took over as mayor he allocated more resources to the program, but even with that, only 87% of the eligible homes have been rebuilt. People apparently dropped out of the program after years of frustration, so it is not clear if this number is indicative of the actual completion rate. 

A second main program was run by the state government, initiated by Governor Andrew Cuomo. This program invested $200 million to buy back the land / damaged homes at pre-Sandy rates in three devastated areas of Staten Island: Oakwood Beach, Ocean Breeze, and Graham Beach. The plan was to demolish those battered homes and rewild the land (seeding it), returning it to wetlands. (This strategy is called managed retreat.) The upside here was two-fold: people could quickly move on with their lives, and the program eliminated the risk of future damage from storms in this waterfront area., because the land is restored to its natural floodplain function. (Other areas in NYC such as Williamsburg, Greenpoint, and Long Island City are rebuilding on the waterfront and tens of thousands of new residents are moving in, a risky proposition.) A large percentage of people in these SI waterfront areas decided to take the buyout offers. 

Here are just some of the sources we used in the research phase:

Sandy: NYC build it back
http://www.nyc.gov/html/recovery/html/home/home.shtml

NYCHA Sandy Recovery & Progress
http://www1.nyc.gov/site/nycha/about/recovery-resiliency.page

Sandy Progam Efficacy and News 

https://www.economist.com/blogs/democracyinamerica/2014/10/hurricane-sandy

https://www.theguardian.com/us-news/2017/oct/27/hurricane-sandy-five-years-later-climate-change

https://ny.curbed.com/2017/10/27/16554180/hurricane-sandy-relief-build-it-back-housing

http://www.nyc.gov/html/recovery/downloads/pdf/october_2017_build_it_ 

https://www.nytimes.com/2017/10/29/nyregion/hurricane-sandy-5-years-rebuilding.html

https://ny.curbed.com/2016/10/27/13431288/hurricane-sandy-staten-island-wetlands-climate-change

https://stormrecovery.ny.gov/housing/buyout-acquisition-programs

https://www.fema.gov/building-code-resources


The next goal was to develop a sketch for the website and the main data visualization. We decided we would focus our analysis on one of the three devastated waterfront areas in SI, Oakland Beach, to keep the number of lots manageable for the data analysis and visualization. This area saw the most dramatic changes since the hurricane due to the state buyout program that aimed to demolish the homes in this vulnerable area and transform the land into wetlands.

All together, our study site at this point included 1284 lots in 2009 (before Sandy) and 1276 in 2017 (the most recent year of data available): we extracted this data from PLUTO. 

We identified which owner names referred to both the city and state recovery programs:

NY State Government
OwnerName = 'HOUSING TRUST FUND COR' OR 'HOUSING TRUST FUND CO' OR 'HOUSING TRUST FUN COR' OR 'HOUSING TRSUT FUND CO' OR  'HOSUING TRUST FUND CO' OR 'HOSING TRUST FUND COR'

Build it Back Program 
OwnerName = 'PROJECT REBUILD, INC.’

NY City Government (excluding Build it Back)
OwnerName = 'DEPT EVIRONMETAL PROT' OR OwnerName = 'DEPT OF ENVIRONMENTAL' OR OwnerName = 'NYC DEP' 

OwnerName = 'PROL PROPERTIES CORPO'

OwnerName = 'DCAS'

OwnerName = 'CITY OF NEW YORK'

Private Land Owners
OwnerName = 'JULIA KARTEN' OR 'I COHEN'

In Excel we generated a pivot table (and chart) to explore ownership changes after Sandy, which was in 2012:  

Year	DEP	Housing Trust	Prol Props	DCAS		Build it back	
2012	210		0				43		38		
2015	239		347				43		36			
2016	252		478				43		44			
2017	315		550				43		37				19	

City of New York						
	8						
	8						
	42						
	41						
	35			

We planned to later include private ownership and vacant lots as well. And in the final deliverable we planned to trace back the homes in our study site back to 2009, a few years before Sandy hits (in Oct 2012). 
							
We decided to make a huge interactive chart called Razing NYC of all the lots in our study site over time, from 2009 to 2017. The idea is to show how the lots change ownership over time, particularly after Sandy, and when and if the homes on the lots are demolished. The colors for each type of ownership would fade out when the home was demolished. When you hover over one of the rectangles / bands representing one of the lots, it will pull up a satellite photo of what the building at that lot looks like now. The photo will appear in a box to the right of the chart. 

Here is our initial sketch. 

![Add image](https://raw.githubusercontent.com/kkkddder/BuildingNYC/master/Images_ReadMe/Initial1.png)

![Add image](https://raw.githubusercontent.com/kkkddder/BuildingNYC/master/Images_ReadMe/Initial2.png)

![Add image](https://raw.githubusercontent.com/kkkddder/BuildingNYC/master/Images_ReadMe/Initial3.png)

The chart aims to make dramatically visible trends in the timing and effect of the state buy out program, which involved first buying the land and buildings, and then demolishing the homes to make way for wetlands. As will be visible in our graphic, houses bought by the state sometimes stood empty for years until the demolition occured. 

Although we could have just shown homes after Hurricane Sandy hit, by going back a few years, we were able to show another approach to flooding control in Oakwood, the Blue Belt, which was still in play years later, and which played a role in securing the state buy out program for Oakwood. 

In preparation for the working prototype, we coded lots by type of owner: 

Private Owners = 0	
Housing Trust Co = 1	  (state)
Project Rebuilt, Inc = 2	(city)
Dep. En. Protection = 3	 (city agency)
DCAS = 4 	              (city agency)
Prol Properties Corpo = 5	(this is a real estate company, so these homes were likely rentals)
Dead couple (I Cohen, Julia Karten) = 6	

We may add, cut or change some of these fields in our classification scheme as we learn more about the ownership data. It may be that there will be a Rental category made up of Prol Properties and other real estate companies, for example. 

A vertical red line at 2012 in the chart will indicate when Sandy hit. When a lot is bought by the state (or city in some cases) it will change color to indicate that, and when a home is demolished its (the lot's) color will be faded out. So if the lot was originally blue in the chart, the lot will look like a very light faded blue if/when it is demolished. 

The chart should also reveal the homes where people have refused the buyout program. The status and number of these homes is a sub-topic that we will explore further as we do more data analysis. Additional research led us to the concept of the jack-a-lantern landscape, areas pockmarked with vacant lots and holdouts. 

Other planned elements: a graphic, perhaps a line chart, that indicates how ownership changed over time in the aggregate. So there will be one line for each of the major owners, and we will see in which years they bought or increased their buying of homes. 

![Add image](https://raw.githubusercontent.com/kkkddder/BuildingNYC/master/Images_ReadMe/Initial4.png)

There will also be an introduction section that will set the stage by describing the destruction caused by Sandy, explain what happened to Oakwood Beach, and explain the different city and state programs, etc. The intro and other explanatory elements will offer a narrative frame for the visualizations. There will also be relevant photos from Oakwood Beach, such as a home destroyed by Sandy, a home being demolished by the state, ducks and geese who have moved back in, and jack a lantern homes. 
 
![Add image](https://raw.githubusercontent.com/kkkddder/BuildingNYC/master/Images_ReadMe/InitialResearch.png)

As we worked on creating a working prototype of our website, and refining our ideas and the layout in various ways, we decided to zero in on the lots in Oakland Beach that were closest to the shore and suffered the most damage from the storm. We started with 843 lots.
But some of these lots had missing information (including ownership and assessed values), so we excluded those lots as part of the data cleaning process (in Excel). In the end we had a total of 831 lots for our study site.

Here is the link for the dataset: https://drive.google.com/drive/folders/1JVgwBgYr7GYqiW1HhKtNC0AUaf_ldbQg?usp=sharing
They were extracted from PLUTO (https://www1.nyc.gov/site/planning/data-maps/open-data/dwn-pluto-mappluto.page)

By using the latitude and longitude data for each lot in PLUTO (2017), we were able to find the centroid of each lot in GIS. Then we used those coordinates in a Google Maps API to download satellite imagery for each lot. We used p5.js to create the large visualization that allows people to hover over each lot and see what each one looks like now (using that 2017 satellite imagery).

We refined our legend scheme so that it includes: Private Property, State Owned (Housing Trust), Build it Back, SI Blue Belt, and Other Municipal Ownership. In the p5 sketch, we first checked for ownership by each of these programs (after first recoding the data in an Excel file).

Then we checked the Building Area data column in PLUTO. If it was zero, that indicates that the lot is vacant. If a building area went to 0 in 2013, we concluded that it was destroyed by Sandy (since the hurricane struck in Oct 2012). If the building area went to 0 in succeeding years, we considered those demolitions. 

In the first draft of the prototype, we changed some of the colors and put in a pop up window for those who wanted to dig deeper into the Oakwood Beach story. That window included photographs for each stage in the narrative, though later we decided to integrate the narrative more directly into the website in a column running down the left side of the interaction. 

The placement and color scheme were prelimnary: we were mainly focused on getting all the info and making the prototype work in an interactive and smooth manner. One question was whether to make the satellite image fixed or relative; if it was fixed we could use the third column real estate, but in the end we preferred the other approach.

In the last week, we redesigned the layout, rewrote the narrative to work more closely with the visualization categories (adding a SI Blue Belt paragraph, for example), added a title image and end image, changed the photographs to black and white, etc. 

![Add image](https://raw.githubusercontent.com/kkkddder/BuildingNYC/master/Images_ReadMe/MainViz.png)

We finetuned the legend to make it clearer, with all the vacant colors next to their original colors when the lot was not vacant. And we decided to make the year bar at the top stick when users scroll down.

To glean patterns and information from our visualization, we made a clickable program that highlights and sorts lots by different properties: distance from the beach, total assessed value, and size of the lot. Originally we were going to offer buttons to re-sort the main visualization in these three ways. We later decided to do the resorting on three smaller versions of the main visualization. We put these smaller versions, ordered differently, next to each other in order to make patterns in buyouts and timing more visible.

![Add image](https://raw.githubusercontent.com/kkkddder/BuildingNYC/master/Images_ReadMe/ThreeImages.png)
              
We wrote text explaining the key takeaways from each of the three versions. 

![Add image](https://raw.githubusercontent.com/kkkddder/BuildingNYC/master/Images_ReadMe/Narrative.png)

We also created a statistical panel that indicated ownership trends over time. After discussion, we turned this panel into a line chart which we thought would be more visually effective. Different colored lines indicate five different ownership options: governor's office; SI Blue Belt; Buy it Back; vacant. 

![Add image](https://raw.githubusercontent.com/kkkddder/BuildingNYC/master/Images_ReadMe/Linechart.png)


FINAL REFLECTIONS

One of the key decisions we made was deciding to focus on a very dramatic incident of natural human interest, Hurricane Sandy and its aftermath. A lot of history, an unusual government buyout program, and the issue of jack-a-lantern landscapes combined to make this a rich story. The story of the profound transformation of Oakwood is unusual in the state program's efficacy and the willingness to return waterfront property to nature for sustainability reasons. The PLUTO data is rich and easily accessible, and by focusing on one neighborhood with such particulary dramatic changes, we were able to deeply explore the data and tell a compelling story. 

We were able to draw some novel conclusions by sorting the data by BBL, total assessed value, and lot size in the three small-scale visualizations towards the bottom. For example, one of the charts revealed that lots with lower total assessed value tended to be demolished before more valuable homes. Such patterns in demolitions are not something that has been explored before. And by putting the three charts next to each other, visual differences and similarities jump out at the viewer. We also made this sorting function interactive, both for clarity and to boost user interest. 

The narrative allows readers to delve deeper, gaining context about Oakwood's story and history, and works hand-in-hand with the visualization through a connected interactive feature. By clicking on titles in the narrative, related colored squares appear next to the visualization to identify which lots participated in the programs to which the summaries refer.  

In terms of design, we used the timing of Sandy, indicated by a red line that travels from the top to the bottom of the site, to provide visual unity to the disparate parts, as well as to make the time scale in all of them more immediately clear. In general, we tried to use a minimum of labelling in the images, and instead have visual elements make key points. We also made the photographs in the narrative black-and-white and a little transparent so as not to detract interest from the main visualization. The photographs at the top and bottom of the site represent beginning and endpoints for Oakwood's journey from waterfront oasis back to natural wetlands. 

One of the key constraints for this project was that we were not supposed to use maps. Our main visualization was our way of making a spatially compelling dramatization of what happened to a geographic area without using a map. The satellite images also were a way of integrating spatial data. Were we allowed to use maps and if we had more time, we would have included little maps below each satellite photo of a lot to show where that lot is located. We might also, were there more time, have done some statistical analysis, in particular around demolition times for example.

We all enjoyed working with each other, and the interdisciplinary skills of our team enriched the project. 



