# 🏏 IPL Analytics | Tableau Dashboard (2008–2020)

<img width="100%" alt="IPL Tableau dashboard screenshot" src="https://github.com/user-attachments/assets/7c9927bb-6eaa-409f-8517-6db916150a69" />

**Portfolio case study · Sports analytics · Match data · Ball-by-ball analysis**

## Executive Summary
This project explores Indian Premier League matches from 2008 to 2020 using two levels of data: match-level records and delivery-level ball-by-ball records. Tableau is used to compare team, player, venue, season and match patterns in a visual format.

## Business Problem
Match outcomes alone do not explain how a team performs across seasons or how player contributions vary. Analysts need to compare outcomes with context—such as toss decisions, venues, innings and delivery-level events—while ensuring that measures are calculated at the right level.

This dashboard is intended as a historical exploration tool, not a guaranteed predictor of future matches.

## Data Model & Grain
| Dataset | Grain | Typical use |
|---|---|---|
| `IPL Matches 2008-2020.csv` | One row per match | Winner, season, venue, toss and match outcome |
| `IPL Ball-by-Ball 2008-2020.csv` | One row per delivery | Runs, wickets, batter/bowler and innings-level detail |

**Important modelling point:** joining match-level and delivery-level data expands each match into many delivery rows. Match counts and win counts should be calculated at match grain or with distinct match IDs to avoid double-counting.

## Business Questions
- Which teams have the strongest historical win records across seasons?
- How do outcomes and team performance change by season or venue?
- What patterns appear in toss decisions and match outcomes?
- Which batters and bowlers stand out on the measures included in the workbook?
- How do delivery-level patterns add context to match-level results?

## KPI Framework
| KPI | Suggested definition | Analytical value |
|---|---|---|
| Matches played | Distinct match IDs | Correct denominator for team comparisons |
| Wins / win percentage | Wins ÷ matches played | Historical team performance |
| Toss-to-win rate | Matches won after winning toss ÷ matches where toss was won | Explore association, not causation |
| Runs scored | Sum of runs under a clearly stated run definition | Batting output |
| Wickets taken | Count of valid wicket events using dataset rules | Bowling impact |
| Player contribution | Player-specific runs, wickets or other chosen measure | Compare roles and opportunities |
| Season trend | KPI by season | Understand change over time |

## Insights & Decision Use
- **Team comparisons:** normalise win counts by matches played so teams with more appearances are not automatically favoured.
- **Toss and venue analysis:** compare rates by season and venue; differences can reflect conditions, team strength and selection as well as toss outcome.
- **Player rankings:** compare players using role-appropriate denominators and account for number of matches/balls faced.
- **Historical context:** separate descriptive season patterns from claims about current team strength.

The actual leaderboard values should be taken from the Tableau workbook or a reproducible calculation; this README does not invent rankings.

## Tools & Repository Contents
| File | Purpose |
|---|---|
| `IPL_Analysis.twb` | Tableau workbook |
| `IPL_DASHBOARD.pdf` | Dashboard export |
| `IPL Matches 2008-2020.csv` | Match-level source |
| `IPL Ball-by-Ball 2008-2020.csv` | Delivery-level source |

## How to Explore
1. Inspect both datasets and confirm their date/season range.
2. Open `IPL_Analysis.twb` in Tableau Desktop and reconnect data if required.
3. Review the PDF and dashboard screenshot.
4. Check calculated fields, filters and aggregation levels before interpreting the charts.
5. Confirm match-level KPIs use distinct match identifiers.

## Limitations & Next Steps
- The data ends in 2020 and should not be presented as current-season performance.
- Rule changes and differences in matches played affect comparisons across seasons.
- Clarify whether extras are included in run totals and how wicket types are counted.
- Add a verified findings section with three to five numbers, the denominator, and the decision each finding informs.
- Add player opportunity-adjusted measures and test dashboard filters for double counting.

## Skills Demonstrated
Tableau · Data visualisation · Multi-grain data modelling · Sports KPI design · Historical trend analysis · Analytical storytelling

## Author
**Yazdan Ahmed** · [GitHub Portfolio](https://github.com/YazdanAhmedData)
