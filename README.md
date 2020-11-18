# Comparing Household Income in Baltimore, MD and Wilton, CT

This project serves to compare household income in two cities, Baltimore, MD, and my hometown, Wilton, CT. Although these areas are only about a 5 hour drive apart, having lived in both places for some time, I noticed that they are incredibly different. Household income is explored as a diffrentiator between these two cities.

According to [research](https://pubmed.ncbi.nlm.nih.gov/20201871/), household income and socioeconomic status (SES) affects the economic environment, which determines the robustness of the area's business and economy. More affluent areass have more robust businesses and economy. It would be helpful to understand what contributes to a socioeconomic status of an area, so parents socioeconomic status is explored as a possible contributor to child's household income. 

# Business Question
Which city supports a more robust business economy? How might parents' SES affect this?

# Data Question
How can parents' SES affect child's household income? 
How do household incomes in Baltimore, MD and Wilton, CT compare?

# Data Sources
**Opportunity Insights**: this is a research group that identifies and attempts to dissolve barriers to social mobility to help those living in poverty. The team developed [Opportunity Atlas](https://www.opportunityatlas.org), which uses childhood to mid-30's data from 20 million people to rate areas based on their social mobility.
This publically accessible data was used in this analysis.
1. Data showing household income in Baltimore, MD and Wilton, CT (data Baltimore - general & data Wilton - general)
2. Data showing household income given parents' income is in the top 25% (data Baltimore - high & data Wilton - high)
3. Data showing household income given parents' income is in the middle (data Baltimore - middle & data Wilton - middle)
4. Data showing household income given parents' income is in the bottom 25% (data Baltimore - low & data Wilton - low)

# Data Answer
![alt text](https://github.com/achow6/comparing-baltimore-wilton-household-income/blob/master/Picture1.png)
This is a visual generated from Excel from Mini-Project 1. Here we can see a large difference between overall average income in both cities. There is a $48,440 difference in average household income.

![alt text](https://github.com/achow6/comparing-baltimore-wilton-household-income/blob/master/Picture2.png)
This is a visual generated from Excel from Mini-Project 1. Here we see that the large difference between average income persists even when looking at children that came from high income and low income families. In both cities, average household income is lower for those that came from low income families compared to high income ones. It is also interesting to see that the average overall household income in Wilton exceeds the average income of a child from high income Wilton parents.

![alt text](https://github.com/achow6/comparing-Baltimore-Wilton-household-income-python/blob/main/Python%20Plotly.png)
This is a visual generated from Python for this project. Here, we still see that there is a large difference in child's household income depending on which income bracket the child grew up in. In both cities, average household income is lowest for children that came from low income families, higher for children that came from middle income families, and highest for children that came from high income families. The average overall household income in Wilton still exceeds the average income of a child from any income parents in Wilton.

# Business Answer
This data suggests that Wilton, CT generally has higher household income compared to Baltimore, MD in all parent SES brackets. The data also suggest that parents' SES is associated with child's household income. 

The middle income dataset was included in the Python analysis to try to determine why overall household income in Wilton exceeds the average income of a child from a high income Wilton family. However, as the Plotly visual shows, the average overall household income in Wilton still exceeds the average income of a child from any income family in Wilton. This suggests that there could be extremely high-earning individuals in Wilton who are pulling the average overall household income up.

The aforementioned research that found that socioeconomic status influences the robustness of a cities' businesses and economy. Therefore, this data suggests that Wilton could have a more robust business structure and economy than Baltimore because Wilton shows a higher household income across all categories than Baltimore.

To further explore the difference in income, data on children's type/length of employment and education level might be helpful. It would also be helpful to include data on the city's economies and businesses (ex. turnover rate, revenue).

# Comparing Python and Excel Analysis
Python presented a much easier method to import, filter, and merge data. Instead of having to open each individual dataset over and over again and selecting specific columns to conduct merging techniques like VLOOKUP, Python allowed me to easily merge the datasets on one screen. Additionally, instead of having to split the cells to include all of the Baltimore, MD rows like I had to in Mini-Project 1, Python could filter the dataset to every cell containing "Baltimore, MD" in the column, which made the filtering process much faster. Python also made calculating averages much easier because instead of calculating averages for each column, Python could calculate averages for every column in the dataset with one command.

One disadvantage I came across with Python was that it assumed my values were objects, and therefore, was not able to calculate the average for each column at first. I had to convert them to floats to get the average. This is a problem I would not have encountered in Excel. I felt that creating visuals for this project was also slightly more difficult in Python. In Excel, I would press the bargraph button, and Excel would automatically generate a visual for me, but for Python, I had to code what I specifically wanted.

# Step-by-Step Data Analysis
[Google Collaboratory Link](https://colab.research.google.com/drive/1-z4Yh4Y-B9VY4IdPbwFNTN5lr4u97uyc?usp=sharing)
**Python Data Analysis:**
1. Libraries were imported (Plotly, Pandas, Numpy)
2. Data were imported and previewed
3. Data were filtered to rows containing "Baltimore, MD" and "Wilton, CT" in the "Name" columns of each dataset
4. Data were merged into one dataframe for Baltimore and one dataframe for Wilton on the "Name" and "tract" columns
5. Removed cells containing "void" in Baltimore dataframe
6. Object columns in the Baltimore dataframe were converted into floats
7. Averages for each column were calculated in each dataframe to determine average child's household income in each parent income bracket
8. Bar graph visual was created using Plotly

**Original Excel Analysis:**
Once the original data was downloaded, the location column (containing neighborhood, city, and state) was split into three separate columns for each (neighborhood, city, state). Cities outside of the scope were then filtered out. The VLOOKUP tool was then used to combine the datasets based on their "tract" number. The datasets from both cities were also combined to create a more cohesive analysis (both datasets shared the same column names and units of measurement). The data were analyzed through pivot charts and tables for numeric and visual results.
