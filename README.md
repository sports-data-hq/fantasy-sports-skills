# Fantasy and DFS skills for Claude

13 Claude skills for fantasy football, fantasy basketball, baseball and hockey, daily fantasy and Fantasy Premier League. They rank your players from real usage, injuries, depth charts and schedules, and use the market's per-player lines as projections, so every number comes from live data, not a guess.

```
/plugin marketplace add sports-data-hq/fantasy-sports-skills
/plugin install fantasy-sports@sportsdatahq-fantasy
```

Codex: `codex plugin marketplace add sports-data-hq/fantasy-sports-skills`. Any agent that reads skills: `npx skills add sports-data-hq/fantasy-sports-skills`.

The first tool call asks you to sign in to SportsDataHQ: one free account covers every sport here, with 1,000 credits a month and no card. [Create it now](https://app.sportsdatahq.com/signup?utm_source=github&utm_medium=fantasy-repo&utm_campaign=fantasy-sports-skills).

## Skills

| Sport | Skill | What it does |
|---|---|---|
| NFL | `nfl-dfs-lineup` | Build a lineup under the cap from your salary file, from the market's per-player projections |
| NFL | `nfl-fantasy-draft-board` | Tiered draft board with value over replacement from last season, against the ADP you paste |
| NFL | `nfl-fantasy-start-sit` | Rank your players for the week from the market's per-player lines turned into fantasy points, with usage and matchup |
| NFL | `nfl-fantasy-trade-value` | Price both sides of a trade in rest-of-season points above replacement, with games left and byes |
| NFL | `nfl-fantasy-waivers` | Waiver pickups ranked by snap-share trend, touches and depth-chart path, with no bid amounts |
| NBA | `nba-dfs-lineup` | Build a lineup under the cap from your salary file, with fantasy points from the market's per-player lines |
| NBA | `nba-fantasy-streaming` | Who to stream this week: games per team, back-to-backs and recent minutes |
| MLB | `mlb-dfs-stacks` | Stacks and lineups from your salary file, with implied team totals and hitter and pitcher projections |
| MLB | `mlb-fantasy-waivers` | Waiver pickups by playing time over the last two weeks, then quality, with sample-size flags |
| NHL | `nhl-dfs-lineup` | Build a lineup under the cap from your salary file, with line and power-play stacks |
| NHL | `nhl-fantasy-streamers` | Who to stream: games in the window, goalie start share, ice time and power-play role |
| Fantasy Premier League | `soccer-fpl-captain` | FPL captain pick ranked by expected points, with the model's goal chance beside the market's |
| Fantasy Premier League | `soccer-fpl-transfers` | FPL transfers over the next four gameweeks from minutes, xG per 90 and fixtures, with the hit cost |

## How the projections work

- **The market as a projection.** A player's prop line is the market's median for that stat. The skills turn lines into fantasy points with your league's scoring, and show the formula.
- **Usage first.** Snap share, targets, carries, minutes, plate appearances, ice time and power-play role, with the trend, because role changes before results do.
- **Schedules.** Games per team in the window, back-to-backs, and fixture difficulty for FPL.
- **What you paste.** Salaries, ADP, ownership, your league's scoring and FPL prices aren't in the data, so the skills ask for them rather than invent them.
- **Sample sizes on every rate,** and a plain "not enough data" when there isn't.

DFS skills build lineups under the cap from your salary file. They never advise on entries, contests or bankroll. Odds are used only as information.

## Example answers

Real runs on live data: [start/sit](https://github.com/sports-data-hq/sportsdatahq-skills/blob/main/docs/examples/nfl/04-fantasy-should-i-start-bijan-robinson-or-jahmyr-gibbs-this-w.md), [NFL waivers](https://github.com/sports-data-hq/sportsdatahq-skills/blob/main/docs/examples/nfl/05-best-waiver-wire-pickups-this-week-for-fantasy-football.md), [NBA streaming](https://github.com/sports-data-hq/sportsdatahq-skills/blob/main/docs/examples/nba/04-which-players-should-i-stream-this-week-in-fantasy-basketbal.md), [FPL captain](https://github.com/sports-data-hq/sportsdatahq-skills/blob/main/docs/examples/soccer/04-fpl-captain-this-gameweek-haaland-salah-palmer-or-saka-defau.md).

## More

- Every sport's full analysis skills (previews, props research, ratings, models): [sports-data-hq/sportsdatahq-skills](https://github.com/sports-data-hq/sportsdatahq-skills).
- These skills are synced from that repo, so please open issues and pull requests there.

MIT licensed. Data from the SportsDataHQ APIs, used under their terms.
