 Data Mining from the News and building a Network Analysis

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Introduction:

We live in an age of media and information, where the importance of understanding the intricacies
of the News cannot be overstated. Building graph representations (i.e. social networks) of data
opens up a whole host of possibilities for data science applications, such as finding the most influential
individuals on the news or identifying clusters (cliques of people) based on connections.
How The sprawling web of politicians, companies look like, using Graph theory and analysing
the network representing this vast web of information through news channels.
The fundamental premise behind building our network will be two-fold and quite simple:

1. If two people are mentioned in the same article, they have co-mention relation.
2. The more articles mention the same two people, the closer they have co-mention relation.

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

README CONTENTS

1.1 Introduction
1.2 Description
1.3 Challenges Faced
1.4 Conclusion/Future Work
1.5 Acknowledgements

2.0 Data Mining from the News and building a Network Analysis_Data Preprocessing.ipynb
2.1 Data Mining from the News and building a Network Analysis_Data Visulaization.ipynb
2.2 CSV Files

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

1.2 Description

The source we used was from the GDELT Project, which is a free, open platform of all world events, monitored in real time from across the globe.
The GDELT Project monitors the world’s broadcast, print, and web news from nearly every corner of every country in over 100 languages.

We have fetched their raw data, which they also make available completely free of charge. 
They publish daily CSVs with thousands of events which occurred during that day, but more importantly, they include the URL of the news source which reported on the event.

We have used the file containing the events that had ocurred on the 23rd of April and extracted the top 800 articles around the globe. 
We had limited the search in a way to narrow down the volume of entities.

The type of raw data we got contained the sources, source urls with the date it was published on and other fields like Tone, Organization etc. 

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

1.3 Challenges Faced and Overcomed

In the initial stages of our project, we had several options to consider for data mining The type of raw data we got contained the sources, source urls with the date it was
published on and other fields like Tone, Organization etc. But according to our requirement, we needed to extract the content from each source urls to get the content of the news.

We have used Named Entity Recognition task for extracting information from text which recognises entities. This is achieved using statistical models trained
on our large dataset, where we make the model learn to recognise and categorise entities based on the context in which they appear in words. 
We will then be using one of these models for the words tagged as persons, organisations for each article.
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

1.4 Conclusion/Future Work

Further attributes can be included in order to enrich the data set which helps in better evaluating and analyzing at the later stage.
Along with additional attributes, additional instances of data can also be added by expanding the scope to other companies.

In other words, can we identify cliques in our network.

                  "Cliques are a set of nodes in a graph in which every pair of nodes is connected."
The algorithm we’ll use to do this is called k-clique communities , which allows us to find closely connected clusters in the network by defining k, 
or the minimum number of nodes required for a clique to be formed. 
There could be a case when one node can be very popular and belong to multiple cliques.
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

1.5 Acknowledgements

All the work done was referenced with the help of the article: 
1. https://towardsdatascience.com/building-a-social-network-from-the-news-using-graph-theory-by-marcell-ferencz-9155d314e77f
2. http://cs.brown.edu/people/rtamassi/gdhandbook/chapters/force-directed.pdf
3. https://towardsdatascience.com/k-means-clustering-algorithm-applications-evaluation-methods-and-drawbacks-aa03e644b48a

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

2.0 Data Mining from the News and building a Network Analysis_Data Preprocessing.ipynb

This is the jupyter notebook where we have all our code along with the description of the pre-processing of the data.

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

2.1 Data Mining from the News and building a Network Analysis_Data Visulaization.ipynb

This is the jupyter notebook where we have all our code along with the description of the visualization of the data.

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
2.1 CSV Files

We have collected over 800 articles from the News.

800Articles.csv

url				- Describes the source url from which the news article has been collected.

title				- Headline of the news

meta_description		- Gives a high level description about the news article

domain				- Gives the domain details of the news article i.e. to which news channel it belongs to and their domain.

content				- describes the news in detail.


df_links.csv

from				- Words generated

to				- To the words it is mapping

weight				- weights assigned to the edges


df_ner.csv

entity 				- This contains the words that has been collected.

type 				- This gives the details whether the details collected are persons or an organisation.

entity_cl 			- This gives the details about what class does the entity belong too.

date 				- Date of the entity created

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

<end of file>



