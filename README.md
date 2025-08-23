# Project Timeline Planner (Gantt Chart)

A modern, interactive web-based Gantt chart and sprint planner for project teams. Easily visualize, configure, and export your project schedule with support for custom team capacities, WIP limits, and CSV import.

## Features
- **Interactive Gantt Chart**: Visualize project tasks by sprint, with color-coded BE/FE/overlap bars.
- **Configurable Team Capacity & WIP**: Set per-sprint or static capacities and parallel work limits for BE and FE teams.
- **Detailed & Basic Modes**: Switch between simple static config and detailed per-sprint configuration.
- **CSV Import**: Upload tasks in bulk using a simple CSV format.
- **Editable Task Table**: Edit tasks directly in the browser.
- **Export Chart**: Download the Gantt chart as a PNG image.
- **Responsive UI**: Clean, modern design using TailwindCSS.

## Setup & Usage
1. **Clone or Download** this repository.
2. **Open `Gantt/index.html` in your browser** (no build or server required).

## How to Use
1. **Configure Your Project**:
   - Set start date, start sprints, team capacities, and WIP (parallel work) for BE/FE.
   - (Optional) Switch to "Detailed Capacity" tab for per-sprint configuration.
2. **Import Tasks**:
   - Click "Upload Epics (CSV)" and select a CSV file (see format below).
   - Or, edit tasks directly in the Data Input tab.
3. **Recalculate Plan**:
   - Click "Recalculate Plan" to update the chart and tables.
4. **Export**:
   - Click "Download Chart (PNG)" to save the current Gantt chart as an image.

## CSV Format
The CSV should have columns:

```
Order,Title,FE,BE
1,Task Name,8,5
2,Another Task,13,0
...
```
- **Order**: Number (for sorting)
- **Title**: Task name
- **FE**: Frontend effort (story points)
- **BE**: Backend effort (story points)

## Libraries Used
- [TailwindCSS](https://tailwindcss.com/) (CDN)
- [Chart.js](https://www.chartjs.org/) (CDN)
- [date-fns](https://date-fns.org/) (CDN)
- [PapaParse](https://www.papaparse.com/) (CDN)

## Credits
Developed with ❤️. For questions or improvements, open an issue or PR! 