# Data

## Source

**Super Bowl Game Results** — [Kaggle](https://www.kaggle.com/datasets/thedevastator/super-bowl-game-results/), compiled from publicly available NFL statistics, broadcast network records, and media rating organizations. Collected annually after each Super Bowl, from Super Bowl I (1967) through Super Bowl LII (2018).

| File | Description |
|------|-------------|
| `super-bowl-dataset-1.csv` | 52 games × 19 variables: game outcomes, viewership, ratings, and the cost of a 30-second advertisement. Primary dataset for the analysis. |
| `super-bowl-dataset-2.csv` | Game results with MVP and stadium/location details. Used in the project proposal. |

## Data Dictionary

### Dataset 1: `super-bowl-dataset-1.csv`

- `Game`: Number assigned to each Super Bowl game.
- `Date`: Date on which the Super Bowl game took place.
- `Winning.team`: Name of the team that won the game.
- `Winning.Team.Points`: Points scored by the winning team.
- `Winning.Team.Conference`: Conference of the winning team.
- `Score`: Final score showing points for both teams.
- `Losing.team`: Name of the team that lost the game.
- `Losing.Team.Points`: Points scored by the losing team.
- `Losing.Team.Conference`: Conference of the losing team.
- `Venue`: Location where the game was held.
- `City`: City where the game was held.
- `Attendance`: Number of people attending the game.
- `Network`: Television network that broadcast the game.
- `Average.U.S..Viewers`: Average number of viewers in the U.S. who watched the game.
- `Rating`: TV rating showing percentage of households with TVs tuned in.
- `Share`: Share of viewers tuned in among households watching TV.
- `Cost.Per.30s.Ad`: Cost of a 30-second advertisement during the game.
- `Notes`: Additional details or interesting facts about the game.

### Dataset 2: `super-bowl-dataset-2.csv`

- `Date`: The date the Super Bowl was played (month, day, year).
- `SB`: The Super Bowl number, in Roman numeral and numeric form.
- `Winner`: The team that won the Super Bowl (categorical, NFL team names).
- `Winner.Pts`: Points scored by the winning team (discrete numerical).
- `Loser`: The team that lost the Super Bowl (categorical, NFL team names).
- `Loser.Pts`: Points scored by the losing team (discrete numerical).
- `MVP`: The player awarded Most Valuable Player for the game (categorical, player names).
- `Stadium`: The name of the stadium where the Super Bowl was played (categorical).
- `City`: The city in which the stadium is located (categorical).
- `State`: The U.S. state where the Super Bowl was played (categorical).
