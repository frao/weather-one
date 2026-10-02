# Weather One

Weather One is a mobile-first static weather web app published with GitHub Pages.

## Live data sources

- **Radar:** Iowa Environmental Mesonet (IEM) CONUS NEXRAD N0Q base reflectivity via WMS-T, with 5-minute frames and an approximately two-hour timeline. RainViewer is retained as an automatic fallback.
- **Weather:** Open-Meteo forecast/current weather.
- **UV and air quality:** Open-Meteo Air Quality API.
- **Official alerts:** National Weather Service API.
- **Tropical:** NOAA/NHC map services.
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
