# GeotagPhotos-Hyperlink
This script can be used to geotag photographs and add a hyperlink to the saved location. A feature class layer will be generated showing the location of the photographs. A hyperlink will be added to the attribute table linking to the file location. The layer can be configured to view the photograph within the pop up window (See section 4).

## 1. Prerequisites

- [ArcGIS Desktop](https://www.esri.com/en-us/arcgis/products/arcgis-desktop/overview)
- [Python](https://www.python.org/) (usually comes with ArcGIS installation).
- Photographs with georeference.

## 2. Important Notes

- <b>Warning!!!</b> Save your project before running the code.
- This code assumes that the ArcGIS project is currently open and active in the ArcGIS Desktop application.
- Make sure you have the necessary permissions to access the specified file location.

## 3. Step by Step Guide

Follow these steps to execute the code.

1. Open an ArcGISPro project.

2. Open a Notebook within ArcGISPro. (Insert --> New Notebook)

3. Copy and paste the [script](ArcGISPro_ExportMultipleMaps) into a cell in the Notebook.

4. Run the script. The code will prompt you to enter input variables.

5. Enter the input variables. Press <b>'Enter'</b> after entering each input.
   
6. Wait for the code to execute. Then check the output folder.
   
| Variable name | Description | Example | 
| -------- | -------- | -------- |
| `inFolder` | Input folder location where the photographs are saved |C:\Pictures\Photos|
| `outputfile` | Output feature class layer name | Photos|
| `outfolder` | Output location of the feature class layer | C:\GIS\MyProject1.gdb|

## 4. Code Explanation

The script performs the following steps:

1. It imports required modules.

2. It opens the current ArcGIS project using the `ArcGISProject` class.

3. Run the GeoTaggedPhotosToPoints tool to create a feature class with geotagged photo locations.
   
6. Add a new field to the attribute table with a hyperlink to the photograph file location.

## 4. View the photograph within the pop up window

To view the photograph within the pop up window:

1. Right click on layer --> configure pop ups --> Text --> edit text.

2. Enable HTML mode.

3. Replace the existing code with the following code.
   <br>``` <img src="{Path}" style="width:800px;height:600px;"> ```</br>
   
## 5. License

This script is provided under the [MIT License](LICENSE).
