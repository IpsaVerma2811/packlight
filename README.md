# Packlight — P32 Weather-Aware Packing Planner

A responsive, single-page packing planner built with plain HTML, CSS and JavaScript.

## Features
- Destination lookup and forecast data from Open-Meteo (no API key required)
- Weather-aware packing suggestions based on trip dates, forecast and activities
- Estimated luggage weight and a configurable weight target
- Activity-specific packing categories and a custom-item option
- Local browser storage for trip details, checklist progress and recent forecasts
- Loading, validation, error and seasonal-fallback states
- Responsive layout, keyboard focus styles and reduced-motion support

## Run locally
Open `index.html` in a browser. Weather requests require internet access. If you want to test clipboard behavior, use a local server or GitHub Pages.

## Publish with GitHub Pages
1. Create a new public GitHub repository, for example `packlight-p32`.
2. Upload `index.html` and `README.md` to the repository root.
3. Open **Settings → Pages**.
4. Under **Build and deployment**, select **Deploy from a branch**.
5. Choose branch **main** and folder **/(root)**, then click **Save**.
6. Wait for GitHub Pages to publish. Your URL will usually look like:
   `https://YOUR-USERNAME.github.io/packlight-p32/`
7. Open the published URL and test a city, dates, activities, ticking items and refreshing the page.

## Notes
- Open-Meteo forecasts have a limited forward range. For dates outside that range, the app clearly explains that available forecast temperatures may not match the exact trip dates.
- If the API is unreachable, the app uses a saved forecast for the same destination when possible; otherwise it shows a clearly labelled seasonal estimate.
- Estimated item weights are illustrative averages, not measured weights.
- Trip data and checklist state are stored in this browser's local storage; they are not sent to a backend.
