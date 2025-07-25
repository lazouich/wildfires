# Wildfire Data Analysis and Visualization

This repository contains materials for a conference talk on wildfire data analysis and visualization using Python. The talk explores how to work with geospatial wildfire data, clean it, analyze it, and create compelling visualizations.


## Key Terminology

### Wildfire Terminology

**Perimeter**  
The outer boundary of a wildfire.

**Containment**  
Limiting the spread of a wildfire. The fire is still active. Usually represented as a percentage. 40% contained doesn't mean 40% of the fire is out. It means 40% of the fire's perimeter isn't expected to spread because of a man-made or natural physical barrier (firebreak).

**Acreage**  
A measure of the land area affected by a wildfire.

**IRWINID**  
Unique identifier assigned to each incident record in IRWIN (Integrated Reporting of Wildland-Fire Information). IRWIN is software that allows data to be shared between applications so that there's a single data source for every incident.


### Geospatial Terminology

**Geospatial Data**  
Data with a component that relates to a location on Earth. Examples include Google Maps, natural disaster tracking, and maps with locations of train stations.

**Point**  
A single location on Earth.

**Polygon**  
A closed shape on a map.

**Coordinate Reference System**  
Describes where a geometry is located on the Earth's surface. A common reference system is 4326 - World Geodetic System 1984.

## Data Source

The **National Interagency Fire Center** (NIFC) is our primary data source. Worth noting that fire data is updated "slowly". Update speed can depend on the size of the fire and where the fire is. A state like CA with regular wildfires and infrastructure to report on them might give a fire update 3x a day. It is not uncommon to not have an update on a fire for days or even weeks.

Data can be found at: https://data-nifc.opendata.arcgis.com/datasets/nifc::wfigs-2025-interagency-fire-perimeters-to-date/about

## Setup and Usage

1. Clone this repository
2. Install [uv](https://github.com/astral-sh/uv) if you don't have it already
3. Set up a virtual environment and install dependencies:
   ```shell
   uv venv
   uv pip install -e .
   ```
4. Open and run the Jupyter notebook:
   ```shell
   jupyter notebook notebook.ipynb
   ```

## Visualization Examples

The notebook demonstrates several visualization techniques:
- Basic wildfire perimeter visualization
- Coloring fires by acreage and cost
- Filtering fires by geographic location
- Aggregating fire counts by state
