# ECE-2112--Exploratory-Data-Analysis-on-Spotify-2023-Dataset

## Getting Started
This project explores a dataset containing Spotify track details for 2023. We perform an exploratory data analysis (EDA) using Python libraries such as `pandas`, `matplotlib`, and `seaborn`.

### Problem 1: Load and Explore the Dataset
This script begins by loading the Spotify dataset using the `pandas` library. The `read_csv()` function is used to load the CSV file into a DataFrame (`df`). The shape of the dataset (number of rows and columns) is displayed using `df.shape`, and the `df.info()` function provides additional details about the data types and any missing values. The first few rows of the dataset are inspected with `df.head()`, and the column names are displayed using `df.columns` to understand the structure of the dataset.

#### Insight:
- The dataset contains information about tracks in the year 2023, with columns related to the track's name, artist, streams, release year, and various musical attributes.

### Problem 2: Handle Missing Data and Convert Columns
In this step, the 'streams' column is converted to numeric using `pd.to_numeric()`, with the `errors='coerce'` argument ensuring that any invalid or non-numeric entries are converted to `NaN`. Afterward, missing values in the 'streams' column are dropped using `df.dropna()`, ensuring that the dataset only includes rows with valid stream data.

#### Insight:
- By coercing non-numeric values in the 'streams' column to `NaN` and then removing rows with missing values, we ensure that subsequent analyses are based on clean and valid stream data.

### Problem 3: Summary Statistics for 'Streams'
The `describe()` function is used to calculate summary statistics for the 'streams' column, such as the mean, standard deviation, minimum, and maximum values. Additionally, the median and standard deviation of the 'streams' column are calculated separately to provide more specific insights into the distribution of streams across the dataset.

#### Insight:
- The summary statistics of the 'streams' column reveal the central tendency (mean and median) and spread (standard deviation) of the streams, which helps in understanding the typical popularity of a track and its variance across the dataset.

### Problem 4: Tracks Released Per Year and Month
The `value_counts()` function is used to count the number of tracks released each year (`tracks_per_year`) and month (`tracks_per_month`). These values are then visualized using bar plots to observe any trends or seasonality in track releases.

#### Insight:
- The bar charts show the distribution of tracks over time, highlighting which years and months had the most releases. This helps to identify trends, such as an increase or decrease in track releases during specific months or years.
  
### Problem 5: Correlation Between Musical Attributes and Streams
Using Seaborn's `pairplot()`, we visualize the relationships between various musical attributes (e.g., `bpm`, `danceability_%`, and `energy_%`) and the 'streams' column. This allows us to identify any potential linear relationships between these features and track popularity (streams).

#### Insight:
- The pair plot reveals how the 'streams' column correlates with attributes like 'bpm', 'danceability', and 'energy'. For example, tracks with higher energy levels may have a positive correlation with higher streams, suggesting that more energetic songs tend to be more popular.

### Problem 6: Correlation Between Other Musical Features
Next, we calculate the correlation between 'danceability_%' and 'energy_%', and between 'valence_%' and 'acousticness_%' using the `corr()` function. These correlation matrices are displayed to understand how these features are related to each other.

#### Insight:
- The correlation matrices provide a quantitative measure of how closely related pairs of musical attributes are. For instance, a high positive correlation between 'danceability' and 'energy' might suggest that tracks with higher energy are also perceived as more danceable.

### Problem 7: Tracks in Different Platforms
In this step, we analyze how many tracks are available across different platforms such as Spotify playlists, Spotify charts, and Apple playlists. The `sum()` function is used to count the total number of tracks in each platform category, and the results are visualized in a bar chart.


#### Insight:
- The bar chart shows the distribution of tracks across various platforms. This helps identify how many tracks are included in Spotify playlists, Spotify charts, and Apple playlists, indicating the visibility of tracks on different platforms.

### Problem 8: Top 5 Most Frequent Artists
We use the `value_counts()` function to find the top 5 most frequent artists in the dataset. This is followed by creating a DataFrame to present the number of tracks for each artist.

#### Insight:
- The most frequent artists are listed along with the number of tracks they have in the dataset. This helps identify the artists who dominate the track releases in the dataset.


# Author
Samantha Louise J. Samoy

2ECE-C
