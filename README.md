# burn-severity
[![img](https://img.shields.io/badge/Lifecycle-Stable-97ca00)](https://github.com/bcgov/repomountie/blob/master/doc/lifecycle-badges.md)

GIS tools for classifying wildfire burn severity from satellite imagery
## Usage
This tool will take a fire perimeter and use pre and post fire Landsat images to classify burn severitsy. The images are compared and a severity polygon layer is created based on the fire perimeter.
Generally Post fire images are Landsat  7 or Landsat  8 with 8 being the most prefered. Prefire images being 5, 7 or 8 with the most preferred being Landsat 8.
### Inputs
  1.Fire perimeter shapefile
  2.Post fire Landsat Image placed in separate folder
  3.Pre fire Landsat Image placed in separate folder

## Script Descriptions

### dnbr_maker.py
This script creates a Differenced Normalized Burn Ratio Raster(DNBR) from Post and Pre fire Landsat imagery.

### barc4_maker.py
This script creates a Burned Area Reflectance Classification(BARC) from a Differenced Normalized Burn Ratio Raster(DNBR).

### landsat.py
This module conatains classes for parsing Landsat 5,7,8 metadata(.MTL) files

### barc_module.py
This module contains Landsat image processing functions and classes that perform; top of atmosphere correction, differenced normalized burn ratio calculations, Metadata parsing

## Requirements
Requires ESRI ArcInfo/Spatial Analyst licensing & ArcMap 10.1+.

## Getting Help or Reporting an Issue
Use the Issues tab to get help or report any issues.

## License
Copyright 2015-2016 Province of British Columbia

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
