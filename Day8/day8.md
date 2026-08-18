# Day 08 — Build Your First AI-Powered Dashboard

**Live Preview:** [Personal Environmental Health Analyzer](https://environmental-health-analyzer-vansh.netlify.app/)

## Objective

The objective of Day 8 was to explore Claude Artifacts and transition from simple prompt responses to generating a complete, interactive front-end application. The task was designed to teach prompt-to-application generation, showing how an AI can build data visualizations, interactive filters, responsive layouts, and state management in a single session. This demonstrates how AI-assisted product building can rapidly move an idea into a functional prototype.

## Challenge Brief

The challenge was to build a "Personal Environmental Health Analyzer" — a data-driven dashboard that visualizes air quality and environmental health metrics across different cities. The deliverable was a fully functional, responsive, single-file HTML/CSS/JS application that allowed users to explore the data interactively.

## Prompt Used

The following prompt was used to generate the initial Artifact:

```text
Build a Personal Environmental Health Analyzer dashboard using Claude Artifacts.

Requirements:
- Single-page application (HTML/CSS/JS).
- Professional, modern, and clean aesthetic.
- Allow me to select a "Focus City" to view its environmental grade and health score.
- Include a way to compare the Focus City against another city.
- Visualize AQI (Air Quality Index) data using charts.
- Allow filtering by different pollutants (e.g., PM2.5, PM10).
- Include an interactive AQI range slider to filter data.
- Include segmented controls and custom dropdowns.
- Provide a summary report or insights section based on the selected city.
- Ensure the layout is responsive and works well on mobile.
- Include a dark mode toggle.
- Use simulated demo data for a few days (e.g., August 17-22, 2026).
- Use Chart.js for data visualization if possible.
```

## Application Overview

The resulting application is the **Personal Environmental Health Analyzer**.

**Dashboard Purpose:** A tool for individuals to track, compare, and analyze environmental health metrics and air quality across major metropolitan areas.

**Features:**
- **City Comparison:** Users can select a "Focus City" and a "Compare City" to see head-to-head metrics.
- **AQI & Pollutant Analysis:** Visualizes Air Quality Index alongside specific pollutant breakdowns (PM2.5, PM10, NO2, O3).
- **Health-Risk Filtering:** Users can filter the displayed cities by risk level (Good, Moderate, Unhealthy, Hazardous).
- **Environmental Health Scoring:** Each city is assigned a dynamic grade (A-F) and an overall health score (0-100).
- **Interactive Charts:** Uses Chart.js to render a multi-day comparison bar chart and a pollutant distribution donut chart.
- **Report-Card Insights:** Generates dynamic recommendations and executive summaries based on the selected focus city's data.
- **Responsive Experience:** The dashboard dynamically adapts from a multi-column desktop layout to a stacked, mobile-friendly interface.

## Design System

The application was built using a custom implementation of the **Vansh Digitals** visual identity:

- **Primary Color:** `#007BFF` (Blue)
- **Accent Color:** `#FFD722` (Yellow)
- **Typography:**
  - `DM Sans` for primary headings and prominent UI elements.
  - `Inter` for standard body text and UI controls.
  - `Inter Mono` for tabular data, metrics, and technical values.

**Aesthetic Principles:**
- Clean white default theme with a fully functional dark mode (using `#3d9bff` for primary contrast in dark mode).
- A modern, professional SaaS aesthetic.
- No gradients, unnecessary emojis, or heavy glassmorphism.
- Consistent, professional icon system using SVG paths.
- Accessible, custom-built UI controls (dropdowns, sliders, segmented buttons) that visually match the rest of the application.

## Data & Methodology

**Important:** The application runs entirely on **simulated/demo data**.

- **Date Range:** 17 August 2026 – 22 August 2026.
- **Simulated Dataset:** The data is deterministically generated within the application logic to provide a realistic demonstration of the dashboard's capabilities. It does not pull from a live API.
- **Demo Mode:** The application is explicitly labeled with a "Simulated data · Demo mode" badge in the header and a disclaimer in the footer to ensure the numbers are not mistaken for real-world environmental observations.
- **Derived Values:** Environmental scores (0-100) and grades (A-F) are calculated within the application based on the simulated AQI metrics.

## Interactive Features

The application includes the following fully working interactive elements:

- **Focus City Dropdown:** Updates the primary health score card, charts, and report insights.
- **Compare City Dropdown:** Updates the comparison chart and secondary metrics.
- **Pollutant Selector:** A segmented control that switches the primary chart's data context (e.g., between PM2.5, PM10, NO2, O3).
- **Health-Risk Filter:** A pill-based filter that filters the city ranking list based on risk categories.
- **AQI Range Control:** A dual-handle range slider that filters the visible cities based on a specific AQI range.
- **Date Selector:** A dropdown that changes the active data day, regenerating the simulated dataset and updating all dashboard components.
- **Compare Mode Toggle:** Switches the chart view to specifically compare the two selected cities.
- **Light/Dark Mode Toggle:** Instantly switches the entire application theme and chart color palettes.

## Responsive Design

The application was engineered to be fully responsive across a wide range of devices:

- **Desktop (>1024px):** Utilizes a spacious, multi-column CSS Grid layout, displaying KPIs, controls, charts, and reports side-by-side.
- **Tablet (768–1024px):** Adapts to a 2-column or 3-column layout where appropriate, stacking some of the broader chart sections.
- **Mobile (<640px):** Transitions to a strict single-column layout. All cards, charts, and controls stack vertically. The custom dropdowns and range sliders resize to fit the viewport, and chart canvases scale proportionally without causing horizontal overflow.

## UI Refinement

After the initial AI generation, the application underwent a dedicated UI and UX refinement pass to elevate the professional quality of the interface:

- **Custom Dropdowns:** Replaced native browser `<select>` elements with fully custom, keyboard-accessible dropdown components that match the application's typography, border radius, and `#007BFF` focus states.
- **Range Control Refinement:** Upgraded the native range slider to feature a visible `#007BFF` fill track between the handles and replaced the default browser thumbs with compact, modern square handles.
- **Segmented Controls:** Converted radio button logic into a clean segmented control interface, using solid blue backgrounds for active states rather than relying on drop shadows.
- **Spacing and Hierarchy:** Adjusted internal padding (`.card`, `.ccard`) and heading scales across breakpoints to ensure the interface didn't feel cluttered on smaller screens.
- **Overflow Prevention:** Fixed CSS rules (`overflow-x: hidden`) that were previously clipping the popovers of the new custom dropdowns on mobile views.

## Testing & QA

The application was rigorously tested to ensure all features work correctly:

- **Interaction Testing:** Verified that all dropdowns, segmented controls, and sliders update the global state and trigger UI re-renders without errors.
- **Date Selection Testing:** Confirmed that changing the date correctly updates the simulated dataset across all charts, cards, and the dynamic insights report.
- **Theme Toggle Testing:** Ensured dark mode applies correctly not just to the CSS variables, but also to the Chart.js configuration (updating grid lines and text colors).
- **Responsive Testing:** Conducted visual QA at multiple widths (down to 360px and 390px mobile viewports) to ensure no horizontal scrolling or clipped text occurred.
- **Console Verification:** Verified that the application runs completely free of JavaScript console errors.

## Evidence

- `dashboard-overview.png`
- `dashboard-interactions.png`
- `dashboard-responsive.png`

## Key Learnings

- **Claude Artifacts:** The ability to render code instantly changes the prompting paradigm from "write this code for me" to "let's build this product together."
- **Prompting for Applications:** Providing a detailed feature list and a strict design system upfront prevents the AI from making generic or contradictory aesthetic choices.
- **State Management:** When having an AI build an interactive dashboard, ensuring all UI components read from and write to a single centralized state object is critical for maintaining consistency across multiple widgets.
- **Iterative Refinement:** AI generated code is a powerful starting point, but dedicated refinement passes (like replacing native inputs with custom UI components) are still necessary to achieve a truly premium, SaaS-level feel.
- **Testing AI Interfaces:** Automated generation means you must rigorously test the edge cases (like narrow mobile viewports or overlapping dropdowns) that a human developer might have naturally anticipated.

## Final Outcome

Day 8 successfully produced a fully self-contained, highly interactive, and responsive Environmental Health Analyzer dashboard. It demonstrates the capability of Claude Artifacts to generate complex, data-driven single-page applications that adhere strictly to a defined visual identity and function reliably across devices.

## Limitations / Important Notes

- **Simulated Data:** All data presented in the dashboard is generated by a deterministic simulation algorithm for demonstration purposes. It does **not** reflect real-time or historical environmental measurements.
- **Browser Compatibility:** The custom UI controls rely on modern CSS features (like CSS Grid, `clamp()`, and custom properties) and may degrade visually on legacy browsers.

## Conclusion

Building the Environmental Health Analyzer with Claude Artifacts proved that AI is no longer just a code-completion tool; it is a rapid prototyping engine. By clearly defining the constraints, design system, and interactivity requirements, it's possible to go from a conceptual prompt to a polished, professional dashboard in a single session.
