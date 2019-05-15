# UrbanHeatPro
Bottom-up model for the simulation of heat demand profiles of urban areas
A. Molar-Cruz @ TUM ENS

## Features

  - UrbanHeatPro is a python-based bottom-up model for the simulation of heat demand profiles of urban areas.
  - It considers both the space heating demand and hot water demand. So far, the hot water demand is calculated only for residential buildings.
  - Characteristic values for the building stock, building thermal properties, building set-temperature and annual hot water consumption are based on statistics for Germany.
  - DSM strategies for the reduction of heat demand such as building renovation, heat load reduction, night-set back operation, etc, are easily implemented.
  - The size of the study area can start from one building. Buildings can be input as a shapefile or as an excel table.
  - By default, the model operates on an hourly time steps. However, the temporal resolution is configurable.


## Requirements
Python 3.6 if multiprocessing is used (installation with Anaconda recommended)
Python 2.7 (installation with Anaconda recommended)


## Input file (csv)
Each building is described with the following information:
<ol>
  <li>Area (required)</li>
      Building ground floor area in m²
  B.	Use (required)
      Building use as integer:
        0	Commercial
        1	Industrial
        2	Public
        3	Residential
  C.	Bid (optional)
      Building identification number as integer
  D.	Free_walls (required)
      Number of walls in contact with ambient temperature. The building is assumed to be a rectangular box with four walls.
  E.	Construction year class (optional)
      Construction year class from TABULA Typology as integer:
        0	<1859
        1	1860 - 1918
        2	1919 - 1948
        3	1949 - 1957
        4	1958 - 1968
        5	1969 - 1978
        6	1979 - 1983
        7	1984 - 1994
        8	1995 - 2001
        9	2002 - 2009
  F.	Building type (optional)
      Building type from TABULA Typology as integer:
        0	Single-Family House (SFH)
        1	Terraced House (TH)
        2	Multi-family House (MFH)
        3	Apartment Block (AB)
All columns are required, if no information is given, the cell value is taken as NaN.
This input file should be located in the corresponding folder input/buildings


## Using UrbanHeatPro
To run the model with the given input data, change the desired information in the runme.py file and run this file in the command line:
>> python runme.py

For more details please refer to the documentation file

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.


## Copyright
Copyright (C) 2018-2019 TUM ENS

This program is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details.

You should have received a copy of the GNU General Public License along with this program. If not, see http://www.gnu.org/licenses/
