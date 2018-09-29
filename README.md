# Basketball Statistics Project

This data storytelling project aims to explore the relationship between NBA team and player statistics and the number of wins/rating of each team. It uses pandas , numpy, and matplotlib to extract, clean, and visualize data from <https://www.basketball-reference.com/>. I used 20 years worth of team per game stats, opponent per game stats, miscellaneous per game stats, and advanced player statistics. I used the team wide data to analyze how strongly related a team's total performance in areas such as points per game (PPG) and assists per game (APG) was to its number of wins/rating. I used the player data to find any relationship between a team having 'star' players and a team's number of wins/rating  (The definition of what I decided is a 'star' player is explained below in the Process section) 

 # Process

I downloaded the team wide data from <https://www.basketball-reference.com/>. For each NBA season, there were 4 tables I was interesed in: team per game stats, opponent per game stats, miscellaneous per game stats, and advanced player stats. 

1. I downloaded the first 3 tables for each season going back to the 1998-1999 season as csv files, and then converted the csv files into pandas DataFrames. 
2. I used a web scraper to extract the advanced player statistics going back to the 1998-1999 season. 
3. After cleaning the data, I filtered the advanced player data so that only the 'star' players  remained in the DataFrame 
    1. I defined a 'star' player using the VORP (value over replacement player) statistic that takes into account many measurable player stats (such as points per game, assists per game, minutes per game) to give an estimate of how much value a player a contributes to his team. 
    2. I filtered the data so that players in the top 95% of the VORP statistic of all players over 20 years remained. 
    3. I then grouped the players together by team and year, adding up the stats of players who were from the same team and year. 
4. Finally, I combined both the player and team data by team and year, and explored the relationships and trends in the data that are more thouroughly explained in the project final.ipynb file. 

# Installing and Running the Project

* Clone this repo to your computer
* Move the data files outside of the ` team_data` folder and into the main project folder
    * `miscStats__.csv` = miscellaneous stats per game
    * `oTeamPG__.csv` = opponent stats per game
    * `teamPG__.csv` = team stats per game
* Install the requirements using ` pip install -r requirements.txt `
* Run ` jupyter notebook `, and navigate to and run the ` project final.ipynb ` file within the notebook

