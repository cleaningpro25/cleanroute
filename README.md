# CleanRoute Utah - Scheduling Assistant

A scheduling tool for a cleaning business operating two teams across Salt Lake County and Utah County, Utah.

## What It Does

Helps dispatchers find the best day, time, and route for new cleaning appointments by analyzing the existing schedule and optimizing for proximity and capacity.

### How It Works

1. Paste a client address or type a city name
2. Select hours of cleaning and recurrence (weekly, bi-weekly, monthly)
3. Optionally pick a preferred day
4. Hit **Search Best Schedule**
5. Review the top 3 options ranked by proximity score, capacity, and conflict status

### Features

- **Smart scheduling engine** scans the next 60 days and accounts for weekly, bi-weekly, and monthly recurrence patterns to find gaps
- **Google Maps integration** with real driving routes and distance/time between stops
- **Recurring date preview** shows the next 2 months of scheduled dates with conflict indicators per date
- **Capacity rules enforced automatically:**
  - Team Utah (Utah County): Monday-Friday, max 2 appointments per day
  - Team Salt Lake (Salt Lake County): Monday-Saturday, max 3 per day, max 1 on Saturday
- **Conflict detection** warns when a new recurring appointment overlaps with an existing one
- **Address parsing** extracts city from full addresses and zip codes

### Schedule Data

The app loads with schedule data exported from ZenMaid. Data persists in your browser's localStorage. Click **Reset** to reload the original dataset.

## Setup

No build step. One HTML file. Open `index.html` in a browser or deploy to GitHub Pages.

### GitHub Pages

1. Push this repo
2. Go to Settings > Pages
3. Set source to **main** branch, **/ (root)**
4. Site goes live at `https://yourusername.github.io/cleanroute/`

## Tech Stack

- Vanilla JavaScript (no frameworks)
- Google Maps JavaScript API + Directions API
- localStorage for data persistence
