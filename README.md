## Analysis Of The Covid-19 Pandemic’s Impact On Montreal’s Bike Sharing Network, BIXI
A Study on montreal’s bike sharing network, BIXI, and how the Covid-19 pandemic pandemic impacted the network.
Networkx graph creation, Use of centrality measures and community detection algorithms, Map visualizations, Litterature review.
<br> [Study in Progress: Code has to be cleaned and converted to a proper .py format]
<br> The paper is currently in peer review for the MSURJ journal. A copy can be found in the main folder.

### Abstract:

Montreal, with its booming growth, is a great demonstration of the urban mobility challenge: with congestion, construction, parking difficulties, weather and environmental conditions to cite a few. To support circumvent- ing this challenge, BIXI, the first large-scale bike sharing network in North America at the time, was launched in May 2009. With over 5 million annual rides, it has been without doubt contributing positively to the city’s development. However, with its increasing adoption, the network has become frustrating to use, with sta- tions often being empty when you need a bike, or full when you need to return one at peak usage times. Through this project, we explore the tens of thousands of BIXI daily bikes trips to extract environmental and socio-economic insights, better understand the habits of Montrealers and understand how this phenomenon occurs. In addition, we analyse how the pandemic impacted these habits and the BIXI network. To do so, we use degree, betweenness and eigenvector centrality measures as well as Louvain and Fast Modularity community detection algorithms. By comparing our results from the 2019, 2020 and 2021 generated graphs, we are able to observe how the BIXI network shifted from being used mainly during commuting hours between residential and business districts pre-pandemic, to being more spread throughout the day and within each neighbourhood during the pandemic.


### Experiment set-up and achievements
- Obtaining the raw datasets
  - BIXI trips from BIXI open data
  - Weather data from the Government of Canada
  - Metro stations from the STM

- Cleaning and preparing of the raw datasets
  - Converting csv files to python panda dataframes for manipulation
  - Renaming, re-ordering, casting data types and formats for consistency and ease of use
  - Filtering datasets
    - BIXI - Filtering out trips related to missing stations and self-loops
    - Weather - Filtering out unneeded weather data, keeping only temperature and precipitation data; writing 0 when no data
    - STM - Filtering out bus stations, keeping only metro stations
  - Concatenating time frames by time and date (hours, day of the week, years)


- Creating networkx simple directed weighted graph (SDG) from processed panda dataframes


- Computing network features
  - Calculating centrality measures on SDG
    - Degree centrality, including net-in-out-degree
    - Eigenvector centrality
    - Betweenness centrality
  - Computing communities
    - Fast modularity
    - Louvain


- Creating visualisations of network features
  - Creating plots from panda dataframes
    - Daily number of BIXI trips over years line plot
    - Number of BIXI trips vs Temperature histogram
    - Number of BIXI trips Day of the week vs Hour of the day heat-map
  - Overlaying network features on top of a map of Montreal using Kepler.gl (code will be posted on Githib before March 2022)
    - => Interactive maps can be viewed at https://rebrand.ly/BIXI-study-web (note: it doesn’t work with Safari).
    - Net-Degree, Eigenvector, and Betweenness Centrality measure heat-maps
    - Net-Degree, Eigenvector, and Betweenness Centrality measure point-maps
    - In-Out-Degree Centrality dynamic point-maps
    - Fast modularity and Louvain community point-maps

- Paper write-up
  - Litterature review
  - Writing & Editing
  - Submitting for publishing
    - Currently in the peer review phase of the MSURJ journal

---
### To-do
- Code cleaning
  - The code works on our end, but has to be cleaned
- Conversion to .py format instead of a .ipynb python notebook format
- More visualisations?
