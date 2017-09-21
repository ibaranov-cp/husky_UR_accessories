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


Copy launch files from:
```
robotiq_force_torque_sensor/launch/ft_300.launch
robotiq_s_gripper/robotiq_s_model_control/launch/s_model.launch
into /etc/ros/indigo/husky-core.d/
```
and modifiy the params in each launch file to point to the appropriate FTDI and IP addresses

check that gripper behaves by re-setting and then activating/opening closing the gripper with:
```
rosrun robotiq_s_model_control SModelSimpleController.py
```
