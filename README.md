# Off-Ball Movement and Attacking Threat

> Understanding how off-ball movement creates attacking threat using tracking-derived data.

## Overview

This project explores how off-ball runs contribute to attacking threat in football.

Rather than focusing only on actions on the ball, the aim is to understand how players create value through movement — where they run, when they run, and how those runs influence attacking situations.

The analysis is based on SkillCorner open data, using off-ball run events and xThreat as a measure of attacking value.

---

## Key Insights

- Not all off-ball runs contribute equally to attacking threat  
- Box-attacking movements (e.g. cross-receiver runs) generate the highest value  
- More frequent runs (e.g. support runs) are less directly linked to danger  
- Runs are significantly more effective during transitions and quick breaks  
- Off-ball movement consistently progresses play into high-value central areas in the final third  

---

## Example Visuals

### Run Starting Locations
Most runs begin in structured attacking areas just beyond the halfway line.
![Run Start Heatmap](images/run_start_heatmap.png)

### Run Ending Locations
Runs consistently finish in central final-third zones, where attacking threat is highest.
![Run End Heatmap](images/run_end_heatmap.png)

---

## Approach

The project follows a simple, structured workflow:

- Classify off-ball runs into different movement types  
- Measure their attacking value using xThreat  
- Compare frequency vs effectiveness  
- Analyse runs across different phases of play  
- Build player-level profiles (per90 metrics)  
- Study spatial patterns (start and end locations)  
- Use a simple regression model to understand what drives run value  

---

## Spatial Insight

A clear movement pattern emerges:

- **Runs typically start in structured attacking areas**  
  (~0 to 20 metres in the attacking half)

- **Runs most often end in high-value zones**  
  (~30 to 50 metres, especially in central areas in front of goal)

This shows how off-ball movement helps turn possession into real attacking threat.

---

## Modelling Run Value

A regression model was used to understand what makes a run dangerous.

Key findings:

- Cross-receiver runs are the most effective in generating threat  
- Runs during quick breaks and transitions are significantly more dangerous  
- The value of a run depends on both the type of movement and the game context  

---

## Results Summary

The analysis shows that off-ball movement creates value in different ways.

Box-attacking runs are the most directly dangerous, especially when they occur in fast attacking phases such as transitions and quick breaks. In contrast, support movements happen more often but are less directly linked to immediate attacking threat.

From a spatial perspective, runs tend to begin in organised attacking positions and finish in more dangerous areas closer to goal. This highlights how movement helps progress attacks into high-value zones.

Overall, the effectiveness of a run is not just about how often it happens, but about where it happens and when it happens.

---

## Project Structure

- `01_data_preparation.ipynb` → data loading and preprocessing  
- `02_off_ball_movement_analysis.ipynb` → full analysis, visualisations, and results  

---

## Data

- SkillCorner Open Data (broadcast tracking-derived events)  
- Off-ball run events  
- xThreat values  

---

## Practical Applications

This type of analysis can support decision-making in several ways.

From a recruitment perspective, it can help identify players who generate attacking threat through movement, not just through actions on the ball. This is particularly useful for profiling forwards and wide players who contribute through positioning and timing of runs.

From a tactical perspective, it can highlight which types of runs are most effective in different phases of play. For example, teams may benefit from encouraging more box-attacking movements during transition phases, where space is greater.

It can also support player development by identifying whether a player relies more on volume of runs or on high-impact movements, helping coaches tailor training and decision-making.

Overall, this approach provides a more complete understanding of attacking contribution beyond traditional metrics.

---

## Limitations

- Does not include full defensive context (e.g. pressure, positioning)  
- xThreat captures attacking value but not all tactical impact  
- Run classifications simplify complex in-game movements  
- Analysis focuses on general patterns rather than team-specific tactics  

---

## Why This Matters

Off-ball movement is a key part of attacking play, but it is often overlooked.

This project shows that combining movement, space, and context can provide deeper insight into how teams create chances — and how players contribute beyond actions on the ball.

---

## Author

Yiannis — MSc Football Data Analytics

  
