# Pioneer P3-DX Model

A ROS/Gazebo Pioneer 3DX model created by Rafael Berkvens (rafael.berkvens@uantwerpen.be) and modified by Mario Serna Hernández. This is a model adapted to the Pioneer P3-DX robot of the Movis Research & Innovation Group.

# Source repository:
https://github.com/SD-Robot-Vision/PioneerModel.git

# To install:
```
$ cd <catkin_ws>/src
$ git clone https://github.com/kmarif/pioneer_p3dx_model.git
$ cd ..
$ catkin_make
```

# To use (1):
```
To make sure your workspace is properly overlayed by the setup script.
$ source <catkin_ws>/devel/setup.sh
Launching Gazebo
$ roslaunch gazebo_ros empty_world.launch
Spawning Robot
$ roslaunch p3dx_gazebo p3dx.launch

p3dx.launch arguments:
* ns:= (namespace) | default: p3dx
* x:= (x position) | default: 0.0
* y:= (y position) | default: 0.0
* z:= (z position) | default: 0.0

Spawning two or more robots
$ roslaunch p3dx_gazebo p3dx.launch ns:=p3dx_1
$ roslaunch p3dx_gazebo p3dx.launch ns:=p3dx_2 x:=2
$ roslaunch p3dx_gazebo p3dx.launch ns:=p3dx_3 x:=2 y:=2

Launching Rviz
$ roslaunch p3dx_description rviz.launch
```

# To use (2):
```
To make sure your workspace is properly overlayed by the setup script.
$ source <catkin_ws>/devel/setup.sh

Launching Gazebo and Robot together 
$ roslaunch p3dx_gazebo pioneer3dx.launch
--> The p3dx_gazebo/launch folder also contians a few other variants of the launch file 
e.g., pioneer3dxCam.launch, pioneer3dxSonar.launch .

Launching Rviz
$ roslaunch p3dx_description rviz.launch
```

# Note:
```
In order to use the other included world files, it is necessary to replace the following for all the matches:

Example:
p3dx_gazebo/worlds/p3dx_map1.world

<uri>/home/<username>/<catkin_ws_name>/src/pioneer_p3dx_model/p3dx_description/meshes/chassis.stl</uri>

```
