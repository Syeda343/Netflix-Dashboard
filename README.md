# Netflix-Dashboard

## Overview
This project is a Netflix Analytics Dashboard built in Power BI, designed to analyze Netflix movies and TV shows based on ratings, votes, and genres across different countries. The dashboard includes key visualizations like geo mapping, reference cards, bar charts, funnel charts, and tables with images.

## Dataset
The dataset used for this project was sourced from Kaggle:
https://www.kaggle.com/datasets/snehaanbhawal/netflix-tv-shows-and-movie-list

## Data Preparation
To prepare the dataset for analysis, the following data cleaning steps were performed:

### 1. Removing Unnecessary Columns
The following columns were removed as they were not required for analysis:
•	Popular Rank
•	Certificate
•	Episodes
•	Language
•	Summary
•	IsAdult
•	Cast

### 2. Renaming Columns
To improve clarity, column names were updated to more intuitive names.

### 3. Changing Data Types
- ID, Title, Start Year, Type, Country, Plot, and Genre → Converted to TEXT
- Rating → Converted to DECIMAL
- Votes and Runtime → Converted to WHOLE NUMBER

### 4. Handling Missing and Incorrect Values
- Runtime: Replaced /N values with NULL.
- Type: Removed rows where the Type column was empty.
- Rating: Removed rows with missing ratings (since the focus is on rated content).
- Country: Removed rows where the Country column was empty.

### 5. Creating New Columns
- Grouped ‘Type’ column into two categories:
o	Movie
o	TV Show
- Extracted the First Genre from the Genres column using DAX:
Genre = LEFT(Listings[Genres], SEARCH(",", Listings[Genres], , LEN(Listings[Genres]) + 1) - 1)
- Created Rating Groups (0-9) for better categorization.

## Power BI Dashboard Features

### 1. Reference Card
Displays key performance indicators (KPIs):
- Total Number of Titles
- Average Rating
- Total Number of Votes

### 2. Slicer for Filtering
- Allows users to manually search and filter the dashboard by Movies or TV Shows.

### 3. Bar Chart: Average Rating & Number of Titles by Genre
- Sorted left to right, showing highest-rated genres.
- Uses a third dimension to show which genre has the most titles.

### 4. Funnel Chart: Number of Titles by Rating Group
- Sorted by rating groups.
- Helps visualize the distribution of movies and TV shows across different ratings.

### 5. Geo Mapping with Dynamic Bubble Size
- Bubble size represents the number of titles in each country.
- Allows dynamic selection to show Ratings and Votes using Parameters.
- Helps visualize distribution across countries and genres.

### 6. Table with Images
- Displays:
Title, Poster Image, Rating, Plot, Number of Votes
- Custom formatting for Rating was applied using a DAX formula.

### 7. Table
- Displays:
  Country, Total number of titles, Average Rating, Total number of Votes, Total Votes per titles

![Image](https://github.com/user-attachments/assets/f1bd2791-37a6-485e-9c15-401a659fa0c9)

## How to Use This Repository
- 1.	Download the Dataset from Kaggle.
- 2.	Load the dataset into Power BI.
- 3.	Follow the data cleaning steps outlined above.
- 4.	Use the provided DAX measures to create visualizations.
- 5.	Design the dashboard using slicers, charts, and tables.

## Future Enhancements
- Implement time-series analysis to track trends over time.
- Add user-driven filters for dynamic insights.
- Integrate IMDb or Rotten Tomatoes scores for additional insights.

## Conclusion
This Power BI dashboard provides a comprehensive analysis of Netflix movies and TV shows, helping users explore trends based on ratings, genres, votes, and country-wise distributions. The dynamic visualizations make it easier to understand the data at a glance.

## Acknowledgment
"This dashboard was recreated as part of my learning journey after watching a tutorial on YouTube. Full credit to the original creator for their guidance and inspiration." The link to the tutorial is http://www.youtube.com/@PowerBIBro


 



