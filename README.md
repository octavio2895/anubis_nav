## Run Intel Realsense permissions script
```
./scripts/realsense_setup_udev_rules.sh
```
## Remap the USB serial port to name rplidar
```
./scripts/rplidar_create_udev_rules.sh
```
Once you have change the USB port remap, you can change the launch file about the serial_port value.
```
<param name="serial_port" type="string" value="/dev/rplidar"/>
```
To install rplidar on your robot, see "https://github.com/robopeak/rplidar_ros/wiki"

```
ls -l / dev | grep ttyUSB
```
## Creating a Map

```
roslaunch anubis_nav start_bringup.launch
```

```
roslaunch anubis_nav slam.launch
```
## Saving the map
When the mapping is finished you can save the map to the robot's computer.
```
 rosrun map_server map_saver -f ~/catkin_ws/src/anubis_nav/maps/map
```

Check if map.pgm and map.yaml has been saved:
```
roscd anubis_nav/maps
ls -a map.pgm map.yaml
```
To read the map use the following command.
```
rosrun map_server map_server map.yaml
```
## Autonomous Navigation

```
roslaunch anubis_nav start_bringup.launch
```

```
roslaunch anubis_nav navigate.launch
```