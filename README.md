## Install of ROS neotic
this is the last and easiest step for now you just have to open the terminal again and copy and paste these commands.

Setup your computer to accept software from packages.ros.org by using this command
```
sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
```
Set up your keys
```
sudo apt install curl


curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -
```
updating
```
sudo apt-get update
```
ROS distributions are linked to Ubuntu versions:

Ubuntu 20.04 -> Noetic

Ubuntu 18.04 -> Melodic

Ubuntu 16.04 -> Kinetic

now i'm using Ubuntu 20.04 so i'll install neotic, you can change "neotic" to one of the above depending on what version you are working with!
Installing ROS neotic Desktop-Full ,Everything in Desktop plus 2D/3D simulators and 2D/3D perception packages
```
sudo apt-get install ros-noetic-desktop-full
```
Environment setup
```
echo "source /opt/ros/noetic/setup.bash" >> ~/.bashrc

source ~/.bashrc
```
```
sudo apt install python3-rosdep python3-rosinstall python3-rosinstall-generator python3-wstool build-essential
```
```
sudo apt install python3-rosdep
```
```
sudo rosdep init
```
```
rosdep update
```
```
mkdir -p ~/catkin_ws/src
```
```
cd ~/catkin_ws/
```
```
catkin_make
```
```
cd ~/catkin_ws/src
```
here you can clone any project you want from Github, i will use the Arduino robot arm from Smart-Methods
```
git clone https://github.com/smart-methods/arduino_robot_arm.git 
```
```
cd ~/catkin_ws
```
```
rosdep install --from-paths src --ignore-src -r -y
```
```
sudo apt-get install ros-noetic-moveit
```
```
sudo apt-get install ros-noetic-joint-state-publisher ros-noetic-joint-state-publisher-gui
```
```
sudo apt-get install ros-noetic-gazebo-ros-control joint-state-publisher
```
```
sudo apt-get install ros-noetic-ros-controllers ros-noetic-ros-control
```
```
catkin_make
```
Launching ROS on a project from @Smart_methods for a robotic arm
```
roslaunch robot_arm_pkg check_motors.launch
```
Congrats!! 
![image](https://user-images.githubusercontent.com/108229185/181573247-90bdd582-8dd1-4bb6-8249-1f41cbaedecb.png)
