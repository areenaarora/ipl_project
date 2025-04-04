# IPL data visualized in D3.js

### [Link to the final project](https://areenaarora.com/the-hindu/ipl)

The project was to create a chart showing top IPL performers across three categories - batting, bowling and overall scores, inspired by FiveThirtyEight's
visual on the best NBA players.
[Web archive link here.](https://web.archive.org/web/20241219203335/https://projects.fivethirtyeight.com/2020-nba-player-ratings/)

The focus was on ensuring smooth working and responsiveness and of course, styling.

## Data source:

Two CSVs (both provided)

1. [IPL data with bowling, batting and overall scores](https://github.com/areenaarora/ipl_project/blob/main/IPL_data.csv)
2. [IPL salaries data](https://github.com/areenaarora/ipl_project/blob/main/scatter_plot/IPL_salaries.csv)
3. [Merged csv with both salaries and performance data](https://github.com/areenaarora/ipl_project/blob/main/scatter_plot/merged_sal.csv)

## Process and challenges

- The visuals with D3 were straightforward with one major challenge - merging salaries data to performance data. Both CSVs had several inconsistencies and instances of missing data. In my first attempt, I merged the two (using Python) on just name, but realized quickly I should use both season and name data to accurately match unique rows since multiple players played multiple seasons and for different teams.

- Once the merging was handled, I tested the data to see how it behaves on the scatterplot and did some spot checks to ensure accuracy.

- The next challenge was ensuring attention was paid to small details - that the dropdowns worked correctly and filters were being applied seamlessly.

- Important to note - in the first chart (the bubble chart), some data points are too close to each other and there was no better way to label them but to produce a dynamincally changing list on the right. This ensures the user can easily consume the information, as intended.

- Another challenge in replicating the FiveThirtyEight graphic was making players' headshots appear on the bubble chart. However, my dataset had 257 unique players, making it extremely difficult to find, edit and use their headshots. That would also have made the project heavier and slower.

- For the second chart (scatter plot), it was important to provide a summary to the reader - what story is the chart ultimately trying to convey? To do this, a sentence was added which dynamically updates and shows the reader how many players were paid above or below average in comparison to their performance. This chart too, is interactive and each dot reveals the player's name, team, salary and performance score.

- Finally, the searchable database puts it all together. This table too is interactive and can be used to look up data on specific players, in specific years and for specific teams.

## Links to individual charts' code

1. [Bubble chart](https://github.com/areenaarora/ipl_project/blob/main/index.html)
2. [Scatter plot](https://github.com/areenaarora/ipl_project/blob/main/scatter_plot/index.html)
3. [Searchable table](https://github.com/areenaarora/ipl_project/blob/main/searchable_table/index.html)
