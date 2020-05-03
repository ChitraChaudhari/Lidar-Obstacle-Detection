# Lidar Obstacle Detection

### Project Goals
-- Implement Obstacle detection on real PCD from a lidar
-- use pcl-library for general data handling and initial testing
-- implement following modules: 
   -- PCD filtering, for reducing computational cost, without loss of detail
  -- Segment the filtered cloud into two parts, road and obstacles, using RANSAC based 3D-plane extraction
  -- Cluster the obstacle cloud, using K-D Tree for 3D space.
  -- Find bounding boxes for the clusters

### Dependencies:

Ubuntu 16.04 OS

cmake >= 3.14

gcc/g++ >= 8.0

PCL >= 1.2 : The code extensively utilizes the Point Cloud Library (PCL).

### Installation

### Linux Ubuntu 16

Install PCL, C++

The link here is very helpful, 
https://larrylisky.com/2014/03/03/installing-pcl-on-ubuntu/

A few updates to the instructions above were needed.

* libvtk needed to be updated to libvtk6-dev instead of (libvtk5-dev). The linker was having trouble locating libvtk5-dev while building, but this might not be a problem for everyone.

* BUILD_visualization needed to be manually turned on, this link shows you how to do that,
http://www.pointclouds.org/documentation/tutorials/building_pcl.php

### Build and Run
clone this repository, enter the cloned directory/folder and build:
```
mkdir build && cd build
cmake ..
make
```

to run, use following from within the build folder:
```
./environment
```
### Sample Result
[![alt text](https://github.com/ChitraChaudhari/Lidar-Obstacle-Detection/blob/master/src/Lidar_Obstacle_Detection.mp4](https://github.com/ChitraChaudhari/Lidar-Obstacle-Detection/blob/master/src/Lidar_Obstacle_Detection.mp4 "title")
