# Italian Catasto Leaflet Map

A web-based interactive map application for viewing Italian cadastral (land registry) data using Leaflet.js. This application overlays official cadastral information from the Italian Revenue Agency (Agenzia delle Entrate) on top of OpenStreetMap tiles.

## Features

- **Interactive Cadastral Map**: Display official Italian cadastral data including parcels, buildings, zoning, and water features
- **Dual Layer Support**: Switch between OpenStreetMap base layer and cadastral overlay
- **Parcel Details**: Click anywhere on the map to retrieve detailed cadastral information including:
  - Parcel typology
  - Location details
  - Municipality code
  - Province
  - Sheet number (Foglio)
  - Parcel number (Particella)
  - Section
  - Development status
  - Attachment information
- **Geographic Coordinates**: Display latitude and longitude for any clicked location
- **Zoom Level Guidance**: Provides user feedback on optimal zoom levels for detailed cadastral data
- **Responsive Design**: Works on desktop and mobile devices

## Data Source

The cadastral data is provided by the Italian Revenue Agency (Agenzia delle Entrate) through their public WMS service:
- **Service URL**: `https://wms.cartografia.agenziaentrate.gov.it/inspire/wms/ows01.php`
- **Projection**: EPSG:6706 (ETRS89)
- **Layers**: Province boundaries, cadastral zoning, water features, parcels, buildings, and symbols

## Technical Details

- **Framework**: Leaflet.js
- **Base Map**: OpenStreetMap tiles
- **Projection Handling**: Proj4.js for coordinate transformations
- **Additional Plugins**:
  - Leaflet Pegman
  - Geocoder control
  - Locate control
  - Zoom display
  - Transparency control

## Usage

1. Open `index.html` in a modern web browser
2. The map will load centered on Padova, Italy
3. Use the layer control (top-left) to switch between street map and cadastral overlay
4. Click on any location to view cadastral details in a popup
5. Zoom in to level 17-18 for detailed building information

## Browser Support

- Modern browsers with JavaScript enabled
- Requires internet connection for map tiles and cadastral data

## License

This project uses data from the Italian Revenue Agency. Please refer to their terms of service for data usage.

## Contributing

This is a static web application. To contribute:
1. Fork the repository
2. Make your changes
3. Test locally by opening `index.html`
4. Submit a pull request

## Deployment

The application is configured for deployment to GitHub Pages via GitHub Actions. Any push to the main branch will automatically deploy the static site.
