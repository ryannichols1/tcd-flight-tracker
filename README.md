# Flight Tracker

An interactive data-visualisation app for exploring US domestic flight data, built in [Processing](https://processing.org) (Java) as a group project for **CSU11013 Programming Project** at Trinity College Dublin (Group 40, 2026).

Six visualisations, all navigable from a sidebar, with a live search that filters every chart at once. They include:

- Delay by airline
- Busiest departure airports
- Destination map of the US
- Flights by time of day (radial clock chart)
- Flights by day of the week

Search by airline code, airport code, flight number or date range, and every chart rebuilds against the matching subset. Press `0` to reset.

## Running it

1. Install [Processing 4](https://processing.org/download).
2. Open `ProgrammingProject/ProgrammingProject.pde`.
3. Press Run. The sample datasets (2k, 10k and 100k rows, plus the full file) are in `ProgrammingProject/Data/`. The app starts on the smallest one.

## How it's built

A `currentScreen` variable decides which chart's `draw()` runs. Each chart is its own class, so views could be built and tested independently before integration. CSV rows are parsed into `DataPoint` objects, and `rebuildCharts()` reconstructs every chart from the filtered data after each query. The write-up covers the design in more detail: [CS11013-report-40.pdf](CS11013-report-40.pdf).

## Team

Vlad Manea, Ryan Nichols, Callum Hughes, Oliver Crosthwaite, Connor Nel, Sean Moriarty
