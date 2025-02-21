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
- Grouped ‘Type’ column into two categories: Movie and TV Show
<img width="469" alt="Image" src="https://github.com/user-attachments/assets/0a291d7f-ea54-435c-b553-d62c2c8d4025" />

- Extracted the First Genre from the Genres column using DAX:
<img width="172" alt="Image" src="https://github.com/user-attachments/assets/0c5d446a-4fb9-42bb-bf34-6a4e22bd8240" />

- Created Rating Groups (0-9) for better categorization.
<img width="253" alt="Image" src="https://github.com/user-attachments/assets/a6b94818-899b-4724-99a9-e28b7fcab222" />

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

<img width="415" alt="Image" src="https://github.com/user-attachments/assets/e8d945a4-4b35-4428-8501-0723440fa339" />

### 6. Table with Images
- Displays:
Title, Poster Image, Rating, Plot, Number of Votes
- Custom formatting for Rating was applied using a DAX formula.

### 7. Table
- Displays:
  Country, Total number of titles, Average Rating, Total number of Votes, Total Votes per titles
  
### DAX Measures Used
- <img width="220" alt="Image" src="https://github.com/user-attachments/assets/308c3455-2e83-450c-a5ef-931214faf30d" />

- <img width="164" alt="Image" src="https://github.com/user-attachments/assets/ed5476a3-ba18-4560-8a86-358e6740ec2a" />

- <img width="225" alt="Image" src="https://github.com/user-attachments/assets/ead1cd5e-5f8c-4d2c-9df2-053ad33126c2" />

- <img width="197" alt="Image" src="https://github.com/user-attachments/assets/1146c4c6-c78f-4f2d-bc74-2cc781de6d43" />

- <img width="446" alt="Image" src="https://github.com/user-attachments/assets/bbf9b5b9-6863-432f-8684-23e3dd0ba42a" />

- <img width="426" alt="Image" src="https://github.com/user-attachments/assets/c92af264-c264-468c-a707-5bbd2ee0b168" />

- <img width="242" alt="Image" src="https://github.com/user-attachments/assets/4ae2e921-59a4-4e89-97be-b71637e468ac" />

- <img width="457" alt="Image" src="https://github.com/user-attachments/assets/b737001e-334d-4915-b10d-25a95e079e97" />

- <img width="411" alt="Image" src="https://github.com/user-attachments/assets/7bbcbca4-b284-4e1f-9873-81d4d9cd1fb0" />

- <img width="461" alt="Image" src="https://github.com/user-attachments/assets/0f0dea8b-7efe-4a26-b731-06913cbf68e9" />

- <img width="431" alt="Image" src="https://github.com/user-attachments/assets/da923066-dc0d-4166-bc47-6de7c1258c6d" />

- <img width="212" alt="Image" src="https://github.com/user-attachments/assets/c62ca99b-73df-42e6-a5d3-e86d3e24b888" />

- <img width="407" alt="Image" src="https://github.com/user-attachments/assets/464dc806-c3b0-4c55-9126-be492d4551a0" />

- <img width="467" alt="Image" src="https://github.com/user-attachments/assets/f7f93255-de9e-4dee-af79-29b1e35f5b63" />


## Netflix Dashboard

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


 



