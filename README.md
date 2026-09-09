# Map Reference Layers

Public GeoJSON reference layers for map-based visualization and distance-band overlays.

## Purpose

This repository hosts reusable geospatial reference files for displaying concentric distance bands around selected map locations.

Current distance bands:

- 200 ft
- 400 ft
- 600 ft
- 800 ft

## Styling

The distance rings use a consistent proximity-weighted color convention:

- 200 ft — fuchsia
- 400 ft — dark navy
- 600 ft — medium blue
- 800 ft — light aqua

Closer distances are given stronger visual emphasis.

## Files

Reference layers are stored in the `rings/` folder.

Example structure:

    rings/
      DEV001_rings_200_400_600_800ft.geojson
      DEV002_rings_200_400_600_800ft.geojson

Each file contains concentric line geometries centered on a specific map location.

## Usage

The GeoJSON files are intended to be accessed through their direct raw-file URLs and consumed by compatible mapping or geospatial visualization tools.

A typical workflow is:

1. Select the GeoJSON file for the desired location
2. Use its direct raw-file URL as the reference-layer source
3. Render the distance rings together with location or point data in the mapping application

## File Naming

Reference-layer files follow this convention:

    DEV###_rings_200_400_600_800ft.geojson

Where:

- `DEV###` is a neutral location identifier
- the distance values identify the included ring radii in feet

## Notes

- Ring geometries are stored as GeoJSON `LineString` features
- Each ring represents a true geographic distance from its center point
- Styling is embedded in the GeoJSON so the same visual convention can be reused consistently
- This repository contains map-reference geometry only and does not contain operational, contact, CRM, or other business data
