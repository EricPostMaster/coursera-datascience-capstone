# Opening a Restaurant in North Carolina
## Introduction
North Carolina's population has grown 32.5% over the past 20 years, and the state is expected to grow by another 100,000 people per year until at least 2038, at which point the state's population will be nearly 13 million [1].  That's a lot of mouths to feed!  This is a good opportunity for forward-thinking restaurant owners and aspiring restaurateurs to make a move into markets that are in early development and are projected to grow significantly into the 2030s.

### Target Audience

According to the National Restaurant Association, there are over 19,000 eating and drinking locations in North Carolina, and restaurant and foodservice work accounts for 11% of state employment [2]!  But competition is fierce in the restaurant industry, and the median lifespan of a small startup restaurant (less than 5 employees) is only 3.75 years [3].  I am a firm believer in the value and viability of smart small businesses, so my goal with this project is to assist small businesses in identifying potential locations for food and drink establishments.

### The Challenge: Reading the Market

Wayne Gretzky, one of the greatest hockey players in history, is often credited with saying that part of his success was due to the fact that he did not skate to where the puck was but rather to where it was going.  If one can predict where the market will swing with some degree of accuracy, then they are more likely to achieve a successful business outcome.

But how to predict that in North Carolina?  One way to predict market growth is to use housing price data.  As demand for real estate increases, home prices will follow suit.  We will use average home price growth as a primary indicator of potential markets.

Another important factor to consider is competition.  Someone may have an outstanding idea for a Mexican food restaurant, but if there is already successful super deluxe burrito and salsa bar in the area of town you are interested in, it might be wise to consider other location possibilities.  We will use eatery data from Foursquare to help identify those potential locations.

## Data
Data for this report will be pulled from multiple sources:
- Housing price data will be sourced from <a href="https://www.zillow.com/research/data/" target="_blank">Zillow's publicly available research database,</a> specifically the Zillow Home Value Index (ZHVI).
- Competition (i.e. currently operating food and drink establishments) data will be sourced from Foursquare.
- Zip code geolocation coordinate data will be sourced from <a href="https://github.com/OpenDataDE/State-zip-code-GeoJSON" target="_blank">Open Data Delaware on GitHub.</a>

## Methodology & Results

This project consisted of two main components: identifying the zip codes in North Carolina experiencing large growth in average home value and then mapping food establishments to those zip codes to identify potential locations for restaurants.

The methodology can be viewed in detail in the accompanying Jupyter notebook, but I will summarize here as well.

### Identifying Target Zip Codes 

First, I downloaded and cleaned Zillow Home Value Index data for all of North Carolina and segmented out only the largest 150 zip codes in the state, figuring that the great majority of people live in those areas.

![home_value_growth_dataframe](images/home_value_growth.png)

