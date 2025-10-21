# Project Timeline Planner (Gantt Chart)

A modern, interactive web-based Gantt chart and sprint planner designed for agile project teams. Easily visualize, configure, and export your project schedule with comprehensive support for Design, Back-end, and Front-end work streams, custom team capacities, WIP limits, configurable dependencies, and CSV import.

🌐 **[Try it live on GitHub Pages](https://ai-elf.github.io/Gantt/Gantt_Planner.html)**

## Features
- **Interactive Gantt Chart**: Visualize project tasks by sprint with color-coded bars. Design work is shown as a thin track, overlaid on the main bar representing Back-end and Front-end work.
- **Tri-Team Support**: Full support for Design (DES), Back-end (BE), and Front-end (FE) task estimations.
- **Configurable Team Capacity & WIP**: Set global or per-sprint capacities and Work-In-Progress (WIP) limits for all three teams.
- **Flexible Dependencies**: Inter-team dependencies (e.g., BE depends on DES, FE depends on BE) are optional and can be toggled with checkboxes.
- **Dynamic Holiday Planning**: Automatically identifies the sprint overlapping the New Year (Dec 25 - Jan 1) and sets its capacity to zero.
- **Detailed & Basic Modes**: Switch between simple static configuration and a detailed per-sprint configuration view.
- **CSV Import**: Upload tasks in bulk using a simple CSV format with DES, BE, and FE columns.
- **Editable Task Table**: Edit task order and effort directly in the browser's "Data Input" tab.
- **Export Chart**: Download the Gantt chart as a high-quality PNG image.
- **Multiple Data Views**: Includes tabs for raw data input, calculated sprint start/end dates, and a detailed breakdown of work scheduled per sprint.
- **Responsive UI**: Clean, modern design using TailwindCSS.

## Setup & Usage

### Quick Start
🌐 **[Use the live version](https://ai-elf.github.io/Gantt/Gantt_Planner.html)** - No installation required!

### Local Setup
1. **Clone or Download** this repository.
2. **Open `Gantt_Planner.html` in your browser** (no build or server required).

### Sample Data
Ready to test? Try these sample CSV files:
- **[BE&FE_sample_estimations.csv](BE&FE_sample_estimations.csv)** - Backend and Frontend tasks only
- **[BE&FE&Design_sample_estimations.csv](BE&FE&Design_sample_estimations.csv)** - Full tri-team sample with Design, Backend, and Frontend tasks

## How to Use
1. **Import Tasks**:
   - Click "Upload Epics (CSV)" and select a CSV file (see format below).
   - Alternatively, edit tasks directly in the "Data Input" tab. The default tasks provide a sample structure.
2. **Configure Your Project**:
   - Set the project's overall **Start Date**.
   - Adjust the **Start Sprint** for DES, BE, and FE teams to stagger their start if needed.
   - Define team-wide **Capacity** (in story points) and **WIP** (Work-In-Progress) limits.
   - *(Optional)* Switch to the "Detailed Capacity" tab for per-sprint configuration overrides.
3. **Set Dependencies**:
   - Use the checkboxes to define whether dependencies are enforced (e.g., should BE work wait for DES completion?).
4. **Recalculate Plan**:
   - Click "Recalculate Plan" to update the Gantt chart and all data tables with your new configuration. The chart will redraw automatically when dependency checkboxes are changed.
5. **Export**:
   - Click "Download Chart (PNG)" to save the current Gantt chart as an image.

## CSV Format
The CSV file must contain a header row. The columns `Order`, `Title`, `FE`, and `BE` are required. The `DES` column is optional.

```csv
Order,Title,FE,BE,DES
1,Task Name,8,5,2
2,Another Task,13,0,4
...
```
- **Order**: A number used for prioritizing and sorting tasks.
- **Title**: The name of the task or epic.
- **FE**: Front-end effort (e.g., story points). Use 0 if not applicable.
- **BE**: Back-end effort (e.g., story points). Use 0 if not applicable.
- **DES**: Design effort (e.g., story points). Use 0 if not applicable.

## Libraries Used
- [TailwindCSS](https://tailwindcss.com/) (CDN)
- [Chart.js](https://www.chartjs.org/) (CDN)
- [date-fns](https://date-fns.org/) (CDN)
- [PapaParse](https://www.papaparse.com/) (CDN)

## Credits
For questions or improvements, open an issue or PR ;)
