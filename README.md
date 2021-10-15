# A.2. Bias in Data
## Goal:
The goal of this assignment is to collect, curate, and analyze data on articles of politicians for many countries, then explore the biases that can be present in this analysis. We will collect article data from Wikipedia as well as population data from the Population Reference Bureau. We want to understand the coverage of politicians for different countries on Wikipedia as well as the quality of article for the politician. It is important to then discuss the biases that can pop within this analysis to better understand moving forward what we can do to alleviate and account for these biases.
## Data Sources:
*   Politicians by Country Dataset: https://figshare.com/articles/Untitled_Item/5513449
*   World Population Data Sheet: https://docs.google.com/spreadsheets/d/1CFJO2zna2No5KqNm9rPK5PCACoXKzb-nycJFhV689Iw/edit?usp=sharing
## Data Descriptions:
### wp_wpds_politicians_by_country.csv:
Country - the name of the country of article origin, str
Article Name - the name of the article of the politician, str
Revision ID - the key that connects politician country dataset and world population data set, str
Article Quality Estimated - the estimated quality of the article, predicted by ORES, str
Population - the population of the country, int
### wp_wpds_countries-no_match.csv:
Country - the name of the country of article origin, str
Article Name - the name of the article of the politician, str
Revision ID - the key that connects politician country dataset and world population data set, str
Article Quality Estimated - these articles could not have their quality predicted so -1 was used as a placeholder to log these articles, int
Population - the population of the country, int
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
### Top 10 countries by relative quality: 10 highest-ranked countries in terms of the relative proportion of politician articles that are of GA and FA-quality
### Bottom 10 countries by relative quality: 10 lowest-ranked countries in terms of the relative proportion of politician articles that are of GA and FA-quality
### Geographic regions by coverage: Ranking of geographic regions (in descending order) in terms of the total count of politician articles from countries in each region as a proportion of total regional population
### Geographic regions by coverage: Ranking of geographic regions (in descending order) in terms of the relative proportion of politician articles from countries in each region that are of GA and FA-quality
## Reflection:
## Questions:
### What biases did you expect to find in the data (before you started working with it), and why?
### What (potential) sources of bias did you discover in the course of your data processing and analysis?
### What might your results suggest about (English) Wikipedia as a data source?
### What might your results suggest about the internet and global society in general?
### Can you think of a realistic data science research situation where using these data (to train a model, perform a hypothesis-driven research, or make business decisions) might create biased or misleading results, due to the inherent gaps and limitations of the data?
### Can you think of a realistic data science research situation where using these data (to train a model, perform a hypothesis-driven research, or make business decisions) might still be appropriate and useful, despite its inherent limitations and biases?
### How might a researcher supplement or transform this dataset to potentially correct for the limitations/biases you observed?
