![Banner logo](https://github.com/zackyndra23/Data_Science/blob/main/Banner1.jpg?raw=true)

# Insightful 3D Data Visualization with PyDeck (Indonesian Waste Piles in 2022): A Solution to the Limitations of Folium and Choropleth Flatmaps
*by Zaky Indra Satria Putra, student at* &nbsp;
<a href="https://purwadhika.com" target="_blank">
    <img src="https://github.com/zackyndra23/Data_Science/blob/main/Logo%20Purwadhika.png?raw=true" width="20%">
</a>

<br>

# Context

<br>

<div style="text-align:center;">
    <a href="https://medium.com/@putra.zakyindras/insightful-3d-data-visualization-with-pydeck-indonesian-waste-piles-in-2022-a-solution-to-the-19ba04c08451" target="_blank">
        <center><img src="https://github.com/zackyndra23/Insightful-3D-Data-Visualization-Exploratory-Analysis-With-Pydeck-in-Phyton/blob/main/(01)%20Visual%20Exploratory%20analysis%20with%20pydeck.png?raw=true" width="60%">
        <figcaption>Created by Zaky Indra Satria Putra on his article (click to explore) </figcaption> </center>
    </a>
</div>

<br>

The increasing complexity of datasets in **data science** needs sophisticated visualization tools. In response to this demand, various tools and libraries have been developed **to help data analysts present data in a more intuitive and informative way**. In this project, we will explore the domain of **3D visualization using PyDeck** in an application to **illustrate the number of waste piles in Indonesia during 2022**.

# Problem Determination

<br>

<div style="text-align:center;">
    <a href="https://www.kompas.id/baca/english/2023/06/27/en-mayoritas-sampah-di-indonesia-adalah-sampah-makanan" target="_blank">
        <center><img src="https://github.com/zackyndra23/Insightful-3D-Data-Visualization-Exploratory-Analysis-With-Pydeck-in-Phyton/blob/main/(02)%20Piles%20of%20Waste%20in%20Batargebang.jpg?raw=true" width="60%">
        <figcaption>Taken by Fakhri Fadlurrohman on his article (click to read) </figcaption> </center>
    </a>
</div>

<br>

Data visualization in three dimensions provides a richer and deeper perspective. However, in choosing a tool for the challenge, it's often difficult to decide whether a 3D approach is more effective than a traditional 2D approach. **What are the advantages and obstacles of each in understanding the number of waste piles spatial distribution of Indonesia in 2022?**

# Methodology

## Data Preparation & Data Wrangling to Prepare Data
* Defining the library
* Importing all .csv files that will be used for data analysis and visualization, then integrating the data into complete information
* Viewing all columns of the imported dataframe to understand the whole information
* Cleaning up the data in df3 so that it can be integrated with the main df. Then, information related to province_id can be unified
* Preparing the df4 dataframe in order to be integrated with the main df. Then, information related to regency_id, longitude, and latitude of regency can be unified
* Preparing the df2 dataframe in order to be integrated with the main df. Then, information related to the number of Micro, Small, and Medium Enterprises (UMKM) and the number of workers/labors related to landfill management, wastewater, food waste, waste recycling, and remediation can be unified.
* Creating a new dataframe for visualization based on the province

## 2D Visualisation Using Folium and Plotly Library
* Creating folium and choropleth maps to visualize the amount of waste production by each province per day
* Create a new dataframe for interactive visualization of choropleth map using Plotly .go
* When the dataframe has no missing values, and columns with integer and float data types are correct, then 3D Data Visualization using PyDeck can be started.
* Creating a folium map containing whole information related to the amount of waste per day, the number of UMK's, and the number of workers/laborers in 2022

## Visualizing 3D data using PyDeck
* [ColumnLayer](https://deckgl.readthedocs.io/en/latest/gallery/column_layer.html)
* [GridLayer](https://deckgl.readthedocs.io/en/latest/gallery/grid_layer.html)
* [HeatmapLayer](https://deckgl.readthedocs.io/en/latest/gallery/heatmap_layer.html)
* [ScatterplotLayer](https://deckgl.readthedocs.io/en/latest/gallery/scatterplot_layer.html)

# Discussion

## 2D Visualisation Using Folium and Plotly Library
<br>

<div style="text-align:center;">
    <center><img src="https://github.com/zackyndra23/Insightful-3D-Data-Visualization-Exploratory-Analysis-With-Pydeck-in-Phyton/blob/main/(03)%20Discussion%202D%20Visualization%2001.png?raw=true" width="60%">
        <figcaption>Folium Vs Plotly Library 2D Choropleth Map</figcaption> </center>
    </a>
</div>

<br>

Figure. 1. A is the result of a 2D choropleth map from the Folium Library while Fig. 1. B. is the result of the Plotly Library. The difference between those two
is **the level of interactivity**. Fig. 1. B, when the cursor is moved to the chosen province, it will show information on the number of waste piles per day in
tons and also the name of the province. Meanwhile, Figure before can only be interpreted using the color index so that **provincial interpretation errors can
occur**. Then, from the level of color difference, fig. 1.B is **more distinguishable** than Fig. 1.A.

<br>

<div style="text-align:center;">
    <center><img src="https://github.com/zackyndra23/Insightful-3D-Data-Visualization-Exploratory-Analysis-With-Pydeck-in-Phyton/blob/main/(04)%20Discussion%202D%20Visualization%2002.png?raw=true" width="60%">
        <figcaption>Regencies Detail Information Map Using Folium Library</figcaption> </center>
    </a>
</div>

<br>

In this fig, using the Folium Library is quite **interactive**, when we click on the icon for the selected regency, it shows information on 3 parameters (number
of waste piles, number UMK’s, and the number of workers/laborers). **Additional provincial and national percentage information data** can also be added and
displayed. In this visualization **we cannot find patterns** so it just provides the info from user configuration.

## Visualizing 3D data using PyDeck
* [ColumnLayer](https://deckgl.readthedocs.io/en/latest/gallery/column_layer.html)
<br>
<div style="text-align:center;">
    <center><img src="https://github.com/zackyndra23/Insightful-3D-Data-Visualization-Exploratory-Analysis-With-Pydeck-in-Phyton/blob/main/(05)%20Discussion%203D%20Visualization%2001.png?raw=true" width="60%">
        <figcaption>ColumnLayer Using PyDeck Library</figcaption> </center>
</div>
<br>

This layer helps users to understand **the comparison between numerical values in various locations**. For example, in Figure (3. A), we can use ColumnLayer to show the number of waste piles per day in tons in various regencies. Then this layer also provides **interactivity on the map**, allowing users to explore the data further by hovering over the bars. Regarding design, this layer also allows **visual adjustments** such as color, bar height, and other styles, so we can customize the appearance according to our needs and visual preferences.

Based on fig. (3. A), we can see the regencies with **the highest number of piles of waste**, such as **Jakarta Timur** Regency, **Tangerang**, **Bekasi**, **Jakarta Barat** and **Jakarta Selatan** Regency. On Kalimantan Island, **Samarinda** Regency in East Kalimantan Province is the area that produces the most piles of waste (587.25 tons/day). On Sumatra Island, the highest production is in **Medan** Regency in North Sumatra Province (1722.6 tons/day). On Sulawesi Island, the highest production is in **Bone** Regency, South Sulawesi Province (405.8 tons/day). And on Papua Island, the highest production is in **Jayapura** Regency in Papua Province (217.9 tons/day)

* [GridLayer](https://deckgl.readthedocs.io/en/latest/gallery/grid_layer.html)
<br>
<div style="text-align:center;">
    <center><img src="https://github.com/zackyndra23/Insightful-3D-Data-Visualization-Exploratory-Analysis-With-Pydeck-in-Phyton/blob/main/(06)%20Discussion%203D%20Visualization%2002.png?raw=true" width="60%">
        <figcaption>GridLayer Using PyDeck Library</figcaption> </center>
</div>
<br>

GridLayer shows **the data intensity** in various provinces. Each tile on the grid is represented by a specific numerical value, and the color of the grid will reflect that intensity level and help in **analyzing data distribution patterns across the map**. This gridlayer allows **visual adjustments** as well such as color, grid density, and other styles, so we can customize the appearance according to our visual needs and preferences.

Based on Figure (3. B), we can see the provinces with **the highest number of workers/laborers in managing waste, household waste, industry, food waste, water and remediation**, such as the **Jawa Barat** Province, **Jawa Timur**, **Jawa Tengah**, **DKI Jakarta**, **Banten**, **Sumatera Utara**, and **Riau** Province. On Kalimantan Island, **Kalimantan Selatan** Province is the area with the largest number of workers (2416 people from 11 regencies). On the island of Sumatra, the highest productivity is in **Sumatera Utara** Province (7675 people from 18 regencies). And on Sulawesi Island, the highest productivity is in **Sulawesi Selatan** Province (3791 people from 17 regencies).

* [HeatmapLayer](https://deckgl.readthedocs.io/en/latest/gallery/heatmap_layer.html)
<br>

<div style="text-align:center;">
    <center><img src="https://github.com/zackyndra23/Insightful-3D-Data-Visualization-Exploratory-Analysis-With-Pydeck-in-Phyton/blob/main/(07)%20Discussion%203D%20Visualization%2003.png?raw=true" width="60%">
        <figcaption>HeatmapLayer Using PyDeck Library</figcaption> </center>
</div>

<br>

Visualization of **the density or intensity of data** on a map can also be represented by HeatmapLayer. Each area on the map is colored to reflect the level of concern from the 'wasteperday' data in each regencies. It can be seen from Figure 3. C, on the island of Java, the reddest data (areas **with high levels of concern**) are in the **Jawa Barat** and **Jawa Timur** Provinces, then move to the east (**Jawa Tengah** to **Bali** Province). Meanwhile, on Sumatra Island, there are 4 points, they are **Medan** Regency in Sumatera Utara Province, **Pekanbaru** Regency in Riau Province, **Batam** Regency in Kepulauan Riau Province, and **Palembang** Regency in Sumatera Selatan Province. These are the areas that **require more regular handling and intensive treatment** by **increasing the number of workers/laborers and waste management sites/banks**, as well as **triggering local and national government for creating local regulations that regulate waste production** so that the environment in those areas is maintained.

* [ScatterplotLayer](https://deckgl.readthedocs.io/en/latest/gallery/scatterplot_layer.html)
<br>

<div style="text-align:center;">
    <center><img src="https://github.com/zackyndra23/Insightful-3D-Data-Visualization-Exploratory-Analysis-With-Pydeck-in-Phyton/blob/main/(08)%20Discussion%203D%20Visualization%2004.png?raw=true" width="60%">
        <figcaption>ScatterplotLayer Using PyDeck Library</figcaption> </center>
</div>

<br>

ScatterplotLayer helps in **understanding the spatial distribution patterns** of a collection of data points. This layer provides a **level of interactivity** that allows users to explore the data further by hovering the cursor or performing other interactions on the map.

Based on figure (3.D), we can see the provinces with **the highest number of UMK’s**, such as **Jawa Barat** Province (21648 UMK’s), **Jawa Timur** (17080), **Jawa Tengah** (14176), **DKI Jakarta** (7864) and **Sumatera Utara** (4448). On Kalimantan Island, **Kalimantan Selatan** Province is the area the highest number of UMK’s **related to the management of industrial, water, household waste, food waste and remediation** (1490). On Sumatra Island, the highest number is in **Sumatera Utara** Province (4448). And on Sulawesi Island, the highest number is in **Sulawesi Selatan** Province (1823).

### Weak points and advantages of using Pydeck in 3D data visualization

#### Advantages:
* **Captivating 3D Visualization**
<br>PyDeck provides the advantage of more engaging and detailed 3D data visualization. This allows users to more deeply understand the spatial distribution of waste.
* **Enhanced Interactivity**
<br>PyDeck allows for better interactivity, allowing users to explore data and gain further insights through the use of features such as tooltips.
* **Flexible Map Configurations**
<br>With PyDeck, users have greater control over the appearance of the map and can easily set visual properties such as color, size, and height.

#### Weak Points:
* **Likely Requiring Advanced Coding Skills**
<br>PyDeck, as a powerful Python library, may require a higher level of coding expertise compared to simpler visualization tools like Folium.
* **Limitations on Some Use Cases**
<br>In some use cases, especially for simple presentation purposes or basic mapping, 2D approaches such as Folium may be effective enough without requiring the complexity of 3D visualization.

#### Brief Insights:
Through the use of PyDeck, analysis of the spatial distribution of waste in Indonesia can be carried out in more depth. The resulting 3D visualization **provides a richer and more contextual understanding of waste patterns and density**, which can be the basis for more effective decision-making in waste management in the future. While PyDeck has its complexities, the advantages it provides in spatial **understanding can be the key to more targeted and sustainable solutions**.


# Conclusion and Recommendation

Through this 3D data explorations, the article aims **to provide detailed insight into how visualization technologies such as PyDeck can help understand the spatial distribution of Indonesia waste piles in 2022**. By comparing with 2D approaches such as Folium and Choropleth maps, users will gain a **better understanding of the advantages and limitations of each approach in the context of increasingly complex waste management problems in Indonesia**.

### Recommendation
* Using 3D visualization by PyDeck, we can present **routes or locations of waste storage areas in a more informative and interesting way**. For example, we can use scatterplots to show the locations of waste storage areas and depict routes between locations.
* Using spatial data, we can visualize the route or location of waste banks in 3D. This can **help the community or related organizations in planning waste collection routes or designing waste management programs** by indicating the strategic location of waste banks.
* Leverage visualization to **increase stakeholder engagement**. This can be done by providing an **interactive platform or including features such as tooltips to provide additional information** about the data displayed.
* We can **recommend effective programs by identifying areas with the highest levels of waste production but whose human and organizational resources are still not sufficient to reach the goals** of sustainable development and good environmental management.

# References

[1] [https://www.kaggle.com/discussions/general/331623](https://www.kaggle.com/discussions/general/331623)

[2] [https://deckgl.readthedocs.io/](https://deckgl.readthedocs.io/)

[3] [https://github.com/UnfoldedInc/pydeck](https://github.com/UnfoldedInc/pydeck)
