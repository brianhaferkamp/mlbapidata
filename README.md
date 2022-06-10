# MLB API DATA
#### Endpoints to get MLB.com API data

The MLB.com API is quite an illusive thing. This should help you get to some commonly used end points.

<br>

## New API Data

This seems to be the newest way to access the API and is suggested by MLB.com.

### Games scheduled for today

`http://statsapi.mlb.com/api/v1/schedule/games/?sportId=1`

<br>

### Games scheduled for particular days

#### Full season schedule
`http://statsapi.mlb.com/api/v1/schedule/games/?sportId=1&startDate=2019-03-28&endDate=2019-09-29`

<br>

### Individual game content

`http://statsapi.mlb.com/api/v1/game/[gameID]/content`

<br>

### MLB and Minor League Ballparks

`http://statsapi.mlb.com/api/v1/venues`

#### Find info for a specific park
`http://statsapi.mlb.com/api/v1/venues/[venueID]`

<br>

### MLB and Minor League Teams

`http://statsapi.mlb.com/api/v1/teams`

#### Find info for a specific team
`http://statsapi.mlb.com/api/v1/teams/[teamID]`

<br>

### Standing information

`https://statsapi.mlb.com/api/v1/standings?leagueId=[leagueID]&season=[season]&date=[date]&standingsTypes=[types]&hydrate=[hydrate]`

**explanation**
- leagueId: which league(s) to show, e.g., `103` is AL and `104` is NL. (`103,104` is available)
- season: which season to show, e.g., `2022`.
- date: which date to show, date is in the format `YYYY-MM-DD`.
- standingsTypes: which types of games to show, e.g., `regularSeason` and `springTraining`, or combine them (`regularSeason,springTraining`).
- hydrate: which information to show in detail, e.g.. `division`, `sport`, `league` and `team` are available. (of course they can be combined as well)

The JSON of this response can be divided into 6 parts, and every part represents a league and a division (e.g., `AL west`), then you can find every team in `teamRecords` in the six parts.

<br>
  
## Old API Data

This is an older way of accessing the API. There is a message in the JSON data that this URL is deprecated but you can access game and social media data through this directory:

`http://gdx.mlb.com/components/game/mlb/`

<br>

### Gameday Scoreboard (all games for a date)

`http://gdx.mlb.com/components/game/mlb/year_2019/month_03/day_28/master_scoreboard.json`

<br>

### Gameday Mini Scoreboard (all games for a date)

`http://gdx.mlb.com/components/game/mlb/year_2019/month_03/day_28/miniscoreboard.json`

<br>

### Data options for specific game matchups (by date)

`http://gdx.mlb.com/components/game/mlb/year_2019/month_03/day_28`

In this directory, you'll see the matchups for the day in the URL above. Click into those individual matchups and get more options for game-specific data including, lineups, box scores, plays, event logs, and more.

<br>

### Team-specific Insider tweets

`http://gdx.mlb.com/components/game/mlb/twitter/`

Get Atlanta Braves Insider tweets:
`http://gdx.mlb.com/components/game/mlb/twitter/atlInsiderTweets.json`

<br>

### Official team tweets

`http://gdx.mlb.com/components/game/mlb/twitter/teams`

Get Atlanta Braves official tweets:
`http://gdx.mlb.com/components/game/mlb/twitter/teams/BravesTweets.json`

<br>

### MLB Fan Cave tweets

`http://gdx.mlb.com/components/game/mlb/twitter/fanCave/`

<br>

### MLB Sports on Earth tweets

`http://gdx.mlb.com/components/game/mlb/twitter/sportsonearth/`
