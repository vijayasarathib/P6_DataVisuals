#Data Visualization: U.S. Domestic Airline Performances - 2003-2015
by Vijayasarathi Balasubramanian

### Summary
i took the data from RITA site to explre and understand the different U.S. domestic airlines' performance for the years 2003-2015.  created visuals for annual average on-time arrivals for different airlines. 

### Design

#### Data Exploration (R)

   I downloaded the data from RITA(http://www.transtats.bts.gov) for the performance analysis. the data set which i downloaded had the data from 2003 to 2015. as its a raw data i had to clean a bit before use it for the analysis. i used the R studio to do the exploratory analysis, have included the rmd file in the source code. as part of the exploratory analysis plaotted different graphs and once among them was different airlines performance for the years. performance of airlines is defined as number of arrivals delayed of the arrivals. just explored the data using the simple line graphs. 

![First look](https://github.com/vijayasarathib/P6_DataVisuals/blob/master/img/1.png)

    
Though the picture looks attractive its difficult to form insight from this graph, i felt like reducing the number of airlines for the analysis might help us to bring some insight. so i went ahead and restricted the number of airlines in the data set to 6. then i just recreated the line chart discussed in the first step.

i just created another graph with total annual flights too. 

![closer view](https://github.com/vijayasarathib/P6_DataVisuals/blob/master/img/2.png)


after looking at the graph, it looks like we have enough details to understand these airlines. It shows how various airlines improved or worsened over time, and which airlines were currently performing the best, as of 2015.  It also showed the general trends that all 6 airlines experienced: an aggregate dip in performance from 2006 to 2008, individual peaks from 2010 to 2012, and a more recent drop from 2012 to 2014. the data we have so far for 2015 shows positive sign.

   then i went ahead of the performance trend analysis of the flight rather than summed up numbers, as the insgihts like  "Which airlines operates with high likely facotr of on time?" will be interesting to know. 

#### Data Visualization

  To create more focused visuals i used the D3.js and dimple.js. 
  steps followed : 
  -- fixed the scaling in the 'on time percentage' axis. 
  -- Overlay scatter plot points to emphasize each airline's individual data points at each year.
  -- Added transparency, as some areas of the graph (2010-2012) have considerable overlap.
  
  I took notes on the issues and reasons for unclear in first picture and tried to correct them in the focused graph. also noted the good points to carry on here too. i decided that having differnt color for each airline is important, as the visuals giving you better picture and observation. adjusted the axis and its scale to have clear picture. added the legend as well in the top right. 
  
  
#### Feedback
 I had a chance to interview few people in person and asked their feedback on the visuals i crated. below are the few comments : 
 
#### Person #1


> having different colors for lines is good, but I think it will be good to highlight individual airlines when we point them.  visual is not that user friendly to take the closer observation.
> 
> you can rephrase the title to match the y-axis or rephrase it better. legends can be right aligned for the better eye sight. 
> 
> other than that, it looks pretty clean and straightforward.

#### Person #2

> i could observe immediately that there is a large dip in in 2007 that 3 of the airlines experienced in performance.  after some more closer looking, I saw that the percentage varied from 65% to 100%.  I wonder if it would be more transparent by showing the full scale?
> 
> Having the right side of the chart open was nice, in addition to the points being spread apart; it was clear to see who the current "champ" is.
> 
> I think the main takeaway is that the competition is still "fair", in the sense that achieving the best performance is still a close match, and fair game.

#### Interview #3

> One thing that I didn't notice was that this was an interactive visual!  Hovering over the points was interesting, but I kind of wanted to see some of the additional data, like how many flights each airline had.
> 
> I liked that there were lines.  It made it easier to follow each "path" of points.  I could see how this would have been a lot more confusing if it were just the circles.
> 
> Honestly, after I got a grasp of what the chart was, I looked all the way to the right, because I wanted to see how these airlines were performing today.


### Post-feedback Design

After reviewing the feedback from the 3 people, updated the visual with the below changes:

- subdued and muted the grid lines.
- changed the chart title to be more consistent with the data presented.
- polished the tooltip variable names to be more natural.
- I added a `mouseover` event for the lines, so it would 'pop' it out and emphasize the path.  This would allow for better understanding of each individual airline's trend from 2003 to 2015.




### Resources

- [dimple.js Documentation](http://dimplejs.org/)
- [Data Visualization and D3.js (Udacity)](https://www.udacity.com/course/viewer#!/c-ud507-nd)
- [D3 multi-series line chart with tooltips and legend](http://bl.ocks.org/Matthew-Weber/5645518)
- Various [Stack Overflow](http://stackoverflow.com/search?q=dimple.js) posts

### Data

- `data/data.csv`: cleaned and truncated dataset, utilized in final dimple.js implementation

