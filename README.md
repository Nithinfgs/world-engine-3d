# 🌍 World Engine — The Digital Twin of Earth

**World Engine** is a high-fidelity, interactive 3D digital twin simulation of Earth. Merging concepts from flight tracking dashboards, space mission telemetry, seismic maps, and AI-driven systems diagnostics, it serves as a fully responsive browser-based HUD interface built for visual excellence and systems-level exploration.

---

## 🛰️ Visualizer & Physics Subsystems

*   **Procedural Holographic Globe**: 
    *   *Continent Matrices*: Renders Earth's landmasses using a high-density, mathematical particle dot-grid for a clean, futuristic vector appearance (no heavy textures required).
    *   *Telemetry Grid*: A glowing cyan wireframe outlining parallels and meridians (latitude/longitude lines) at 24-division resolution.
    *   *Glow Atmosphere*: Embedded semi-transparent internal sphere (`#08111F`) providing depth and night-side shading.
*   **Solar System Mode**:
    *   *Heliostatic Core*: Renders a central glowing Sun mesh with slow axial rotation.
    *   *Earth-Moon Orbital Mesh*: Renders a shrunken wireframe Earth model orbiting the Sun, accompanied by a Moon node orbiting Earth with local gravity physics.
    *   *Mars Node*: Renders a red wireframe Mars orbiting the Sun on a wider trajectory.
    *   *Orbit Rings*: Renders concentric orbital path rings representing planetary tracks.
*   **Cinematic Camera Flight Path Engine**:
    *   Uses **three-dimensional LERP linear interpolation** to glide the camera smoothly from space down to precise coordinates when a search query, alert, or sensor is activated.
*   **Tectonic Alert Camera Shaker**:
    *   Applies a fast, pseudo-random coordinate jitter vector to the active camera position, simulating tectonic ground shaking when high-intensity earthquake warnings are triggered.
*   **Temporal Timeline Asset Scale**:
    *   Adjusts active assets on the fly based on the timeline slider. For example, selecting year **2015** limits satellites to older groups, while **2035** overlays high-density Starlink constellations and changes forestry density indicators.

---

## 📊 The 7 Core Telemetry Layers

Each layer can be toggled on/off in the Sidebar to overlay data streams directly on the 3D globe:

1.  **Aviation Control**:
    *   *Bezier Trajectories*: Curved flight paths connecting major international airport hubs.
    *   *Aircraft Markers*: Dynamic flight icons traversing vectors with randomized airspeed factors.
    *   *Airspace Logs*: Air Traffic Control logs monitoring flight routes, slot delays, and volcanic ash NOTAM reports.
2.  **Space Command**:
    *   *Orbit Rings*: Inclined, polar, and equatorial orbital tracks.
    *   *Satellite Telemetry*: Satellite meshes tracking orbit progressions.
    *   *Space Weather*: Logs reporting solar wind indexes, Goldstone ground stations, and ISS coordinates.
3.  **Ocean Command**:
    *   *Shipping Fleets*: Telemetry logs tracking cargo vessel distribution and port queue delays.
    *   *Eco Zones*: Monitors coral reef temperatures and marine protected whale migration bands.
    *   *Subsea cables*: Visual checkouts of sea-bed transit lines.
4.  **Climate Grid**:
    *   *Environmental Stats*: Monitors atmospheric CO₂ ppm rates and temperature anomalies.
    *   *Thermal Plumes*: Tracks active wildfire vectors and Arctic sea-ice area changes.
5.  **Energy Infrastructure**:
    *   *Renewables Tracker*: Splits global consumption vectors (Solar, Wind, Coal, Nuclear).
    *   *Grid Frequency*: Monitors grid transmission stability indicators (49.98 Hz).
6.  **Internet Grid**:
    *   *CDN Outages*: Monitors regional server checkouts for AWS and Cloudflare CDNs.
    *   *Latency Meters*: Logs subsea fiber cable packet loss anomalies.
7.  **Health Grid**:
    *   *Air Quality (AQI)*: Tracks air quality risk zones.
    *   *Logistics*: Tracks vaccine supply transit streams and WHO risk metrics.

---

## 🧠 Integrated Intelligence & Command HUD

*   **Universal Earth Search**:
    *   Matches keywords (e.g. `Japan`, `ISS`, `Dubai`, `Tesla`, `Nuclear`) to fly the camera directly to targeted lat/lon coordinates.
*   **Layer Fusion Gauges**:
    *   An analytical overlay that checks combinations of active layers in the Sidebar:
        *   *Weather + Aviation + Grid*: Evaluates convective storm cells over flight corridors.
        *   *Weather + Geology + Earth*: Analyzes tidal surge impacts on fault lines.
        *   *Space + Grid + Earth*: Gauges satellite signal and solar wind interference.
*   **Interactive Tectonic Alert Ticker**:
    *   Pulsing warning banner in the bottom-left. Clicking it initiates camera flights, turns on geology layers, and triggers a 2.5-second camera tremor shake.
*   **Clickable Sensor Nodes**:
    *   Raycasted green dots representing buoys, weather stations, and transceivers. Clicking any dot opens a detailed telemetry panel displaying real-time sea temperatures, barometric pressures, or grid latencies.
*   **Planet Health Command Deck**:
    *   A full-screen analytical dashboard detailing composite global health indexes (Climate 71%, Oceans 68%, Carbon emissions rates, and forestry totals).
*   **AI Compare Modal**:
    *   Generates side-by-side diagnostic cards comparing countries (e.g. India vs China) across population, energy limits, and carbon rates.
*   **AI Continental Investigator**:
    *   Initiates simulated airspace checklists, checking weather charts, radar, and NOTAM logs for Europe or North America.

---

## 🛠️ Technology Stack

*   **HTML5 / CSS3**: Responsive CSS Grid layout with custom glassmorphic panel filters and custom sliders.
*   **React 19 (via ESM CDN)**: Declarative component framework loading from `esm.sh` directly in the browser.
*   **Three.js (via ESM CDN)**: WebGL-based hardware-accelerated 3D graphics rendering loops.
*   **Lucide Icons (via ESM CDN)**: SVGs dynamically rendered as React components.
*   **Zero Build Dependencies**: Runs native browser ES modules without compilation.

---

## 🚀 How to Run the App

Since modern browsers restrict ES modules from executing over local file systems (`file://` URLs), you cannot run the app by simply double-clicking the `index.html` file. Instead, launch a simple local web server:

### 1. Using Python (Built-in)
Open a terminal in the project folder and run:
```bash
python3 -m http.server 8000
```
Then navigate to [http://localhost:8000](http://localhost:8000) in your browser.

### 2. Using VS Code (Live Server)
If you are using VS Code, install the **Live Server** extension, open the project folder, and click **Go Live** at the bottom-right corner.

---

## 🌐 Online Deployment Guide

Because **World Engine** is a single, zero-dependency `index.html` file, hosting is instant:

1.  **Netlify / Vercel (Drag-and-Drop)**:
    *   Log into your Netlify or Vercel dashboard.
    *   Drag and drop the single `index.html` file directly onto the dashboard upload box.
    *   The app is instantly live online with a secure SSL link!
2.  **GitHub Pages**:
    *   Create a public GitHub repository.
    *   Commit and push your `index.html` file.
    *   Go to **Settings > Pages**, select the `main` branch, and click Save. Your page is published instantly.
