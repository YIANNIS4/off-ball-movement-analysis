# Off-Ball Movement and Attacking Threat

Understanding how off-ball movement contributes to attacking threat using tracking-derived data.

---

## Project Summary

In this project, I analysed off-ball movement using tracking-derived data to understand which types of runs generate attacking threat.

By linking movement patterns to xThreat values, I explored how players create danger without touching the ball.

The results show that not all runs are equally valuable, with movements attacking the penalty area having a significantly higher impact on attacking outcomes.

---

## Highlights

- Approximately 5,000 off-ball runs analysed  
- Multiple run types identified and compared  
- xThreat used to evaluate attacking value  
- Analysis across different phases of play  
- Player profiling using per 90 metrics  

---

**Tools:** Python, pandas, matplotlib, SkillCorner Open Data

---

## Overview

Most football analysis focuses on actions on the ball such as passes and shots. However, many attacking situations are created before the ball is played, through movement that disrupts defensive structure.

The aim of this project is to understand how players create value through movement, where they run, when they run, and how those runs influence attacking situations.

The analysis is based on SkillCorner open data from the A-League, using off-ball run events and xThreat as a measure of attacking value.

---

## Problem

Traditional football analysis focuses heavily on on-ball actions.

Off-ball movement, although essential in creating space and attacking opportunities, is harder to quantify and is often under-analysed.

This project addresses that gap by evaluating how different types of off-ball runs contribute to attacking threat.

---

## Key Insights

- Cross-receiver runs are the most dangerous movement, generating approximately 0.108 xThreat per run, more than five times higher than support movements (~0.018)

- Runs in behind are the most valuable non-crossing movement, producing approximately 0.051 xThreat per run, more than two and a half times the value of support or overlap runs

- Transition phases create the highest value, with cross-receiver runs during transitions reaching approximately 0.155 xThreat per run

- There is a clear trade-off between frequency and effectiveness, high-volume movements contribute less directly to attacking threat

- Attacking players, particularly centre forwards and wide players, generate the highest total threat through repeated high-value movements, with players such as G. May and N. Botić standing out

This shows that the value of a run is not defined by how often it happens, but by when, where, and how it is executed.

---

## Example Visuals

### Run Value by Type  
![Run Value](images/run_value_by_type.png)

Cross-receiver runs clearly stand out as the most dangerous movement, generating significantly higher attacking threat than all other run types. In contrast, support and build-up movements are more frequent but contribute less directly to dangerous situations.

---

### Run Starting Locations  
![Run Start Heatmap](images/run_start_heatmap.png)

Most runs originate in structured attacking areas just beyond the halfway line, where teams are organised in possession and looking to progress play.

---

### Run Ending Locations  
![Run End Heatmap](images/run_end_heatmap.png)

Runs consistently finish in central final-third zones, directly in front of goal. This highlights how movement helps transform controlled possession into dangerous attacking positions.

---

## Approach

The project follows a structured workflow:

- Classify off-ball runs into different movement types  
- Measure attacking value using xThreat  
- Compare frequency and effectiveness  
- Analyse runs across different phases of play  
- Build player-level profiles using per 90 metrics  
- Study spatial patterns through start and end locations  
- Apply a regression model to understand what drives run value  

---

## Spatial Insight

A clear pattern emerges from the data.

Runs typically start in organised attacking areas and end closer to goal in central, high-value zones. This reflects how teams use movement to progress play into more dangerous positions.

---

## Modelling Run Value

A regression model was used to explore what makes a run more dangerous.

The results show that both the type of movement and the phase of play influence the value of a run. Movements that attack the defensive line, especially during transitions, are significantly more effective.

---

## Results Summary

Off-ball movement contributes to attacking threat in different ways depending on context.

Runs that attack the penalty area are the most directly dangerous, particularly during fast attacking phases such as transitions. In contrast, support movements are more frequent but less directly linked to immediate threat.

From a spatial perspective, movement helps progress attacks from structured areas into more dangerous zones closer to goal.

Overall, effectiveness is not determined by volume, but by timing, location, and intent.

---

## Player Insight

A. Goodwin records one of the highest attacking outputs in the dataset, with approximately 3.20 xThreat per 90.

This shows that efficient movement can generate high attacking value even without a high volume of runs, highlighting the importance of movement quality.

---

## Project Structure

- [01_data_preparation.ipynb](01_data_preparation.ipynb) - loads the SkillCorner open data, extracts off-ball run events, and prepares the dataset  
- [02_off_ball_movement_analysis.ipynb](02_off_ball_movement_analysis.ipynb) - includes run-type analysis, player profiling, spatial analysis, and modelling  

---

## Data

- SkillCorner Open Data, tracking-derived event dataset  
- Competition, A-League sample matches  
- Approximately 5,000 off-ball runs analysed  
- xThreat used as the main measure of attacking value  

Built using Python, pandas, and matplotlib, working with SkillCorner open data.

---

## Practical Applications

This type of analysis can support decision-making in several areas.

From a recruitment perspective, it helps identify players who generate attacking threat through movement, not only through actions on the ball.

From a tactical perspective, it highlights which types of runs are most effective in different phases of play, helping teams optimise attacking patterns.

It can also support player development by identifying whether a player relies more on volume of runs or on high-impact movements.

Overall, this approach provides a more complete understanding of attacking contribution beyond traditional metrics.

---

## Limitations

- Does not include full defensive context such as pressure or positioning  
- xThreat captures attacking value but not all tactical impact  
- Run classifications simplify complex in-game movements  
- Analysis focuses on general patterns rather than team-specific tactics  

---

## Why This Matters

Off-ball movement plays a key role in creating attacking opportunities but is often overlooked in traditional analysis.

By combining movement, space, and context, this project provides a clearer understanding of how players contribute to attacking play without touching the ball.

---

## Final Takeaway

Not all movement is equal. The most effective players are those who combine timing, space, and intent to create real attacking value.

---

## What I Learned

- How to extract tactical insight from tracking-derived events  
- How different run types contribute to attacking value  
- How to link movement patterns to xThreat  
- How to communicate analytical findings clearly

---

## Author

Yiannis  
MSc Football Data Analytics
