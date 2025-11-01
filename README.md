# CodeQuest-Interactive-Learning-Dashboard

A front-end web application that simulates an interactive coding lesson platform. Users can view coding modules, track progress, unlock lessons, and visualize learning streaks — all built with reusable components and modern UI design principles.

## Tech Stack

- Vue.js (Progressive JavaScript Framework)
- vue-chartjs (Vue wrapper for Chart.js)
- Chart.js (Chart visualization library)

## Requirements

- Use component-based design with reusable logic and props (split complex UI into atomic components)
- Store progress or completion state in local storage (sync state using Vue lifecycle hooks)
- Use a chart library for visualizing data (vue-chartjs + Chart.js)

## Installation

bash
# Clone the repository
git clone https://github.com/your-username/Bitasmbl-CodeQuest-Interactive-Learning-Dashboard.git
cd Bitasmbl-CodeQuest-Interactive-Learning-Dashboard

# Install dependencies
npm install

# Compiles and hot-reloads for development
npm run serve


_No additional environment variables are required for local development._

## Usage

1. Run `npm run serve` to launch the development server.
2. Open your browser at `http://localhost:8080`.
3. Browse coding modules, complete lessons, and watch your progress update in real time.
4. Check the "Learning Streak" chart to visualize your activity over time.
5. Progress and completion states are persisted in local storage across sessions.

## Implementation Steps

1. Initialize the Vue.js project using Vue CLI: `vue create codequest-dashboard`.
2. Install charting libraries: `npm install vue-chartjs chart.js`.
3. Create a `components/` directory and add atomic components:
   - `LessonCard.vue` for individual lesson previews.
   - `ModuleList.vue` to display a list of modules.
   - `ProgressTracker.vue` to show completion state and unlock buttons.
   - `StreakChart.vue` to render the learning streak using vue-chartjs.
4. Implement a composable `useProgress.js` for local storage sync:
   - Use `onMounted` and `watch` from Vue to read/write JSON data in `localStorage`.
   - Expose reactive state and mutation functions via props or `provide/inject`.
5. In `StreakChart.vue`, import `Bar` or `Line` from `vue-chartjs` and feed it reactive streak data.
6. Assemble the main dashboard in `App.vue` or a dedicated `Dashboard.vue`, passing props to child components.
7. Style components with scoped CSS or a utility-first approach to maintain design consistency.
8. Test the flow: unlock lessons, update progress, refresh page, and verify persistence.
9. Build for production: `npm run build`.

<!--
(Optional) API Endpoints
Not applicable—this is a fully client-side application using Local Storage.
-->