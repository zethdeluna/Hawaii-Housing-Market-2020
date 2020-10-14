# Hawaii Housing Market 2020
Hawaii is known for its beautiful culture, delicious food, and that feeling of paradise anywhere you go in the islands. It's no wonder why people are looking to Hawaii when they're trying to escape the hustle and bustle of the typical American city.   

We're going to analyze data on housing in Hawaii that I scraped from Zillow.com, a popular American online real estate marketplace that allows consumers to explore their potential new home with the help of pictures, current market prices, rooms, square-footage, and more. The data (available in my repository) contains information on Zillow listings in Hawaii that were available on September 21st of 2020. We're going to use this data to train and test various regression models to predict the price of a house given its features (number of bedrooms/bathrooms, square-footage, location).  

Results: We were able to train a model that predicts the price of a property in Hawaii with an R<sup>2</sup> value around 0.75 using housing features including: type (Condo, House, Studio, or Townhouse), square-footage, number of bedrooms/bathrooms, and location (street, city, and zipcode).

## The Data
`hawaii_listings_2020.csv` 
  * Contains uncleaned data on the housing market in Hawaii (Oahu, Maui, Kauai, and the Island of Hawaii) scraped from Zillow.
  * Feature Definitions:
    * `address`: the address of the listing (e.g. 5621 Kalanianaole Hwy, Honolulu, HI 96821)
    * `url`: link to the webpage of the listing
    * `type`: the type of property (e.g. House, Condo, Studio, etc.)
    * `bedrooms`: number of bedrooms
    * `bathrooms`: number of bathrooms
    * `sqft`: square-footage of the property
  
`zipcode_islands.csv`
  * Contains Hawaii zipcodes grouped by island
 
 `for_sale_by_owner.csv` and `new_construction.csv`
  * These datasets contain the property types of some listings from `hawaii_listings_2020` that were missing their property type.
  * Column Definitions:
    * `Index`: index of the listing taken from `hawaii_listings_2020`
    * `type`: property type &mdash; Condo, House, Townhouse, or weird (weird implies the listing needs further investigation)
