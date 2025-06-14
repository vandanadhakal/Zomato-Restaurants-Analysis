# Zomato Restaurant Segmentation Analysis

## Overview
Zomato is a multinational restaurant aggregator and food delivery company. This project analyzes the business performance of restaurants from various aspects of the restaurant market.
There are 1,48,455 restaurants listed in the restaurants.csv of the Zomato database. The analysis is done in 3 major categories for the restaurants: Veg and non-Veg Analysis, Sales Analysis, and Cuisine Analysis.

#### Database

<img src="https://github.com/vandanadhakal/Zomato-Restaurants-Analysis/blob/main/Database.png">

The Project Tableau Visualization can be found <a href='https://public.tableau.com/app/profile/vandana.dhakal/viz/ZomatoRestaurantAnalysis_17443888388170/ZomatoRestaurantsAnalysis?publish=yes'><u>here</u>.</a>

The Tableau Visualization in pdf is <a href='https://github.com/vandanadhakal/Zomato-Restaurants-Analysis/blob/main/Zomato%20Restaurants%20Analysis.pdf'><u>here</u>.</a>

The Project Report with Explanation of Visuals can be found <a href='https://github.com/vandanadhakal/Zomato-Restaurants-Analysis/blob/main/Zomato%20Analysis-Final%20Report.pdf'><u>here</u>.</a>

## Analysis
1. Veg and Non-Veg Analysis: In the world, the highest population of Vegetarians reside in India. About 20% - 39% of Indian population is vegetarians. Are there vegetarians’ restaurants to cater these population? How does the customer feel about the vegetarian food vs non-vegetarian food?

2. Sales Analysis: Which cities have the largest number of restaurants? Does having more restaurants bring more revenue for the cities' restaurants? How does sales look like over time?

3. Cuisine Analysis: Are Restaurants more inclined to have Indian cuisines on their menu? Is there influence from other parts of the world on Indian restaurant industry?

<img src="https://github.com/vandanadhakal/Zomato-Restaurants-Analysis/blob/main/Ve%3Anon-Veg%20Story.png">

<img src="https://github.com/vandanadhakal/Zomato-Restaurants-Analysis/blob/main/Veg%3Anon-Veg%20Analysis.png">

## Conclusions
Only 1.86% of the restaurants are veg only. 18.1% are veg and non-veg type restaurants. 80% of the restaurants don’t have any food/category assigned to them.
27.3% of food items are categorized as non-vegetarian food and 73.31% as vegetarian foods. Only 2.4% of sales are from restaurants that are veg only. 21.8% are from veg/non-veg restaurants. Rest from restaurants that aren’t categorized as veg/non-veg. 

Large number of foods have prices within ₹100 - ₹300 range. Foods costing the same have ratings that vary largely. Generally, higher costing foods have higher ratings but the number of ratings for higher cost foods are low indicating few numbers of people are eating higher cost foods. Lots of low-cost foods (₹50 - ₹400) have good ratings that are > 3.5. Based on the number of reviews and value of the ratings, Zomato customers find worth in less pricey foods.  

Cities like ‘Bikaner’, ‘Noida-1’, ‘Indirapuram, Delhi’ have the largest numbers of restaurants. Bikaner has 1666 restaurants with ₹11M in sales. ‘Electronic City, Bangalore’ has the largest cumulative sales of ₹29M with only 1039 restaurants. The number of cities and sales don’t have direct relationship, it is important to understand the population, demographics and prevalence of offices in the cities to get a better picture on this topic. 

India has lots of chain restaurants. Restaurants with multiple locations have larger cumulative sales. Restaurants with just a single location or very few locations see large sales per restaurants compared to restaurant chains. Having more restaurant locations doesn’t mean more sales for each location which in turn may not mean more profit as well. Sales of the restaurants is in a declining trend from Q4 2017 to Q2 2020. Most quarters have seen sales decline from the previous quarter. Covid may be responsible for the declines in 2020 but the reasons for the declines in previous years need more study.

Among the 15 most adopted cuisines by the restaurants, 8759 restaurants are branded as “Chinese, North Indian”, the cuisine adopted by the largest number of restaurants. Looking at the name of the top cuisines, Indian restaurant industry is influenced by neighboring country China. Lots of restaurant’s cuisines are a fusion of cuisines from around the world for example, ‘Chinese, North Indian’, ‘Continental, Pizzas’, ‘Italian, Mexican’. Multiple chain restaurants like Domino’s Pizza, Pizza Hut, KFC etc have larger number of restaurants under their belts. The presence of these restaurants along with Baskin Robins, Subway, McDonald’s to name some is an indication that Indian restaurant market is influence by western foods/restaurants. 

## Recommentdations
#### Veg/non-Veg Analysis
- Restaurants should provide the information on food items and their veg and non-veg category to increase visibility, trust and making it easier for customers to order food. 
- There is very low percentage of vegetarian only restaurant serving the vegetarian population. Restaurant community or prospective restaurant owners could tap into this deficit to attract this population to their restaurants. 
- As lower cost foods are preferred by customers, restaurant owner could focus and increase the variety of low-cost food offered by the restaurants. 
- For a non-veg restaurant, the variety of non-veg menu can be increased to provide more choices to the customers as people are eating veg and non-veg food equally and satisfied by both.
#### Sales Analysis
- Restaurants in certain cities like ‘Electronic City, Bangalore’, ‘Malviya Nagar, Delhi’ etc. have more sales, so prospective restaurants owners may benefit from this. But this requires study into demographics and socio-economic aspects of the cities. 
- It is beneficial to have restaurants with 1 or few locations from sales point of view. They turn in more sales per restaurants than chain restaurants.
#### Cuisine Analysis
- Bringing food from around the world to test the Indian market could be a good starting approach for someone in the culinary world.
- Since Indian food with a fusion of Chinese food have large sales so, including Chinese foods in the restaurants may not go wrong. 

<img src="https://github.com/vandanadhakal/Zomato-Restaurants-Analysis/blob/main/Recommendations.png">

## Data Cleaning and Preparation
The following were used to clean and prepare the data for analysis:
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
   
   _a.	Singh Hut, CIRCULAR ROAD NEAR NEHRU PARK ABOHAR_

   _b.	CHAWLA SAAB THE JUICE MASTER, SAHITYA SADAN MARKET, ABOHAR ,  Abohar (M Cl) , Fazilka 1(Abohar), Fazilka,  Punjab-152116_

   _c.	The Momo corner, F-318 Kamla Nagar Agra_

So, use of these data for geographical representation or Geocoding is not possible.

2.	Demographics studies within a city could provide more information on the restaurant types, number and provide explanation on the sales. Demographics isn’t going to be studied in this analysis.
   
3.	Some text fields in the database are not in a clean format. For example, search of the word Domino in the Restaurant name returns multiple data with one symbol variation (– or , or ‘ etc). This causes confusion and errors in the analysis. Same is true for other fields.

## Future Improvements on Data
A lot of fields data in the database is not in a clean format and wasn’t possible to clean before use. For example, for the Restaurant Name below, search of the word Domino returns the following. The names of these restaurants have one symbol (– or , or ‘ etc) difference. Whether this is intentional or not is not something an analyst would know. This causes confusion and errors in the analysis. Same is true for other fields.

<img src="https://github.com/vandanadhakal/Zomato-Restaurants-Analysis/blob/main/Restaurant%20Name%20Mismatches.png">

The addresses of the restaurants are also provided in an inconsistent fashion. A lot of the addresses misses major parts of the address format. This makes it difficult to analyze the data in terms of geographical locations.

These are some areas of data that could be improved to have more accurate analysis.

