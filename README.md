# Weather Station Dashboard

Live dashboard for a Pantech PT-WH2950 (Fine Offset / EasyWeather) weather station.

The station uploads readings to a PC on the local network (via a local DNS + DHCP +
Weather Underground receiver). A publish step exports the readings to `data.json` and
pushes this folder, which is served as a static site via **GitHub Pages**.

- `index.html` — self-contained dashboard (current conditions + time-series charts, light/dark, PWA)
- `data.json` — latest readings in metric units (°C, km/h, hPa, mm), refreshed periodically
- `manifest.webmanifest`, `sw.js`, `icon-*.png` — installable PWA shell

Data updates every few minutes; the page re-fetches `data.json` once a minute.
