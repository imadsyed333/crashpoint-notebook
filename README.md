# GeoCrash

A geospatial analysis project that validates the geocoding accuracy of traffic collision records by matching them against their nearest intersection in the road network.

## Overview

Collision datasets often include textual street-name fields (e.g., `stname1`, `stname2`) alongside coordinate data. This project investigates whether those two representations agree — i.e., whether the coordinates of a collision actually place it at the intersection named in the record.

## Data

| File                     | Description                                                                                   |
| ------------------------ | --------------------------------------------------------------------------------------------- |
| `data/collisions.csv`    | Traffic collision records with street names, coordinates, ward, and contributing-factor flags |
| `data/intersections.csv` | City intersection centreline features with geometry and intersection descriptions             |

## Project Structure

```
geocrash/
├── data/
│   ├── collisions.csv
│   └── intersections.csv
├── notebooks/
│   └── analysis.ipynb   # Main analysis notebook
└── README.md
```

## Requirements

- Python 3.x
- [geopandas](https://geopandas.org/)
- [pandas](https://pandas.pydata.org/)
- [shapely](https://shapely.readthedocs.io/)
- [rapidfuzz](https://github.com/rapidfuzz/RapidFuzz)
- [matplotlib](https://matplotlib.org/)
