# LIDAR-Grid-Visualizer
This project provides a Python implementation for converting LIDAR (range) measurements to an occupancy grid map. The occupancy grid map is a popular probabilistic representation of the environment, which discretizes the space into a grid and indicates whether each grid cell is occupied, free, or unknown.

## Overview
The main goal of this project is to take LIDAR measurements and create an occupancy grid map from them. The process involves the following steps:

1. Reading LIDAR Measurements: The LIDAR measurements, which include angles and corresponding distances, are read from a CSV file.
2. Converting LIDAR Measurements to Cartesian Coordinates: The angles and distances obtained from LIDAR are converted to Cartesian coordinates (x, y) using trigonometric functions.
3. Bresenham Line Drawing Algorithm: The Bresenham line drawing algorithm is utilized to generate straight lines between points in the grid map. This helps in creating the basic map.
4. Flood Fill Algorithm for Occupancy Grid Filling: The project implements a queue-based flood fill algorithm to fill empty areas in the occupancy grid map. The algorithm starts from a given center point and expands to neighboring elements until it encounters obstacles or free boundaries.
5. Generating Grid Map from Real LIDAR Data: The code provides functions to generate a grid map from real LIDAR data using ray casting.

## Requirements
To run this project, you need the following dependencies:
* Python 3.x
* NumPy
* Matplotlib

## Usage
1. Open the Jupyter notebook "LIDAR_to_Occupancy_Grid_Mapping.ipynb" in Google Colab.
2. Follow the instructions in the notebook to execute each cell and run the code step-by-step.
3. The notebook will guide you through visualizing the LIDAR measurements, generating the occupancy grid map, and displaying the results.

## License
This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments
This project is based on the work of Hans Moravec and A.E. Elfes in their paper "High resolution maps from wide-angle sonar" (1985). Special thanks to the original author, Atsushi Sakai, for providing the initial implementation as part of the PythonRoboticsGifs repository.
