# Launching Autoware


## Autoware Only
### To launch Autoware:
```
source $HOME/autoware/install/setup.bash
source /opt/ros/humble/setup.bash
```
Nishijinuku Map:
```
ros2 launch autoware_launch planning_simulator.launch.xml vehicle_model:=sample_vehicle sensor_model:=awsim_sensor_kit map_path:=$HOME/autoware_map/nishishinjuku_autoware_map/
```
Sample Map:
```
ros2 launch autoware_launch planning_simulator.launch.xml vehicle_model:=sample_vehicle sensor_model:=awsim_sensor_kit map_path:=$HOME/autoware_map/sample-map-planning/
```

## Autoware and AWSIM Binary
### To launch Autoware:
```
source $HOME/autoware/install/setup.bash
source /opt/ros/humble/setup.bash
ros2 launch autoware_launch e2e_simulator.launch.xml vehicle_model:=sample_vehicle sensor_model:=awsim_sensor_kit map_path:=$HOME/autoware_map/nishishinjuku_autoware_map/
```
### To launch Awsim:
```
cd $HOME/AWSIM_v1.2.0
./AWSIM_v1.2.0.x86_64
```
## SIRC or Nishishinjuku Parking Autoware and AWSIM Unity Editor
`Note that “source /opt/ros/humble/setup.bash” must be taken out of the .bashrc file, and the terminal must not be ROS2 sourced.`
### First launch Unity Editor:
` Make sure ROS2 is NOT SOURCED in terminal`
```
cd $HOME/Unity
./UnityHub.AppImage
```
- Click on AWSIM project with path ‘home/ovin/Unity/AWSIM’
- Click play at the top.
### Launch Autoware:
```
cd $HOME/autoware
source $HOME/autoware/install/setup.bash
source /opt/ros/humble/setup.bash
```
SIRC Parking Lot Map: 
```
ros2 launch autoware_launch e2e_simulator.launch.xml vehicle_model:=sample_vehicle sensor_model:=awsim_sensor_kit map_path:=$HOME/autoware_map/sirc_parking_lot/ 
```
Nishishinjuku Map: 
```
ros2 launch autoware_launch e2e_simulator.launch.xml vehicle_model:=sample_vehicle sensor_model:=awsim_sensor_kit map_path:=$HOME/autoware_map/nishishinjuku_autoware_map/
```
