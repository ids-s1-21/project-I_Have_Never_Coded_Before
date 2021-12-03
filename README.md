Innocent Death’s caused by Police Project
================
by Abhey , Reuben , Mieke

## Summary

As of recently, there has been a lot of uproar about the police killing people, for example the recent death of George Floyd that sprouted mass protests. As a result, we decided to choose the "Innocent Deaths caused by Police" data-set from kaggle. We chose this data-set because we wanted our project to be meaningful and show information that can shed light on an important issue. 

The first bit of cleaning that we had to do was to make a zip code that would group countries together since having 50 different states on the x-axis would be hard to read. As a result, we took the zip code by the first number which grouped states together by geographical location. Additionally, we extracted the year from the date so we could group by year. Finally, we mutated the "European-American/White" race since one of the observations had different capitalization, so we added it by changing the capitalization.

 For the first plot, we wanted to identify whether there was any change to the number of police deaths over time. Although time itself does not have a causal relationship with police deaths, we can infer that potentially political and societal factors do have an effect. These factors will change and alter the number of deaths at the hands of police each year. We facetted our plot by race to identify whether there were any noticeable changes over time.
 
Overall, we found that Native American/Alaskan, Asian/Pacific Islander and Middle Eastern had a relatively low number of deaths per year. In contrast, European – American/White and African – American/Black have relatively high deaths per year. Both show an increase from 2000 until around 2015 and then plateau before having a noticeable decrease in 2021. This is understandable as 2021 isn’t a full year sample. However, another striking feature is the close proximity in the number of deaths between European – American/White and African – American/Black races. Which begs the question how do deaths per year for each race reflect as a proportion of the population?

So, we sampled three years 2000(1), 2010(2) and 2019(3) and then for each race divided the number of deaths by the race population for that year. We could then identify whether there had been a change in police deaths for each race per capita. We used data gathered from the US census for these years. An issue that cropped up was that there wasn’t a population category for Middle Eastern in the census, so we added the Middle Eastern deaths to the Asian/Pacific Islander deaths and divided this result by the Asian/Pacific Islander population. This allowed us to analyse all races for each year.
 
We found that in 2000 the highest police deaths per capita for a race was for Native American/ Alaskan group followed by African – American/Black. In 2010 and 2019 the highest police deaths per capita was clearly recorded as African – American/Black. This would strongly suggest that race does contribute to a person’s likelihood of being killed by the police and confirms our preconceptions that there is racial discrimination within the US police force. Furthermore, there is an increase in deaths by police per capita for this race over time suggesting that the racial discrimination within the police force is prevalent and is getting worse. 

 For our fourth plot, we wanted to graph something that could take into 2 variables, the state and year, with the number of deaths on the y-axis. We knew that we couldn’t facet the graph with 50 different states so we used the first number of the zip code which we mutated when cleaning the data. When we plotted this graph we found that the top three states with the highest frequency of deaths were the states that started with the zipcode 3 (southeast states),7 (south states), and 9 (west states). The states with the least amount of deaths are in the central but we can account for the fact that central states in general have a lesser population compared to other states. 

We then wanted to visualise our results from the Police Deaths by Grouped States plot and view how this looked on a geographical map(4). We did this by calculating the proportions of death in a state against the population of that state in 2010. The heatmap shows us that the proportions of deaths in the state seem to be much higher in the south, which seems to be where views are more pro-police. Additionally, we can see that there is a white space in the middle of the map, which is where Wyoming is meant to be. This indicates to us that there were no deaths from the police in Wyoming in 2010. This seems to line up with the fact that Wyoming is one of the safest states in the US and about 9 in 10 people feel safe living there. 
 
We repeated this for 2019 which showed the central states having the greatest police related deaths per capita. In general these states are pro-gun(5) in contrast to the more democratic(6) western coastal states and north-eastern coastal states which have less police related deaths. Thus suggesting, the state you live in plays a role in how likely you are to be shot by the police.





## Presentation

Our presentation can be found [here](presentation/presentation.html).

## Data

Kaggle.com. 2021. Innocent Deaths caused by Police (All time). [online] Available at: <https://www.kaggle.com/kannan1314/innocent-deaths-caused-by-police-all-time/version/> [Accessed 22 October 2021].

## References

(1) Census.gov. 2021. [online] Available at: <https://www.census.gov/prod/2001pubs/cenbr01-1.pdf> [Accessed 30 November 2021].

(2) Census.gov. 2021. [online] Available at: <https://www.census.gov/prod/cen2010/briefs/c2010br-02.pdf> [Accessed 30 November 2021].

(3) En.wikipedia.org. 2021. Demographics of the United States - Wikipedia. [online] Available at: <https://en.wikipedia.org/wiki/Demographics_of_the_United_States#Race_and_ethnicity> [Accessed 30 November 2021].

(4) Ggplot2.tidyverse.org. 2021. Polygons from a reference map — geom_map. [online] Available at: <https://ggplot2.tidyverse.org/reference/geom_map.html> [Accessed 26 November 2021].

(5) Worldpopulationreview.com. 2021. Gun Ownership by State 2021. [online] Available at: <https://worldpopulationreview.com/state-rankings/gun-ownership-by-state> [Accessed 30 November 2021].


(6) En.wikipedia.org. 2021. Red states and blue states - Wikipedia. [online] Available at: <https://en.wikipedia.org/wiki/Red_states_and_blue_states> [Accessed 30 November 2021].


