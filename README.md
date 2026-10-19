# East Africa Hazards Map

A small interactive web map showing sample drought, flood and displacement
hotspots across the IGAD region (Kenya, Ethiopia, Somalia, South Sudan, Sudan,
Uganda, Djibouti and Eritrea). Built with Leaflet and plain JavaScript, reading
data from a GeoJSON file.

This is a **personal learning project** I built to get hands-on with web GIS
(Leaflet, GeoJSON, map layers and popups). The data is **illustrative sample
data only** — the figures are invented placeholders, not official IGAD or ICPAC
numbers.

## What it does

- Loads point data from `hazards.geojson`
- Colours each point by hazard type (drought, flood, displacement)
- Scales circle size roughly by the number of people affected
- Lets you toggle each hazard layer on and off
- Shows a popup with the location, hazard type, severity and people affected
- Includes a legend

## Tech

- [Leaflet](https://leafletjs.com/) for the map
- OpenStreetMap tiles for the base map
- GeoJSON for the data
- Plain HTML, CSS and JavaScript (no build step)

## Run it locally

Because the page fetches `hazards.geojson`, opening `index.html` directly from
the file system will be blocked by the browser. Serve it with a tiny local web
server instead:

```bash
# from inside the project folder
python -m http.server 8000
# then open http://localhost:8000 in your browser
```

## Deploy on GitHub Pages

1. Push this folder to a GitHub repository.
2. Go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to *Deploy from a branch*,
   branch `main`, folder `/root`.
4. Save. After a minute your map is live at
   `https://<your-username>.github.io/<repo-name>/`.

## Ideas to extend

- Swap the sample data for real open data (for example from an IGAD/ICPAC
  GeoNode or a HDX dataset).
- Add a time slider to show how hotspots change month to month.
- Pull live data from a REST API instead of a static file.
- Add polygons (district boundaries) and style them by severity.

## Licence

MIT — see `LICENSE`.
