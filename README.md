HexRouteMapper
A static browser-based walking route planner that counts distinct Uber H3 cells intersected by a route.
Features
Leaflet + OpenStreetMap map
Click to add start, end and intermediate waypoints; drag markers to adjust
Public Valhalla pedestrian routing, with explicitly labelled straight-line fallback
H3 resolution 8–15 (12 by default)
Exact segment-vs-cell-polygon intersection tests on candidate cells
Distance, distinct cell count, CSV export, location search
Publish using GitHub Pages
Upload `index.html` and `README.md` to the root of the repository on branch `main`.
Open Settings → Pages in GitHub.
Under Build and deployment, choose Deploy from a branch, branch `main`, folder `/ (root)`, and Save.
Once Pages is active, open `https://waveform06.github.io/Page-HexRouteMapper/`.
The app requires an internet connection for the CDN libraries, map tiles, geocoding and routing. Public Valhalla routing is best-effort and may have availability or rate limits. Straight-line fallback is not a walking route.
The route intersection algorithm uses H3 gridDisk-1 around route samples spaced at most 3 metres. This is designed for resolutions 8–15; routes near poles or crossing the antimeridian need additional handling. Boundary-only touches count as intersections.
