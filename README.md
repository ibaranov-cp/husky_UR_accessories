# husky_UR_accessories
Repo for various accessories attached to UR arms

Install pre-requisites for UR usage on system
```
sudo apt-get install ros-indigo-ur-modern-driver ros-indigo-moveit-planners* ros-indigo-moveit-ros-planning* ros-indigo-moveit-ros-move-group ros-indigo-moveit-ros-control-interface -y
```

Install pre-requisites for Gripper usage on system
```
sudo apt-get install ros-indigo-soem -y
rosdep install robotiq_modbus_tcp
```
S gripper is the 3 finger model, C gripper is 2 finger model
