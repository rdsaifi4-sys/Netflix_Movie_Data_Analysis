# Netflix_Movie_Data_Analysis
Project Summary: Netflix Movie Database Analysis 
Project Overview: This project involved an end-to-end data analysis of a movie database containing 9,827 entries. The goal was to clean the raw data, perform 
exploratory data analysis (EDA), and visualize key trends such as genre distribution, popularity outliers, and movie ratings.  
1. Data Inventory & Exploration 
Initial inspection of the mymoviedb.csv file revealed a robust dataset with the following characteristics:  
• Total Rows: 9,827 
• Total Columns: 9 (Release_Date, Title, Overview, Popularity, Vote_Count, Vote_Average, Original_Language, Genre, Poster_Url) 
• Data Quality: The dataset was initially very massy, contains many missing values.  
• Missing Values: Inspection revealed 100 missing values in the Vote_Average column, which were subsequently dropped to ensure statistical accuracy.  
2. Data Cleaning & Feature Engineering 
To prepare the data for visualization, several transformation steps were executed: 
• Temporal Conversion: The Release_Date was converted to datetime64[us] format. The year was then extracted as an integer to facilitate chronological 
analysis.  
• Dimensionality Reduction: Irrelevant columns for this specific analysis—Overview, Original_Language, and Poster_Url—were dropped to streamline the 
dataframe.  
• Genre Normalization: The Genre column contained comma-separated strings (e.g., "Action, Adventure"). These were split into lists and "exploded," resulting in 
a new expanded dataset of 25,552 rows, where every movie-genre pair occupies its own row.  
• Categorization: Using a custom categorize_col() function, the Vote_Average was binned into four distinct categories based on quartiles: not_popular, 
below_average, average, and popular.  
3. Statistical Insights 
Through the df.describe() method, the following metrics were identified:  
• Average Rating: The mean Vote_Average across the dataset is 6.44.  
• Popularity Trends: The mean popularity is 40.33, but a massive standard deviation of 108.87 indicates significant outliers.  
• Max Popularity: The most popular movie in the dataset is "Spider-Man: No Way Home" (2021), with a popularity score of 5083.95.  
• Vote Distribution: The categorizing process resulted in a balanced distribution 
across the four rating tiers, with "not_popular" holding 2,467 entries and "popular" holding 2,450.  
4. Key Visualizations & Findings 
A. Genre Dominance 
Analysis of the 19 unique genres revealed that Drama is the most frequent genre in the database, appearing 3,715 times. Other highly frequent genres include Comedy and Action.  
B. Historical Production Trends 
A histogram of the Release_Date shows that movie production has seen an exponential increase over the decades, with the vast majority of the 9,827 movies being released between 2010 and 2022.  
5. Conclusion 
The analysis successfully transformed a raw CSV into a clean, categorical dataset. The findings highlight a modern-leaning database where Drama is the king of content, and high-budget blockbusters like Spider-Man: No Way Home represent extreme statistical outliers in terms of global popularity. indings highlight a modern-leaning database where Drama is the king of content, and high-budget blockbusters like Spider-Man: No Way Home represent extreme statistical 
outliers in terms of global popularity. 
