# Data_115 FDA Recalled Food Analysis
Data 115 personal dataset project

## Motivation
This semester, outside of DATA 115, I am also taking a class on the fundamentals of cooking. We frequently talk about foodborne illnesses. This topic motivated me to begin looking into related datasets. I didn’t need to look very far to find the list of all food and drug recalls made by the FDA over the past few years. I wanted to find out what types of categorizations and generalizations could be made to recalled foods. Some of my initial questions included: “What are the most common reasons for food recalls?”, “What are the most common categories of recalled foods?” and “Are certain recall reasons associated with certain categories of recalled foods?”. 

## Data Source
I obtained the Data from the U.S. Food and Drug Administration website. They have posted a description of all the recalled food and drug items in the US between 2017-2020. It is an open data source with over a thousand entries. I removed all of the entries related to drugs, cosmetics, medical devices, etc. by narrowing the Type column to Food.

## Processing Steps
There were a significant number of cleaning steps I needed to take in order to work with the dataset. I took what I considered the minimal number of steps needed in order to feel confident in my conclusions. If I wanted do additional analysis or ask additional questions, other cleaning steps would need to be taken. In my analysis I am able to point out correlations and make generalizations, but there are so many string processing errors it is difficult to make specific statements without checking a multitude of individual entries. To access my step-by-step processing and analysis, see the Personal Dataset Project.rmd file. 

## Visualizations

### Most Common Reasoning for Recalls
<img src="https://raw.githubusercontent.com/hannahpeha/Data_115/main/Figures/recall.reasons.png">
All of the columns in the dataset are categorical. I chose to focus my initial analysis on patterns related to the most commonly recalled foods. This bar chart shows the most common reason foods were recalled in the United States from 2017-2020. As seen in the chart, the most common reason a food was recalled was for "Undeclared Milk". An "undeclared" designation means a product did not list the presence of a major food allergen on the finished packaging. The next most common reasons were listeria and potential listeria contamination. Listeria is a food-borne bacterial illness. It is commonly found in unpasteurized milk products and improperly handled deli meats.

### Attention Grabbing Recall Reasons
<img src="https://raw.githubusercontent.com/hannahpeha/Data_115/main/Figures/Attention%20Grabbing.png">
I printed out the full list of unique reasons for recalls. Some of the ones which caught my attention I included in the table above. There were a couple of interesting patterns which I haven't included here but can be seen with pivot tables. For example, lead related recalls seemed to be associated with spices, and Foreign Object recalls, espically those involving metal, seemed to be associated with ice cream products. Further research could be carried out to determine why these patterns appear. 

### Most Commonly Recalled Food Types
<img src="https://raw.githubusercontent.com/hannahpeha/Data_115/main/Figures/foodsub.plot.png">
I then applied the exact same process to find the most commonly recalled categories of food. Snack Food items and Prepared Foods were by far the most common occurances. These categoeries are obviously very broad containing most processed convience foods. I was surprised that meats such as beef and pork did not make this list. 

### Most Commonly Recalled Brands
<img src="https://raw.githubusercontent.com/hannahpeha/Data_115/main/Figures/Brand%20Name.png">
Most of the brands are only listed in the data set once. However, there are a few which are repeat offenders. With the exception of Murray Jarlsberg, a cheese company, all of the others are brands belonging to their associated supermarket chain. These Supermarkets tend to be higher end, Whole Foods Market as the hallmark example, with a focus on organic and 'natural' food products. 

## Analysis

### Common Associations Between Food Category and Recall Reason
<img src="https://raw.githubusercontent.com/hannahpeha/Data_115/main/Figures/Contingency.png">
This simplified contingency table shows the most common associations between recall reason and food group category. For example undeclared milk is frequently associated with processed convenience foods including: bakery products, chocolate products and snack food items. 

### Additional Cleaning Needed
When creating the full contingency table in R, it can be seen that the underlying dataset is not as clean as I would like it to be. "Food-borne Illness" is not a category of food but for some reason it is showing up in that column. There are also a bunch of entries which don't have anything listed in the Food.Subcategory column because nothing was listed in the original dataset. If I wanted to do further analysis on this dataset, I would need to spend a significant amount of time further cleaning the dataset. This project was a good introduction to the issues present in a real world government dataset. 
