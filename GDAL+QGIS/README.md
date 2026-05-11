# GDAL and QGIS Raster Workflow

This section demonstrates basic geospatial raster processing and GIS visualization workflows using GDAL and QGIS.

## Tools Used

- GDAL
- QGIS

---

## GDAL Workflow

Basic GDAL commands were used for raster inspection, raster conversion, and raster resizing operations.

### Raster Metadata Inspection

```bash
gdalinfo input.jpg
```

Used to inspect raster properties such as:
- image dimensions
- raster bands
- metadata structure

### Raster Conversion

```bash
gdal_translate input.jpg output.tif
```

Used to convert raster images into GeoTIFF-compatible formats for GIS visualization workflows.

### Raster Resizing

```bash
gdal_translate -outsize 128 128 input.tif output_128.tif
```

Used to resize raster images and demonstrate basic raster manipulation operations commonly used in geospatial preprocessing workflows.

---

## QGIS Workflow

QGIS was used to:
- load raster layers
- visualize satellite image outputs
- explore raster properties
- export raster visualizations

This workflow demonstrates familiarity with basic GIS raster handling and visualization concepts 

---

## Notes

The EuroSAT RGB dataset contains satellite image patches and does not include full georeferencing metadata. GDAL and QGIS were used primarily to demonstrate raster processing and GIS visualization workflows.