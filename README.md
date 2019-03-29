# MLB API DATA
#### Endpoints to get MLB.com API data

The MLB.com API is quite an illusive thing. This data should help you get to some common end points.

## New API Data

### Games scheduled for today

`http://statsapi.mlb.com/api/v1/schedule/games/?sportId=1`

### Games scheduled for particular days

#### Full season schedule
`http://statsapi.mlb.com/api/v1/schedule/games/?sportId=1&startDate=2019-03-28&endDate=2019-09-29`

#### One Month
`http://statsapi.mlb.com/api/v1/schedule/games/?sportId=1&startDate=2019-06-01&endDate=2019-06-30`


## Old API Data

There is a message in the JSON data that this URL is deprecated but you can access game and social media data through this directory:

`http://gdx.mlb.com/components/game/mlb/`


### Gameday Scoreboard (all games for a date)

`http://gdx.mlb.com/components/game/mlb/year_2019/month_03/day_28/master_scoreboard.json`


### Gameday Mini Scoreboard (all games for a date)

`http://gdx.mlb.com/components/game/mlb/year_2019/month_03/day_28/miniscoreboard.json`


### Data options for specific game matchups (by date)

`http://gdx.mlb.com/components/game/mlb/year_2019/month_03/day_28`

In this directory, you'll see the matchups for the day in the URL above. Click into those individual matchups and get more options for game-specific data including, lineups, box scores, plays, event logs, and more.


### Team-specific Insider tweets

`http://gdx.mlb.com/components/game/mlb/twitter/`

Get Atlanta Braves Insider tweets:
`http://gdx.mlb.com/components/game/mlb/twitter/atlInsiderTweets.json`


### Official team tweets

`http://gdx.mlb.com/components/game/mlb/twitter/teams`

Get Atlanta Braves official tweets:
`http://gdx.mlb.com/components/game/mlb/twitter/teams/BravesTweets.json`


### MLB Fan Cave tweets

`http://gdx.mlb.com/components/game/mlb/twitter/fanCave/`


### MLB Sports on Earth tweets

`http://gdx.mlb.com/components/game/mlb/twitter/sportsonearth/`
