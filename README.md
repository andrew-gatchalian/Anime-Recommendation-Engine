## 🌟 Anime Recommendation Engine Project 🌟
Dive into the world of Japanese animation with our team's Anime Recommendation Engine! Developed by Yilu Chen, Andrew Gatchalian, Sara Hart, Hsuan-Yi Lin, and Rakesh Venkata Subramaniyan at the University of California, Irvine.
- Leveraged viewer preference data to develop a machine learning recommendation engine for anime.
- Utilized web scraping and API integration to collect, clean, and pre-process data from MyAnimeList.

# Context
This dataset for this project is available on my [Kaggle](https://www.kaggle.com/datasets/andrewgatchalian/myanimelist-user-ratings) account. It contains over 44 million rows of anime-related data, representing interactions from 18,145 unique users and 16,135 unique shows.

# Source
The data was sourced directly from the website MyAnimeList, one of the largest anime-driven forums that allows users to track, rate, and review anime.

The dataset contains 4 files:
- `anime_titles.csv` is a list of all available anime titles from MyAnimeList (IDs 1 to ~52,000). The data was pulled using MyAnimeList's API (last updated 11/2023). 
- `anime_user_ratings.csv` contains over 40 million ratings from over 18k users, pulled from the MyAnimeList API. Data was cleaned to only include: 'Completed' & 'Dropped' status and non-zero ratings (removed '0' ratings since there was overlap with users who did not rate titles). *NOTE: Users are a random sample from over 70k unique usernames we collected. Usernames were web scraped from the MyAnimeList [Recently Online Users](https://myanimelist.net/users.php) tab over the span of November 2023.*
- `anime_genres.csv` is a file containing dummy variables for all available genres in our dataset (for modeling purposes).
- `username_list_full.csv` is a list of over 70k unique usernames scraped from MyAnimeList.

&gt;Instances of '-1' in the data represent information unavailable on MyAnimeList as of 11/2023.

# Content
`anime_titles.csv`
- **anime_id**: MyAnimeList unique number ID
- **title**: full name of anime
- **mean**: average user rating on MyAnimeList (as of 11/2023)
- **genres**: comma separated list of genres
- **studios**: animation studio(s)
- **synopsis**: anime summary
- **media_type**: type of medium (tv, movie, ona)
- **num_episodes**: number of episode(s) per anime

`anime_user_ratings.csv`
- **user_id**: MyAnimeList username
- **anime_id**: MyAnimeList unique number ID
- **title**: full name of anime
- **user_status**: completion status (only limited to completed or dropped)
- **user_score**: user rating of anime
- **user_eps_watched**: number of episodes watched
- **user_rewatch**: if user is watching show again (Bool)
- **updated_at**: rating time stamp

`anime_genres.csv`
- **anime_id**: MyAnimeList unique number ID
- **genre_(*)**: genre_(name of genre)

`username_list_full.csv`
- **username**: MyAnimeList username

# Acknowledgements
Thanks to:
1. [MyAnimeList](https://myanimelist.net/) website and API
2. [Cooperunion](https://www.kaggle.com/datasets/CooperUnion/anime-recommendations-database) Kaggle Dataset

# Inspiration
To make anime accessible for both old and new viewers!
