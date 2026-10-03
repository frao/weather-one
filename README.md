# Weather One

Weather One is a mobile-first static weather web app published with GitHub Pages.

## Live data sources

- **Radar:** Iowa Environmental Mesonet (IEM) NEXRAD N0Q is the primary radar, using 5-minute frames and an approximately two-hour timeline. Playback uses buffered frame swapping to reduce flicker. RainViewer is retained as an automatic fallback.
- **Weather:** Open-Meteo forecast/current weather.
- **UV and air quality:** Open-Meteo Air Quality API.
- **Official alerts:** National Weather Service API.
- **Tropical:** NOAA/NHC track, cone, wind fields and watches/warnings. NOAA nowCOAST/NESDIS GOES infrared cloud imagery is available as a separate optional layer and is off by default. The app keeps a single animated radar layer to avoid duplicate radar overlays.
- **Basemap:** Esri World Imagery with reference/transportation layers.
- **ZIP lookup:** Zippopotam with Nominatim fallback.

## Product rules

Weather One does not generate synthetic weather alerts or tropical systems. Alert banners are sourced from the National Weather Service. Tropical information is sourced from NOAA/NHC.

## Deployment

The site is deployed from the `main` branch through GitHub Pages. It is also installable as a PWA using `manifest.webmanifest` and `sw.js`.

## Current deployed assets

- `index.html`
- `index-DNDlda4d.js`
- `index-CqPkHdAp.css`
- `manifest.webmanifest`
- `sw.js`
- `weather-one-icon.svg`

When changing JS/CSS, also bump the query-string asset version in `index.html` and the cache name/asset URLs in `sw.js` so installed PWA clients receive the update.

- **High-zoom radar trial:** at zoom 10+, Weather One attempts to switch from the CONUS IEM mosaic to the nearest available IEM single-site NEXRAD N0B archive, with automatic fallback to the mosaic if the local source is unavailable.
