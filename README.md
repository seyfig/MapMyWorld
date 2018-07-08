
# Map My World

In this project you will create a 2D occupancy grid and 3D octomap from a provided simulated environment. Furthermore, you will then create your own simulated environment to map as well.

## Installation Instructions

The project requires
* ROS Kinetic
* Gazebo
* RViz
* RTABMap, prefered version (https://github.com/introlab/rtabmap.git)
$ sudo apt-get install ros-kinetic-amcl

## Run the Project

```bash
$ cd ~/catkin_ws
$ catkin_make
$ source devel/setup.bash
```

And then run the following in *separate* terminals -
Select one
For Kitchen Dining World:
``` bash
$ roslaunch slam_project world.launch
```
For X World
``` bash
$ roslaunch slam_project xworld.launch
```
Then run these three, all in separate teminals.

``` bash
$ roslaunch slam_project teleop.launch
$ roslaunch slam_project mapping.launch
$ roslaunch slam_project rviz.launch
```

To save a new map:
``` bash
$ rosrun map_server map_saver -f xworld
```

To view recorded RTABMap database:
``` bash
$ rtabmap-databaseViewer ~/.ros/rtabmap.db
```

## Databases
The recorded databases have a size greater than 100MB for each. Therefore, they are stored in Google Drive. The link is as follows:
https://drive.google.com/drive/folders/14CR-ov-U2nzQxGAV2I7jGU6f5yugSc5v?usp=sharing