# kickstarter-analysis

# Kickstarting with Excel

## Overview of Project 
Louise's play called Fever came close to its fundraising goal in a short period of time. She wants to see and compare  how well the other plays faired in relation to their launch date and goals. 

### Purpose
The purpose of this project is to analyze all the data from the "Kickstarter" datasheet,  extract meaningful data and visualize the data in a graph. The graph should show a clearer picture of the trends. The data that I will be focusing on is from the "plays" subcategory.

## Analysis and Challenges
Using the dataset, I exctracted data that was used to create two line graphs, using the data from the plays subcategory. Two line graphs were created; one plotting the outcomes against the launch date, while the second graph plotted the percentage outcome against the goal amount

### Analysis of Outcomes Based on Launch Date
For the first analysis, I created a new column called Years. This column contained the years from the date_created_conversion column. Using my entire dataset, a pivot table was created. In the rows field, the dates were added by month. In the column field, the outcomes were added. Two filters were also added; the "years" column and the parent_category column. After the pivot table was created, the filter was applied to only include the theatre subcategory (this is the data we are trying to analyze). The outcomes column was modified in descending order, with the "live" outcome being excluded. Once all filters were applied, a line graph was created to display the outcomes based on Launch date. https://github.com/somtoesomeju/kickstarter-analysis/blob/main/Outcomes_vs_goals.png
### Analysis of Outcomes Based on Goals
For the second analysis, a new sheet was created to include different parameters for rows and columns. The rows included a range of values for the campaign goal amounts. The column included the outcomes; both in numerical form and percentage. In order to get the outcome values, the COUNTIF function was used. For the first cell (B2) in order to get the value, the COUNTIF function was filtered with the range, the sub_category of plays and the amount of times the campaign was successful. Since the range is different in every row, indivdual formulas were created for each cell. After getting the value of all outcomes, the total was added using the SUM function. In order to get percentages, the outcome was divided by the total value to get a fraction. The format was changed from General to Percentage to give the range in percentages.  The resulting table was converted into a line graph, with the percentage of the outcomes plotted against the goal amounts. 
![outcomes_vs_goals](path/to/outcomes_vs_goals.png)

### Challenges and Difficulties Encountered
So far I did not encounter any error when I used the proper commands to excecute the function. Initially, I had an error due to the fact that I used the wrong column (pledged instead of goals). It led to an error when calculating the results as one of my values could not be divided to make a percentage. A common error can be caused by using the wrong command to run the script. The COUNTIF and COUNTIFS functions are similar words with different commands. Initially I used COUNTIF which led to an error. Once corrected to COUNTIFS, the error was corrected as well.

## Results

- Conclusions from the launch date
From the outcomes based on launch date, the two things that can be concluded from the graph is that the most successful theatre campaigns happened in the summer months (June and July) and the least successful campaigns happened in the winter. There is a positive association between the time of the year and how sucessful the campaign is. In the winter months (December and January), the outcomes are almost the same. This concludes that campaigns launched in the summer are the most successful, while the ones launched in the winter are more likely to fail.

- Conclusion of the outcomes based on goals
From the line chart, there is a trend between the amount of the goal and its success rate. The lower the goal amount of the play, the more likely it is to succeed. 

- Limitations
One of the main limitations with the dataset is from the "canceled" column in "Outcomes Based on Goals" analysis. I did not get any numbers in the canceled column as there are no cancelled plays. If there was data for canceled plays it would have deepened the analysis and might have given a better idea of the trends. 

- Alternative tables/graphs for analysis. In addition to the line graph, a stacked bar chart![outcomes_vs_launch_stackedbar](path/to/outcomes_vs_launch_stackedbarpng) could be created for the outcomes against the launch date. The stacked bar would better visualize the trend as opposed to the line graph. It is easier to see that the campaigns are most successful during the summer months. 
