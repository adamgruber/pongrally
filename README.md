# pongrally

PongRally is the successor to [Pongy][]. It is a full fledged application for managing Players, Teams, and Matches.

## Tech

### Front End

The following solutions are being considered:

- React
- React Router
- Redux
- Styles (styled-components / cssnext / sass ?)
- Webpack

### Backend

The following solutions are being considered:

- koa server
- GraphQL
- SQL Database (Postgres?)

## Models

### Player (User)

A player has
  - a unique username (login)
  - a password
  - a real name made up of first and last name
  - a paddle hand
  - a cumulative rating
  - an avatar

A player can belong to one or more teams

### Team

A team has
  - a unique name
  - a list of Matches played
  - a unique list of Players on the team (one or two)

Single-player teams have a ranking among other single-player teams

Doubles teams have a ranking among other doubles teams

A team has stats consisting of
  - total number of wins
  - total number of losses
  - current win streak
  - best win streak
  - performance versus other teams
    - matches won when serving
    - matches won when receiving
    - matches lost when serving
    - matches lost when receiving
    - total points won when serving
    - total points lost when receiving    

### Match

A match has
  - an initial serving Team
  - an initial receiving Team
  - a score
  - a winning Team
  - a losing Team
  - a status (active, finished)

A match has stats consisting of
  - total points scored
  - duration of play

### Tournament (Future Consideration)

A tournament has
  - a list of matches
  - a winning Team
  - current standings

## Views / Screens

### Dashboard

The default view when there are no active matches

The dashboard shows
  - a running list of previous matches
  - player rankings

### Scoreboard

A view of the active match showing
  - names of teams playing
  - player names, avatars, and basic stats
  - current score
  - current game state (deuce?)
  - game clock

The scoreboard *may* have a secondary view showing
  - running list of previous matches

### Player Profile

A view showing player information and stats

### Team Profile

A view showing team information and stats

### Login / Signup

A view with fields for new player signup or existing player login

[Pongy]: https://github.com/adamgruber/pongy