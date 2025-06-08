# UK Food Hygiene Database Analysis

This project analyzes food hygiene ratings from the UK Food Standards Agency to provide insights for *Eat Safe, Love* magazine.

## Setup

1. **Import the Data**: 
   Use `mongoimport` to load the `establishments.json` file into a MongoDB database named `uk_food`, with a collection `establishments`.

2. **Notebook Setup**: 
   - Import libraries like `pymongo` and `pprint`.
   - Set up a MongoDB client to connect to the `uk_food` database.
   - Confirm the database and collection are properly created.

## Part 1: Database Setup and Data Import 

- **Data Import**: Imported the `establishments.json` file into the `uk_food` database and confirmed the collection was created.
- **Database Check**: Ensured the `uk_food` database and `establishments` collection were correctly listed.
- **Data Verification**: Displayed one document from the collection to confirm proper import and data format.

## Part 2: Database Updates

- **Add New Restaurant**: Added *Penang Flavours*, a new restaurant, to the collection with all necessary details including business type, address, and geocode.
- **BusinessTypeID Update**: Retrieved the `BusinessTypeID` for "Restaurant/Cafe/Canteen" and updated *Penang Flavours* with the correct ID.
- **Remove Dover Establishments**: Found and removed all establishments under the Dover local authority and confirmed deletion by checking the updated document count.
- **Data Type Conversion**: Converted latitude, longitude, and `RatingValue` fields to appropriate data types using `update_many` to ensure proper querying.

## Part 3: Exploratory Analysis

- **Hygiene Score of 20**: Identified all establishments with a hygiene score of 20, providing insights into the hygiene levels of lower-rated establishments.
- **London Establishments with RatingValue >= 4**: Filtered establishments in London with a rating of 4 or higher to identify top-rated locations.
- **Top 5 Establishments Near *Penang Flavours***: Found the five closest establishments with a rating of 5 and sorted by hygiene score, helping to highlight the best-rated and nearest food spots.
- **Hygiene Score of 0 in Local Authorities**: Analyzed the top 10 local authority areas with the most establishments having a hygiene score of 0, helping to target areas with the worst hygiene practices.

## Conclusion

This project successfully utilized MongoDB to manage and analyze food hygiene ratings across the UK. The following key insights were derived:

- **New Restaurant**: Added *Penang Flavours* as a new restaurant, contributing to the dataset and improving its completeness.
- **Data Cleanup**: Removed establishments in Dover and corrected data types, ensuring more accurate queries and analysis.
- **Exploratory Analysis**: The analysis addressed specific questions, providing valuable insights:
  - **Hygiene Score Trends**: Found establishments with poor hygiene scores and highlighted areas for improvement.
  - **Top Locations**: Identified highly-rated establishments in London and near *Penang Flavours*.
  - **Local Authority Analysis**: Highlighted local authorities with the most poor hygiene establishments, guiding future actions for health and safety.

These findings will assist *Eat Safe, Love* magazine in focusing their future articles on establishments with better hygiene practices and help them avoid locations with poor ratings.
