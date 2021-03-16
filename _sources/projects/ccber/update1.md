# Update 1
## Week 1
We spent the first week learning about our research interest ([bees](https://www.wikiwand.com/en/Bee)) and exploring the [Global Biotic Interactions (GloBI)](https://www.globalbioticinteractions.org/about) dataset. Our data come from literature reports, human observations, and natural history specimen. 
Goal of GloBI is to structure data into a usable form (csv., tsv.). \
<img src="http://clipart-library.com/images/yTk4eXgTE.png" width="200" />\
During our weekly meeting with the sponsors, we gained substantial knowledge about bees, especially the vital role it plays in global biotic interactions. In particular, we want to focus our research on the interactions between bees and plants. Interactions are directional, i.e. "Apis Mellifera pollinates brasicca rapa" will be categorized into source, interaction, and target, respectively.\
The goal for this week is to get a sense of the strengths and liminations of differnt query methods. Our options are direct access to the data files, [rglobi](https://github.com/ropensci/rglobi) package, [GloBI Web API](https://github.com/globalbioticinteractions/globalbioticinteractions/wiki/API), and [Cypher](https://neo4j.globalbioticinteractions.org/browser/) on [Neo4j](https://neo4j.com/developer/cypher/). We discovered that these methods operate on the same dataset, which renders the same result regardless which one we use.


## Week 2
During our meeting for week 2, we went over the 8 levels of taxonomy, which is shown below. We also learned about the 7 bee families. For instance, the honey bee belongs to Apidae, the largest bee family. 
![](https://cdn.britannica.com/78/103778-050-D797CF4F/Animals-groups-organisms-succession-general-particular.jpg)

![](https://github.com/angelchen7/ucsb-ds-capstone-2021.github.io/blob/main/ucsb_ds_capstone_projects_2021/projects/ccber/Screen%20Shot%202021-01-29%20at%204.16.20%20PM.png?raw=true)

Then, we discussed our results from using rglobi, the GloBI Web API, and Cypher. Each querying method has its own pros and cons. For example, rglobi was easy to use, but it didn't seem to have complete information in all of its columns. Cypher had a big learning curve, so we chose to not use that method. In the end, we decided it was better to use the raw csv file, which was 15 GB, for completeness. 

The goals after this meeting were to take some time to explore the raw dataset, since it was huge, check for reflexiveness in the data, and begin thinking about how we want to visualize these pollination networks. Additionally, we needed to brainstorm how to work with large data files that need to be shared and updated periodically. Some of us chose to explore the dataset with R while others were more comfortable with Python.

## Week 3
We discussed the attributes and qualities of the raw data. Also, we explored different options for querying and subsetting the data in more detail. Our sponsors provided more insight on variations in the interactions data. Some of this variation includes: size, coloration, foraging behavior, and sociality of bees. There is significant diversity in the Apidae bee family. Classification and taxonomy can be used to filter some of this variation. 

![](https://github.com/angelchen7/ucsb-ds-capstone-2021.github.io/blob/main/ucsb_ds_capstone_projects_2021/projects/ccber/different_bees.png?raw=true "variation in Apidae")

Another topic for consideration was visualization. We learned of different methods to visualize network data. Some of our options included igraph & bipartite for R packages; NetworkX, Plotly, Dash for Python packages. By visualizing this data, we would gain more insight on the network structure and attributes of the data.

![](https://github.com/angelchen7/ucsb-ds-capstone-2021.github.io/blob/main/ucsb_ds_capstone_projects_2021/projects/ccber/Rplot04.png?raw=true)


## Week 4

This week we focused on the specific bee family melittidae to create interaction networks. Our python group had some difficulty with creating the network visualizations. We tried using NetworkX and Plotly but there was a pretty steep learning curve when it came to the syntax involved. One issue we had was that the specific plotly module we were using required numerical values so we would have to assign values to the different melittidae interactions in our data. We were able to get some networks plotted but they were in no way presentable or useful. 

In R, we spent time cleaning data in a way that would be useful in coding various visualization methods. In particular, building ways to filter data by various genus, species, and family levels took a good amount of time. To accomplish this, and also to use the information to identify the unique interactions between interesting bees and various types of plants, we utilized the dplyr and tidyr quite a bit. Finally, using these data, we were able to assign occurrence quantities to these interactions, inspiring the use of ggplot and its heat map feature to give us more useful results. 

In meeting, we discussed ideas for various filtering methods and their respective uses, and also discussed future possibilities for use of such data.

![](https://github.com/mitchellrapaport/ucsb-ds-capstone-2021.github.io/blob/main/ucsb_ds_capstone_projects_2021/projects/ccber/Screen%20Shot%202021-01-30%20at%205.10.01%20PM.png?raw=true)

![](https://github.com/mitchellrapaport/ucsb-ds-capstone-2021.github.io/blob/main/ucsb_ds_capstone_projects_2021/projects/ccber/Screen%20Shot%202021-01-27%20at%202.16.23%20PM.png?raw=true)
