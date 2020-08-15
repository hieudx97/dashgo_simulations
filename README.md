# dashgo
# dashgo_simulations
Dashgo Simulation in URDF &amp; Gazebo

Update ver 7:
---
https://github.com/hieudx97/dashgo_simulations.git
- Đế Robot, 2 bánh xe Lidar
- Tách riêng description và gazebo

Hướng dẫn sử dụng (trong trường hợp chỉ tải dashgo_simulations):
---
$ cd dashgo_ws/src/dashgo

$ sudo rm -r dashgo_description

$ git clone https://github.com/hieudx97/dashgo_simulations

$ cd ~/dashgo_ws

$ catkin_make

$ source devel/setup.bash

Để chạy description:
---
roslaunch dashgo_description dashgo_description.launch


Hướng dẫn Gmapping với giả lập:
---

Chạy factory:
---
roslaunch dashgo_gazebo factory_dashgo.launch


Chạy Gmapping:
---
roslaunch dashgo_gazebo gmapping.launch

Chạy Rviz:
---
roslaunch dashgo_rviz view_navigation.launch

Chạy teleop_keyboard:
---
rosrun dashgo_tools teleop_twist_keyboard.py

Lưu bản đồ:
---
roscd dashgo_gazebo/maps 
rosrun map_server map_saver -f factory_dashgo 

Hướng dẫn Navigation với giả lập:
---

Chạy factory trên Gazebo:
---
roslaunch dashgo_gazebo factory_dashgo.launch

Chạy Navigation:
---
roslaunch dashgo_gazebo navigation.launch

Chạy Rviz:
---
roslaunch dashgo_rviz view_navigation.launch
