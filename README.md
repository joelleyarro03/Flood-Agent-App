# Flood-Agent-Semantic-Kernel

A Flask-based backend API for flood monitoring and emergency response routing. This service provides real-time flood alerts, hazard polygons, and safe hospital routing for the Houston area.

## Features

- **Flood Alerts**: Fetches active flood warnings from the National Weather Service (NWS) API
- **Flood Inundation Mapping (FIM)**: Integrates with NOAA's FIM service for detailed flood extent predictions
- **TranStar Flood Points**: Access to Houston TranStar flood-prone location data
- **Safe Hospital Routing**: Calculates flood-aware routes to nearby hospitals using OSRM
- **Geocoding**: Converts addresses to coordinates using Nominatim
- **Health Check**: Simple endpoint to verify service availability

## API Endpoints

### Health Check
- `GET /api/health` - Returns service health status

### Flood Data
- `GET /api/flood-mask` - Returns unified flood polygon data (NWS alerts + FIM + TranStar points)
  - Query params: `bbox` (optional) - Bounding box as `west,south,east,north` (lon/lat)

### Geocoding
- `GET /api/geocode` - Convert address to coordinates
  - Query params: `q` (required) - Address string to geocode

### Hospital Routing
- `GET /api/hospital-route` - Get flood-aware route to nearest hospitals
  - Query params: 
    - `lat` (required) - Starting latitude
    - `lon` (required) - Starting longitude
    - `radius` (optional) - Search radius in km (default: 20)

## Installation

1. Clone the repository:
```bash
git clone https://github.com/joelleyarro03/Flood-Agent-Semantic-Kernel-.git
cd Flood-Agent-Semantic-Kernel-
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Run the application:
```bash
python app.py
```

The server will start on `http://localhost:5001`

## Configuration

Edit `config.py` to customize:
- `DEFAULT_RADIUS_KM` - Default search radius for hospitals
- `FLOOD_BUFFER_METERS` - Buffer distance for flood polygons
- `TRANSTAR_POINT_BUFFER_METERS` - Avoidance radius for flood-prone points
- `DEFAULT_BBOX` - Default bounding box for Houston area

## External Services

This application integrates with:
- **National Weather Service API** - Real-time flood alerts
- **NOAA FIM** - Flood inundation mapping
- **Houston TranStar** - Local flood monitoring data
- **Nominatim** - OpenStreetMap geocoding
- **OSRM** - Routing engine
- **Overpass API** - OpenStreetMap hospital data

## Development

The application uses Flask with CORS enabled for cross-origin requests. Caching is implemented using `cachetools` to reduce external API calls.

## License

This project is part of the Panacea emergency response system.
