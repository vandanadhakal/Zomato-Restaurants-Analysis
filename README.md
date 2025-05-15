# Zomato-Restaurants-Analysis

## Overview
Zomato is a multinational restaurant aggregator and food delivery company. This project analyzes the business performance of restaurants from various aspects of the restaurant market.
There are 1,48,455 restaurants listed in the restaurants.csv of the Zomato database. The analysis is done in 3 major categories for the restaurants: Veg and non-Veg Analysis, Sales Analysis, and Cuisine Analysis. 

The Project Tableau Visualization can be found <a href='https://public.tableau.com/app/profile/vandana.dhakal/viz/ZomatoRestaurantAnalysis_17443888388170/ZomatoRestaurantsAnalysis?publish=yes'><u>here</u>.</a>

The Tableau Visualization in pdf is <a href='https://github.com/vandanadhakal/Zomato-Restaurants-Analysis/blob/main/Zomato%20Restaurants%20Analysis.pdf'><u>here</u>.</a>

The Project Report with Explanation of Visuals can be found <a href='https://github.com/vandanadhakal/Zomato-Restaurants-Analysis/blob/main/Zomato%20Analysis-Final%20Report.pdf'><u>here</u>.</a>

## Analysis
1. Veg and Non-Veg Analysis: In the world, the highest population of Vegetarians reside in India. About 20% - 39% of Indian population is vegetarians. Are there vegetarians’ restaurants to cater these population? How does the customer feel about the vegetarian food vs non-vegetarian food?

2. Sales Analysis: Which cities have the largest number of restaurants? Does having more restaurants bring more revenue for the cities' restaurants? How does sales look like over time?

3. Cuisine Analysis: Are Restaurants more inclined to have Indian cuisines on their menu? Is there influence from other parts of the world on Indian restaurant industry?



## Data Cleaning and Preparation
1.	Cuisine information (String type) is provided in a random way. For example, “Pizzas, Beverages” are cuisines of some restaurants while “Beverages, Pizzas” are for others. They are the same but written differently. So, the words in the cuisines are separated, sorted and combined alphabetically.
2.	Rating is in String type data, to make it usable this data is converted to float and ‘--' is assigned 0.0. New column Rating Clean is created to store this data.
3.	Cost from restaurant table is in text format, it needs to be converted to real after removing the Indian Rupee symbol (character ₹). 
4.	Restaurant is characterized as ‘Veg Only’ and ‘Veg and non-Veg’ based on whether the restaurant sold only veg food or both veg and non-veg food.

## Assumptions
1.	The Cost (Cost Real) in the Restaurant table is considered the average cost of food item in the restaurant.
2.	Restaurant type is determined by the Cuisine type of the restaurant. For example, “Chinese, Indian”, “Desserts, Ice Cream” etc
3.	Ratings of the customers is a reflection of their perception/satisfaction level of the food item.
4.	The Veg/non-Veg categorization of the restaurants are done based on the kind of foods each restaurant is selling. If the restaurant is selling vegetarian foods only, the restaurant is considered vegetarian restaurant. If it is selling both veg and non-veg food the restaurant is considered non-veg. 

## Limitation
1.	The addresses of the restaurants are provided in an inconsistent format. Zipcodes, city, states, or country are provided to some and not to others. Eg:
   
a.	Singh Hut, CIRCULAR ROAD NEAR NEHRU PARK ABOHAR

b.	CHAWLA SAAB THE JUICE MASTER, SAHITYA SADAN MARKET, ABOHAR ,  Abohar (M Cl) , Fazilka 1(Abohar), Fazilka,  Punjab-152116

c.	The Momo corner, F-318 Kamla Nagar Agra

So, use of these data for geographical representation or Geocoding is not possible.

2.	Demographics studies within a city could provide more information on the restaurant types, number and provide explanation on the sales. Demographics isn’t going to be studied in this analysis.
   
3.	Some text fields in the database are not in a clean format. For example, search of the word Domino in the Restaurant name returns multiple data with one symbol variation (– or , or ‘ etc). This causes confusion and errors in the analysis. Same is true for other fields.

## Future Improvements on Data
A lot of fields data in the database is not in a clean format and wasn’t possible to clean before use. For example, for the Restaurant Name below, search of the word Domino returns the following. The names of these restaurants have one symbol (– or , or ‘ etc) difference. Whether this is intentional or not is not something an analyst would know. This causes confusion and errors in the analysis. Same is true for other fields.

The addresses of the restaurants are also provided in an inconsistent fashion. A lot of the addresses misses major parts of the address format. This makes it difficult to analyze the data in terms of geographical locations.

These are some areas of data that could be improved to have more accurate analysis.
