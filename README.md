# OSHAC Analytics — v0.1.0

Mobile-first independent swim performance dashboard. Four navigation sections (Overview, Swimmers, Progress, Meets) and individual swimmer profiles.

## Data
- `data/swimmers.csv`: OSHAC-specific swimmer IDs, name, training group.
- `data/meets.csv`: OSHAC-specific meet IDs, name, start date, course.
- `data/results.csv`: OSHAC-specific result IDs, swimmer ID, meet ID, event, time in seconds, status.

All identifiers have been remapped to project-specific IDs. **This does not change the provenance of historical data.** The initial historical results were imported from a Hy-Tek export. Maintain this note privately for data accuracy and corrections. Do not claim that imported historical results were manually recorded. New results can be entered manually.

## Run
Open with VS Code Live Server or `python3 -m http.server 8000` in this directory. GitHub Pages also works. Do not double-click the HTML file, since CSV loading requires HTTP.

## Manual entry
From the repository root in RStudio: `source("scripts/enter_results.R")`. Existing swimmer and meet IDs are respected. Do not overwrite CSVs with older copies.

## Dates and accuracy
Seasons run September 1–August 31. Imported results use the meet start date; exact race-day dates for multi-day meets may differ. Course comes from the meet record. Review the club's permissions before publishing named swimmer results.

## Profile chart controls
Use **Career** to show all recorded races for the selected event and course, or **Season** to display only the season selected in the profile filter. The season selector continues to control season summary statistics independently.
