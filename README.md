# A.2. Bias in Data

## Goal:
The goal of this assignment is to collect, curate, and analyze data on articles of politicians for many countries, then explore the biases that can be present in this analysis. We will collect article data from Wikipedia as well as population data from the Population Reference Bureau. We want to understand the coverage of politicians for different countries on Wikipedia as well as the quality of article for the politician. It is important to then discuss the biases that can pop within this analysis to better understand moving forward what we can do to alleviate and account for these biases.

## Data Sources:
*   Politicians by Country Dataset: https://figshare.com/articles/Untitled_Item/5513449
*   World Population Data Sheet: https://docs.google.com/spreadsheets/d/1CFJO2zna2No5KqNm9rPK5PCACoXKzb-nycJFhV689Iw/edit?usp=sharing
*   
## Data Descriptions:
### wp_wpds_politicians_by_country.csv:
Country - the name of the country of article origin, str
Article Name - the name of the article of the politician, str
Revision ID - the key that connects politician country dataset and world population data set, str
Article Quality Estimated - the estimated quality of the article, predicted by ORES, str
Population - the population of the country, int
Sub-Region - the name of the Sub-Region that the country is found in, str
### wp_wpds_countries-no_match.csv:
Country - the name of the country of article origin, str
Article Name - the name of the article of the politician, str
Revision ID - the key that connects politician country dataset and world population data set, str
Article Quality Estimated - these articles could not have their quality predicted so -1 was used as a placeholder to log these articles, int
Population - the population of the country, int
Sub-Region - the name of the Sub-Region that the country is found in, str
### Some other fields that can be found in the tables below:
percentage - proportion of articles per selected country population, int, (Number of Articles/Country Population) * 100
Percentage of Quality Articles - proportion of high quality articles per total number of articles for each country, int, (Number of High Quality Articles/Total Number of Articles) * 100

## Notes:
When booting up notebook, you'll have to uncomment to reinstall ores locally. You'll have to do this each time you reboot the notebook. It is then recommended to rerun the cell with the installation code commented out.
Most of the names from World Population Data Sheet that are of type = 'sub-region' (or can be identified by all caps) do not have a revision-id that will allow a match with politician by country dataset. These were excluded from our initial cleaning and analysis, and then brought back in to find regional metrics related to percentage and proportion.

## Charts:
### Top 10 countries by coverage: 10 highest-ranked countries in terms of number of politician articles as a proportion of country population
https://colab.research.google.com/drive/1uoPw5-ut70QY5BrvpKbiHlLP2gOpf6lb#scrollTo=IS-VQPFXh0ls&line=2&uniqifier=1

### Bottom 10 countries by coverage: 10 lowest-ranked countries in terms of number of politician articles as a proportion of country population
https://colab.research.google.com/drive/1uoPw5-ut70QY5BrvpKbiHlLP2gOpf6lb#scrollTo=R-Gnr8VGh0pn&line=2&uniqifier=1

### Top 10 countries by relative quality: 10 highest-ranked countries in terms of the relative proportion of politician articles that are of GA and FA-quality
https://colab.research.google.com/drive/1uoPw5-ut70QY5BrvpKbiHlLP2gOpf6lb#scrollTo=Axjv3KkLh0su&line=2&uniqifier=1

### Bottom 10 countries by relative quality: 10 lowest-ranked countries in terms of the relative proportion of politician articles that are of GA and FA-quality
https://colab.research.google.com/drive/1uoPw5-ut70QY5BrvpKbiHlLP2gOpf6lb#scrollTo=ENJ_9CpQh0v8&line=2&uniqifier=1

### Geographic regions by coverage: Ranking of geographic regions (in descending order) in terms of the total count of politician articles from countries in each region as a proportion of total regional population
https://colab.research.google.com/drive/1uoPw5-ut70QY5BrvpKbiHlLP2gOpf6lb#scrollTo=ld8cwmKTsT0u&line=2&uniqifier=1

### Geographic regions by coverage: Ranking of geographic regions (in descending order) in terms of the relative proportion of politician articles from countries in each region that are of GA and FA-quality
https://colab.research.google.com/drive/1uoPw5-ut70QY5BrvpKbiHlLP2gOpf6lb#scrollTo=AunaktxxwXE7&line=2&uniqifier=1

## Reflection:
I learned a lot form this short project, accomplishing many tasks such as data sanization, using ORES, and analyzing metrics about a country's political articles on Wikipedia.
## Questions:
### What biases did you expect to find in the data (before you started working with it), and why?
I expected there to be a bias toward English speaking countries and the quality of articles they produce. I imagined that countries where English was the native lanuage would produce more articles of politicians as well as high quality articles because we are working with data from English Wikipedia.
### What (potential) sources of bias did you discover in the course of your data processing and analysis?
Some sources of bias that I discovered in the course of data processing and analysis included assuming that the number of politicians per population were linearly related as well as the number of quality articles per total number of articles were linearly related as well. To compare number of politican articles to the population of a country may be misguided because articles of historical political figures are included as well as current political figures. As previously mentioned, number of politicans vs population would not be linearly related because the number of politicians is dependent upon how far back chronologically they include people, the way a country is sectored or split up (such as number of districts, etc.), the way a government is (parlimentarian, democratic, totalitarian, etc.), and not just population size. With this in mind, while it is interesting to note the ratio of politican articles to the population, I do not know how effective it is as a metric. On top of this, we are looking at English Wikipedia which is bound to have a certain slant on different politicians even if there is an appropriate rating system in place. Allegedly, North Korea has a high amount of quality articles, but those articles could say something much different than what can be said in Korean Wikipedia. Which one more accurately reflects the reality of the politician? For reference, Kim Jong Un is rated as a B-quality article and would not be included in the high quality article assessment.
### What might your results suggest about (English) Wikipedia as a data source?
For the particular subject of politicians, English Wikipedia can be a treacherous data source to navigate if you are looking for high quality information. The highest percentage of quality articles versus total number of articles was around 20% from North Korea, which in my opinion, is a low percntage if quality articles to have in politics. The United States in particular only has 80 quality articles about politicians out of 1068. Some of those high quality articles include Barack Obama, Ronald Regan, and George Washington (albeit he is good as compared to featured). Abraham Lincoln was a featured article but dropped to good article quality. I could not find the article quality of Donald Trump. Based on this very limited research, I assume that current politicians, those with high amounts of controversy, are politicians in history are harder to accurately reflect in high quality articles. For surface level information and summaries, Wikipedia is a great place to go to in general, but for deeper understanding and thorough research, it would be best to go to the scholarly articles that are linked in the references.
