# Ronde Van Brianza

Static, client-side event page for the Ronde Van Brianza ride. It has no build
step or backend and can be published from the repository root with GitHub Pages.

## Run locally

Serve the repository over HTTP (the map loads the GPX with `fetch`; opening
`index.html` directly with `file://` will not work):

```sh
python -m http.server 8000
```

Then open <http://localhost:8000>.

## Route map

- `assets/RVB derde editie [WINTER].gpx` is the source for the route line and
  elevation profile. Keep this file at that path, or update the URL in
  `js/main.js` when replacing it.
- The map supports wheel, button, drag, and touch zoom/pan; Reset returns to the
  route view. Tile resolution follows the current zoom level, with the zoom-out
  extent covering Lombardy.
- The basemap uses OpenStreetMap tiles and needs an internet connection.
  Attribution is displayed on the map.
