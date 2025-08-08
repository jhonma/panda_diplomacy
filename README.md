# panda_diplomacy  
The artilce is <a href="https://jhonma.github.io/panda_diplomacy/"># HERE</a>
The explanation is <a href="https://jhonma.github.io/panda_diplomacy/"># HERE</a>


## Short description of what I aimed to accomplish

As I wrote in the footer of the article, I chose the theme based on my intuition during class. It is widely known that China uses pandas as a diplomatic tool, and I was able to find many articles related to this topic. However, I could not find any detailed analysis at the individual level, so I thought I might be able to find a new angle.

## Short description of my findings

According to my data analysis, Japan has bred far more pandas than it borrowed from China and has exported them back to the country. This little-known fact may add an interesting twist to the story of Japan's continued tributary diplomacy toward China.


## Summary of the data collection process, with links

There are three zoos in Japan that have continuously kept pandas, excluding short-term stays. Each zoo has detailed descriptions of the individual pandas on their websites. For the analysis, I used the first blog listed below as the primary source material, scraped some of the tables using the pandas read_html method, exported it as a CSV file locally, and manually supplemented and verified the data in Excel while cross-referencing with the zoo's records as needed.

#### Main data sources

- Panda Tokidoki Manuruneco  
https://panda-manuruneko.com/panda-history-japan/  
A blog about pandas and manul cats by Japanese enthusiasts. Although it is a personal blog, we determined that the content is highly accurate after comparing it with zoo websites and other sources. The second long table, although incomplete, contained a significant amount of text describing loans and returns from China, making it suitable as a basis for data creation.

- Ueno Zoo  
https://www.ueno-panda.jp/history/  

- Adventure World  
https://www.aws-s.com/panda_breeding_and_research/history/individuals.html

- Kobe Oji Zoo  
https://www.kobe-ojizoo.jp/animal/panda/




## Overview of the data analysis process


The year of start of breeding and return (or death) for each zoo and individual were organized into a time series graph. Columns were created for the start and end of breeding, and two types of flags were set for each.

- Whether the panda was loaned from China / born in a Japanese zoo
- Whether it was returned to China / died in Japan

Based on the above data, a four-quadrant matrix was created. To make it easier to understand, the quadrants were color-coded and given intuitive titles. These elements were reflected in Graph 1 (case examples) and Graph 2 (series).

- PRACTICALLY GIFTED: rented from China, died in zoo
- RENTED & RETURNED: from/to China
- HOMEGROWN: born in a zoo, died in a zoo
- CONTRIBUTED: born in a zoo, transferred to China

## What new skills, approaches, etc I used, or where I grew the most during the project

Contrary to the name, the use of pandas was limited. This was due to the data requiring a lot of manual input and the fact that working in Excel was simply more efficient.

The most time-consuming tasks were data exploration, followed by DataWrapper and Adobe Illustrator. Becoming somewhat familiar with DataWrapper's operations was a notable achievement. While DataWrapper allows for quick visualization, it has limitations in terms of the number of data series and color expression capabilities. As a result, much of the post-production work had to be done in Adobe Illustrator.

To create Graph 1, four SVGs were output for each series (corresponding to each color pattern of the bars) and manually overlaid in Adobe Illustrator. Initially, that resulted in a simple PNG file, but in order to resolve blurring of text within the graph, I switched to compositing an image and text using AI2HTML. In the process, I needed to add support for mobile display (which was cumbersome). For graph2, I am simply loading the DataWrapper output into an iframe.


#### Tools I used (other than python)
- Microsoft Excel
- DataWrapper
- Adobe Illustrator
- AI2HTML 

## Things I tried to do or wanted to do but did not have the skills/time (but if you have more time you might do)

Initially, this analysis aimed to track the movement of pandas globally, including Japan. I attempted to obtain a list of panda locations or a list of captive animals issued by zoo industry associations or UN agencies, but after several attempts, I realized that it was difficult to obtain comprehensive data. Considering the submission deadline, I decided to focus on Japan, where relatively complete breeding data, including time series, is available.

While it is unclear how much this contributed to the acquisition of coding skills, I feel that the story is interesting and well-timed, and that some results were achieved. If time permits, I would like to continue the research with additional data, add map data, and add anecdotes about individual pandas to create a more human (or panda-ish?) story. For future reference, I will list the data sources that I initially attempted to use.


#### Data sources I considered for use: 

- Panda News  
https://pandanews.org/the-pandas.1.html  
Compiled by a U.K. enthusiast who have worked as a zookeeper in China, this source looks highly reliable and comprehensive. However, the latest update is from 2013. I tried scraping using the WGET command and Playwright, and was able to download the HTML. However, normalization using GREP and Regex remain as a significant burden.

- Wikipedia  
https://en.wikipedia.org/wiki/List_of_giant_pandas  
Focuses on well-known individuals, with low data comprehensiveness outside the United States. Source verification is necessary. Table scraping is relatively straightforward.
