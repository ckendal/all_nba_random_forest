# all_nba_random_forest
Using Random Forests to predict All-NBA teams

# README

Author: Chris Kendall, www.chriskdata.com, Twitter: @ChrisKdata

Data source: www.basketball-reference.com

Tools: Jupyter Notebook, Python 3.6 (Pandas, Numpy, sklearn, matplotlib)

### Data Dictionary:
Columns in dataset "nba_1989_thru_2018.csv":
- **All_NBA**: (Float) Multiclass labels (0.0, 1.0 , 2.0, 3.0) (0.0 indicates no All-NBA team, (1.0, 2.0, 3.0) refer to 1st, 2nd, 3rd All-NBA teams)
- **Player**: (String) Concatenated string of player name and unique identifier used by Basketball-Reference.
- **Pos**: (Integer) Basketball player positions numerically enconded. (1: Point Guard, 2: Shooting Guard, 3: Small Forward, 4: Power Forward, 5: Center)
- **Age**: (Integer) Age of player as of February 1st of that season.
- **Tm**: (String) Abbreviation for player's team. ("TOT" is used to indicate total stats for a player that changed teams in-season).
- **G**: (Integer) Number of games the player participated in.
- **GS**: (Integer) Number of games started by the player.
- **MP/G**: (Float) Average minutes played per game by player throughout the season.
- **FG**: (Float) Field goals made per game.
- **FGA**: (Float) Field goal attempts per game.
- **3P**: (Float) 3-point shots made per game.
- **3PA**: (Float) 3-point shot attempts per game.
- **2P**: (Float) 2-point shots made per game.
- **2PA**: (Float) 2-point shot attempts made per game.
- **eFG%**: (Float) Effective Field Goal Percentage (Weighted field goal percentage that accounts for 3-point field goals being worth more than 2-point field goals).
- **FT**: (Float) Free throws made per game.
- **FTA**: (Float) Free throw attempts per game.
- **ORB**: (Float) Offensive rebounds per game.
- **DRB**: (Float) Defensive rebounds per game.
- **TRB**: (Float) Total rebounds per game.
- **AST**: (Float) Assists per game.
- **STL**: (Float) Steals per game.
- **BLK**: (Float) Blocks per game.
- **TOV**: (Float) Turnovers per game.
- **PF**: (Float) Personal fouls committed per game.
- **PS/G**: (Float) Points scored per game.
- **Year**: (Integer) Year in which the NBA season ended. (i.e. *2018* refers to 2017-18 NBA season)
- **MP_season**: (Integer) Total minutes played throughout the season.
- **PER**: (Float) Hollinger's Player Efficiency Rating. A measure of per-minute production, standardized so that the league average is 15.
- **TS%**: (Float) Measure of shot efficiency that accounts for Free Throw, 2-point field goals, and 3-point field goals.
- **3PAr**: (Float) 3-Point Attempt Rate, percentage of field goal attempts that were from 3-point range.
- **FTr**: (Float) Number of free throw attempts per field goal attempt.
- **ORB%**: (Float) Offensive Rebound Percentage, an estimate of the percentage of available offensive rebounds the player made while on the floor.
- **DRB%**: (Float) Defensive Rebound Percentage, an estimate of the percentage of available defensive rebounds the player made while on the floor.
- **TRB%**: (Float) Total Rebound Percentage, an estimate of the percentage of all available rebounds the player made while on the floor.
- **AST%**: (Float) Percentage of teammate field goals the player assisted on.
- **STL%**: (Float) Percentage of opponent possessions ended by a steal while the player was on the floor.
- **BLK%**: (Float) Percentage of oppenent 2-point field goal attempts blocked by the player while on the floor.
- **TOV%**: (Float) Turnover Percentage, an estimate of turnovers made per 100 possessions.
- **USG%**: (Float) Estimate of the percentage of team plays used by player while on the floor. 
- **OWS**: (Float) Offensive Win Shares, estimated number of wins contributed by the player's offense.
- **DWS**: (Float) Defensive Win Shares, estimated number of wins contributed by the player's defense.
- **WS**: (Float) Total Win Shares, estimated number of wins contributed by the player.
- **WS/48**:  (Float) Estimated number of wins contributed by player per 48 minutes (league average is approx. 0.100)
- **OBPM**: (Float) Offensive Box Plus Minus, box score estimate of the offensive points per 100 possessions a player contributed above a league-average player, translated to an average team.
- **DBPM**: (Float) Defensive Box Plus Minus, box score estimate of the defensive points per 100 possessions a player contributed above a league-average player, translated to an average team.
- **BPM**: (Float) Box Plus Minus, box score estimate of the points per 100 possessions a player contributed above a league-average player, translated to an average team.
- **VORP**: (Float) Value Over Replacement Player, a box score estimate of the points per 100 team possessions that a player contributed about a replacement-level (-2.0) player, translated to an average team and prorated to an 82-game season. (Multiply by 2.70 to calculate Wins Over Replacement Player.

