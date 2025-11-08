# Dar es Salaam Daladala and UDART Shapefiles

Geographic data repository containing shapefiles for Dar es Salaam's public transportation systems, including traditional Daladala routes and the UDART Bus Rapid Transit (BRT) network.

## Overview

This repository provides geospatial data for analyzing and mapping public transportation in Dar es Salaam, Tanzania. The data includes:

- **Daladala Routes**: Traditional informal minibus routes serving the city
- **UDART/DART Routes**: Bus Rapid Transit (BRT) system infrastructure and routes

## About the Transport Systems

### Daladala
Dalaladas are medium-sized privately-operated minibuses that form the backbone of Dar es Salaam's public transportation. With over 200 routes across the city, they provide affordable transportation for millions of residents daily.

### UDART (Usafiri Dar es Salaam Rapid Transit)
Launched in May 2016, UDART is East Africa's first Bus Rapid Transit system, operated under the regulatory framework of the Dar es Salaam Rapid Transit Agency (DART). The system features:
- 21 km of dedicated median bus lanes (Phase 1)
- 27 median stations
- 5 terminals
- Fleet of 210 articulated buses
- Serves approximately 165,000-200,000 passengers daily

## Data Format

The shapefiles in this repository are in standard ESRI Shapefile format (.shp, .shx, .dbf, .prj) and can be opened with GIS software such as:
- QGIS (free and open-source)
- ArcGIS
- GRASS GIS
- Any software supporting OGC standards

## Usage

### Loading in QGIS
1. Open QGIS
2. Go to Layer → Add Layer → Add Vector Layer
3. Browse to the shapefile (.shp) and click Add

### Loading in Python with GeoPandas
```python
import geopandas as gpd

# Load daladala routes
daladala = gpd.read_file('path/to/Daladala - Roads.shp')

# Load UDART routes
udart = gpd.read_file('path/to/UDART - Roads.shp')

# Display basic information
print(daladala.head())
print(udart.crs)  # Check coordinate reference system
```

### Loading in R
```r
library(sf)

# Load shapefiles
daladala <- st_read("path/to/Daladala - Roads.shp")
udart <- st_read("path/to/UDART - Roads.shp")

# Plot routes
plot(st_geometry(daladala))
```

## Coordinate Reference System

Please check the .prj file accompanying each shapefile for the specific coordinate reference system used. Common systems for Tanzania include:
- WGS 84 (EPSG:4326)
- UTM Zone 37S (EPSG:32737)

## Use Cases

This data can be used for:
- Transportation planning and analysis
- Urban development studies
- Accessibility mapping
- Transit optimization research
- Mobile app development for route planning
- Academic research on urban mobility
- Integration with OpenStreetMap

## Data Sources & Credits

### Primary Data Collection
This data was collected and compiled by **Samweli Mwakisambwe** as part of the Ramani Huria project in 2015, working in collaboration with ally (a mobility-based company) to map the entire public transport system in Dar es Salaam.

**Project Links:**
- Project Page: [https://samweli.github.io/Daladala-Routes/](https://samweli.github.io/Daladala-Routes/)

The mapping effort included:
- Field mapping of daladala routes
- OpenStreetMap contributions
- Collaboration with World Bank and transportation stakeholders
- Community-driven data collection through Ramani Huria

## Contributing

Contributions to improve and update these shapefiles are welcome! Please:
1. Fork the repository
2. Make your changes
3. Submit a pull request with a clear description of updates

## License

Please specify the license under which this data is shared. Common options for geographic data include:
- Open Database License (ODbL)
- Creative Commons licenses (CC-BY, CC-BY-SA)
- Public Domain

## Related Projects

- [Ramani Huria](https://ramanihuria.org/) - Community mapping project in Dar es Salaam
- [OpenStreetMap Tanzania](https://www.openstreetmap.org/)
- [Digital Matatus](http://digitalmatatus.com/) - Similar mapping project in Nairobi

## Contact

For questions, issues, or suggestions regarding this data, please open an issue in this repository.

## Acknowledgments

**Special thanks to Samweli Mwakisambwe** for leading the data collection and mapping efforts that made this repository possible. His work with the Ramani Huria project in 2015, in collaboration with ally and the World Bank, created the foundation for understanding and mapping Dar es Salaam's complex public transportation network.
His - GitHub: [https://github.com/Samweli](https://github.com/Samweli)

Additional acknowledgments to:
- Ramani Huria community mapping project
- ally (mobility-based company)
- World Bank
- OpenStreetMap Tanzania community
- All volunteers who contributed to field mapping efforts

---

**Note**: This data is provided for informational and analytical purposes. For real-time transit information, please consult official DART/UDART sources and local daladala operators.
