# Spotify Listening Behavior Analysis Dashboard

## Overview
This project is a Power BI dashboard built using my Spotify listening history from my Spotify account data export (JSON). I created this as an end-of-year project inspired by Spotify Wrapped, but instead of just looking at static yearly summaries, I wanted something I could freely explore, filter, and analyze in more detail.

The dashboard summarizes listening activity from 2021 to 2025. It focuses on what I listen to, when I usually listen, and how my listening behavior changes through time. More than just visuals, this project was a way to practice the complete workflow behind data visualization: preparing data, shaping it into a usable model, designing charts, building meaningful interactions, and documenting the process.

A more detailed narrative write-up with background, motivation, reflections, design decisions, limitations, and future improvement plans is included in the `docs/Project Background.pdf`.

---

## What this dashboard tries to answer

### Listening Behavior and Trends
- How has my listening changed from 2021 to 2025?
- Which months record the highest listening activity?
- What periods stand out the most?
- How much time do I actually spend listening overall?

### Artists, Albums, and Tracks
- Who do I listen to the most?
- Which albums receive the most listening time?
- What are my top songs?
- Is my listening concentrated around a few artists, or spread across many?

### Habits and Patterns
- Which days do I usually listen the most?
- What time of day do I normally listen?
- Do I usually listen in short sessions or long sessions?
- How different are weekdays and weekends?

Across the report, charts include **customized tooltips** that provide extra context when hovered, such as shares, additional metrics, and information that is not shown directly on the visual. This makes the dashboard easier to understand without overcrowding the visuals.

---

## Report Pages

### 1) Overview Page
This page provides a quick but meaningful summary of listening behavior.

It includes:
- total listening minutes, total streams, active days, and distinct artists
- a clickable month-by-month trend line that lets you explore peak periods
- top artists, top albums, and top tracks ranked by listening time
- an interaction flow where selecting an artist updates album and song views

The page is designed so that someone unfamiliar with the data can immediately see the big picture, then drill deeper by clicking months, artists, or visuals. Customized tooltips on this page help explain peaks, shares, and key drivers behind totals.

<img width="1407" height="791" alt="01 Overview Page - Spotify Dashboard" src="https://github.com/user-attachments/assets/7f001327-84c3-4c45-b57c-cecd21af9a08" />


### 2) Patterns Page
This page focuses on listening habits rather than totals.

It includes:
- a heatmap showing minutes played by day of week and hour of day
- a chart showing which days have the highest listening totals
- a chart showing what time of day I usually listen
- a daily listening distribution (minute buckets) showing how many days fall into each listening range

This page helps reveal routine behavior, such as peak evening times or certain days that consistently dominate listening time. The tooltips on this page provide additional insight such as contribution shares and supporting details that are not directly visible in the charts.

<img width="1411" height="791" alt="02 Patterns Page - Spotify Dashboard" src="https://github.com/user-attachments/assets/45ea4894-188c-43ac-98d1-e8480a45d6a2" />
---

## Repository Contents
- `powerbi/`  
  Contains the Power BI report file (`.pbix`).

- `docs/Project Background.pdf`  
  Full background, motivation, reflections, design discussion, limitations, and planned improvements.

- `docs/etl_notes.md`  
  Summary of Power Query data preparation, transformation steps, cleaning logic, and derived fields.

- `docs/data_dictionary.md`  
  Definitions of key fields used in the model.

- `docs/measures_catalog.md`  
  List of key DAX measures with explanations of what each one represents.

- `docs/dashboard_guide.md`  
  Simple guide on how to navigate, filter, and interact with the dashboard.

- `CHANGELOG.md`  
  Notes on project updates and revisions during development.

---

## Data Source and Scope
- **Source:** Spotify “Your Data” export (JSON)
- **Coverage:** 2021 to 2025, based on data available in the export
- **Unit of analysis:** each record represents a playback event recorded in Spotify’s export
- **Privacy:** raw personal Spotify data files are not included in this repository

---

## Using or Refreshing with Your Own Data
If you want to build something similar using your own Spotify export:
1. Download your Spotify account data export (JSON).
2. Place the JSON files in a local `Streaming History Data/` folder.
3. Open the `.pbix` file in `powerbi/`.
4. Update the data source path if Power BI asks.
5. Refresh the report and verify updated totals and date coverage.

---

## Notes
This is a **personal learning and portfolio project**. The goal was to practice end-to-end dashboard creation using real personal data, while also reflecting on what the data actually says about listening habits. More detailed discussion is documented in the accompanying PDF to keep the README readable and focused.


