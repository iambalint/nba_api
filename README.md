# NBA Shot Analysis Project

This repository contains a Python-based analysis of NBA player Victor Wembanyama's shooting data across various seasons. The project leverages the nba_api library to extract detailed shot data and visualize it using seaborn and matplotlib.


## Summary
The project performs the following key steps:

1. **Player and Career Data Retrieval:** Retrieves player details and career statistics using the nba_api library.
2. **Shot and Game Data Extraction:** Extracts shot data for each season and combines it with game information.
3. **Data Aggregation and Transformation:** Groups and pivots data for analysis by shot distance and season.
4. **Visualization:** Creates visualizations to depict shot performance trends across seasons and distances.


## Features
- Extract player and game data using nba_api.
- Combine and transform shot and game data for analysis.
- Visualize shooting trends by distance and season using seaborn and matplotlib.


## Tools and Libraries Used

### Python Libraries:
- **nba_api:** For accessing NBA player and game data.
- **pandas:** For data manipulation and transformation.
- **seaborn:** For creating statistical visualizations.
- **matplotlib:** For plotting custom visualizations.
- **requests:** For handling API requests.
- **json:** For parsing JSON data.


## Step-by-Step Overview

### 1. Player and Career Data Retrieval
- Use `nba_api.stats.static.players` to find Victor Wembanyama's player ID.
- Fetch his career statistics using `playercareerstats.PlayerCareerStats`.
- Identify all NBA seasons he played in.

### 2. Shot and Game Data Extraction
- Retrieve all game data using `leaguegamefinder.LeagueGameFinder`.
- Extract shot chart details for each season using `shotchartdetail.ShotChartDetail`.
- Combine shot data across all seasons into a single DataFrame.

### 3. Data Aggregation and Transformation
- Group data by season and shot distance to count the number of shot attempts.
- Pivot the data to prepare it for visualization, focusing on close, mid-range, and long-distance shots.

### 4. Visualization
- Use seaborn's FacetGrid to create a ridgeline plot of shot distances over seasons.
- Customize the plot with labels, themes, and player-specific annotations.

## How to Use

### Prerequisites
- Install the required Python libraries using pip:
  ```bash
  pip install nba_api pandas seaborn matplotlib requests
  ```

### Running the Code
1. Clone the repository and navigate to the project directory.
2. Run the Python script to fetch and analyze player data:
   ```bash
   python analyze_shots.py
   ```
3. View the generated visualizations in the `visualizations` directory.


## Summary
This project demonstrates how to analyze and visualize NBA player shooting data using Python. By combining game and shot chart data, it provides a detailed look at Victor Wembanyama's shooting trends over his career. The pipeline can be adapted for other players or advanced analytics.

Feel free to explore and customize the code for your specific use case!

