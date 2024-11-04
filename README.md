Travis Scott Burger Fantasy League 2025
================

### Contents

- [Team Standings](#team-standings)
- [Points Scored per Game](#points-scored-per-game)
- [Points Against per Game](#points-against-per-game)
- [Points Scored and Against](#points-scored-and-against)
- [Optimal Lineup Setting](#optimal-lineup-setting)
- [Season Long Optimal Lineups](#season-long-optimal-lineups)
- [Most Points Scored in a Loss](#most-points-scored-in-a-loss)
- [Fewest Points Scored in a
  Victory](#fewest-points-scored-in-a-victory)
- [Weekly Scoring Trends](#weekly-scoring-trends)
- [Close Games](#close-games)
- [Highest Scoring Games](#highest-scoring-games)
- [Biggest Blowouts](#biggest-blowouts)
- [Closest Games](#closest-games)
- [Most Points Scored by One Team](#most-points-scored-by-one-team)
- [Fewest Points Scored by One Team](#fewest-points-scored-by-one-team)
- [Past Week One Player Merchants](#past-week-one-player-merchants)
- [Full Season One Player Merchants](#full-season-one-player-merchants)
- [Luckiest Teams This Past Week](#luckiest-teams-this-past-week)
- [Luckiest Teams Season Long](#luckiest-teams-season-long)
- [Self Luck and Opponent Luck](#self-luck-and-opponent-luck)
- [Average Weekly Finishing
  Position](#average-weekly-finishing-position)
- [Chug Analysis](#chug-analysis)
- [Win Percentage by Strength of
  Schedule](#win-percentage-by-strength-of-schedule)
- [League Wide Optimal Scoring](#league-wide-optimal-scoring)

------------------------------------------------------------------------

### Team Standings

![](README_files/figure-gfm/unnamed-chunk-2-1.png)<!-- -->

------------------------------------------------------------------------

### Points Scored per Game

![](README_files/figure-gfm/unnamed-chunk-3-1.png)<!-- -->

------------------------------------------------------------------------

### Points Against per Game

![](README_files/figure-gfm/unnamed-chunk-4-1.png)<!-- -->

------------------------------------------------------------------------

### Points Scored and Against

![](README_files/figure-gfm/unnamed-chunk-5-1.png)<!-- -->

------------------------------------------------------------------------

### Optimal Lineup Setting

![](README_files/figure-gfm/unnamed-chunk-6-1.png)<!-- -->

------------------------------------------------------------------------

### Season Long Optimal Lineups

![](README_files/figure-gfm/unnamed-chunk-7-1.png)<!-- -->

------------------------------------------------------------------------

### Most Points Scored in a Loss

- Week 3: JP def. Adam 136.12-122.98
- Week 8: Chad def. JP 136.84-122.03
- Week 8: Jeremiah def. Adam 131.87-121.79
- Week 6: David def. Hank 143.83-120.26
- Week 4: JP def. Andrew 162.54-118.23

------------------------------------------------------------------------

### Fewest Points Scored in a Victory

- Week 4: Adam def. Eric 72.44-70.28
- Week 8: Andrew def. Matthew 90.23-82.87
- Week 1: Eric def. Andrew 91.4-68.57
- Week 7: Chad def. Eric 91.6-62.28
- Week 6: Jeremiah def. Eric 97.64-62.4

------------------------------------------------------------------------

### Weekly Scoring Trends

![](README_files/figure-gfm/unnamed-chunk-10-1.png)<!-- -->

------------------------------------------------------------------------

### Close Games

![](README_files/figure-gfm/unnamed-chunk-11-1.png)<!-- -->

------------------------------------------------------------------------

### Highest Scoring Games

- Week 4: JP def. Andrew 162.54-118.23
- Week 5: Adam def. David 165.1-111.25
- Week 6: David def. Hank 143.83-120.26
- Week 3: JP def. Adam 136.12-122.98
- Week 8: Chad def. JP 136.84-122.03

------------------------------------------------------------------------

### Biggest Blowouts

------------------------------------------------------------------------

- Week 5: Love Hurts def. Orthopedics PreOp 143.83-80.98
- Week 6: DSM-5 All Stars def. Orthopedics PreOp 137.75-76.64
- Week 2: cArOLinA pAntHErS def. Dakshots 137.81-82.82
- Week 5: Hank’s Ass def. Shock Squad 165.1-111.25
- Week 6: Hank’s Ass def. Bearly Alive 142.83-91.58

### Closest Games

- Week 3: Dakshots def. Love Hurts 98.13-98.11
- Week 4: Hank’s Ass def. Dakshots 72.44-70.28
- Week 3: Orthopedics PreOp def. Tua’s Brain Scan 103.08-99.47
- Week 3: Bearly Alive def. Shock Squad 97.73-93.26
- Week 4: DSM-5 All Stars def. Love Hurts 107.04-102.47

------------------------------------------------------------------------

### Most Points Scored by One Team

- 165.1 (Adam, Week 5)
- 162.54 (JP, Week 4)
- 148.92 (Jeremiah, Week 7)
- 147.4 (Hank, Week 8)
- 143.83 (Hank, Week 5)

------------------------------------------------------------------------

### Fewest Points Scored by One Team

- 62.28 (Eric, Week 7)
- 62.4 (Eric, Week 6)
- 68.57 (Andrew, Week 1)
- 70.28 (Eric, Week 4)
- 72.44 (Adam, Week 4)

------------------------------------------------------------------------

### Past Week One Player Merchants

- De’Von Achane: 26.3% of total points for Andrew
- CeeDee Lamb: 25.1% of total points for Jeremiah
- James Cook: 24.5% of total points for Eric
- Kyler Murray: 23.1% of total points for Matthew
- Jalen Hurts: 22.2% of total points for Hank

------------------------------------------------------------------------

### Full Season One Player Merchants

- Lamar Jackson: 18.67% of total points for Adam
- Baker Mayfield: 17.13% of total points for Jeremiah
- Derrick Henry: 16.99% of total points for JP
- James Cook: 16.98% of total points for Eric
- Kyler Murray: 15.26% of total points for Matthew

------------------------------------------------------------------------

### Luckiest Teams This Past Week

![](README_files/figure-gfm/unnamed-chunk-19-1.png)<!-- -->

------------------------------------------------------------------------

### Luckiest Teams Season Long

![](README_files/figure-gfm/unnamed-chunk-20-1.png)<!-- -->

------------------------------------------------------------------------

### Self Luck and Opponent Luck

![](README_files/figure-gfm/unnamed-chunk-21-1.png)<!-- -->

------------------------------------------------------------------------

### Average Weekly Finishing Position

![](README_files/figure-gfm/unnamed-chunk-22-1.png)<!-- -->

For example: if Hank had the best score in the league, the third best
score in the league, and the second best score in the league through
three weeks, his average weekly finishing position would be (1 + 3 + 2)
/ 3 = 2. Closely related to points per game, but not the exact same.

------------------------------------------------------------------------

### Chug Analysis

![](README_files/figure-gfm/unnamed-chunk-23-1.png)<!-- -->

------------------------------------------------------------------------

### Win Percentage by Strength of Schedule

``` r
get_opp_proj_scores = function(tm) {
  w = end_with_proj |> filter(win_team == tm) |> pull(lose_proj_score)
  l = end_with_proj |> filter(lose_team == tm) |> pull(win_proj_score)
  return(round(mean(c(w, l)), 2))
}

data.frame(team = all_teams) |>
  mutate(sos = sapply(team, get_opp_proj_scores)) |>
  inner_join(team_records, by = "team") |>
  ggplot(aes(sos, win_pct)) +
  geom_text(aes(label = first), size = 4) +
  geom_line(stat = "smooth", formula = y ~ x, method = "lm", linetype = "dashed")
```

![](README_files/figure-gfm/unnamed-chunk-24-1.png)<!-- -->

------------------------------------------------------------------------

### League Wide Optimal Scoring

![](README_files/figure-gfm/unnamed-chunk-25-1.png)<!-- -->

------------------------------------------------------------------------
