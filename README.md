<img width="536" alt="Screenshot 2023-10-24 at 10 54 00 AM" src="https://github.com/Azizbek-Akhmadov/SM-202302-IGS3231-001/assets/81019633/3bbdf6e0-5a7f-40b5-95a8-eb26f0d5511c"># SM-202302-IGS3231-001

# Week 3 
ROS Installation
*Set Locale
*Setup Sources: Output

![image](https://github.com/Azizbek-Akhmadov/SM-202302-IGS3231-001/assets/81019633/833052da-fdf5-4bee-99ce-91a1e8f1ceef)


*Setup Sources
*aptcache policy | grep universe

*sudo apt install software properties common
*sudo add apt repository universe

![Endpoint Badge](https://img.shields.io/endpoint?label=Smart%20Mobility%20Engineering%20Lab%20%5B202302-IGS3231-001%5D)

ROS2 VMWare Workstation Player Setup
• Configuring Ubuntu Virtual Machine
• ROS 2 Installation
• Activity Session ( OS & ROS 2 Test)

# Configuring Ubuntu Virtual Machine


<img width="1135" alt="Screenshot 2023-10-24 at 10 44 50 AM" src="https://github.com/Azizbek-Akhmadov/SM-202302-IGS3231-001/assets/81019633/4c174712-c8d6-47f8-8b0a-94e818e6c64a">

<img width="1078" alt="Screenshot 2023-10-24 at 10 45 18 AM" src="https://github.com/Azizbek-Akhmadov/SM-202302-IGS3231-001/assets/81019633/e97fe176-20bf-4354-a2ce-9bdd413ff181">

<img width="1143" alt="Screenshot 2023-10-24 at 10 45 37 AM" src="https://github.com/Azizbek-Akhmadov/SM-202302-IGS3231-001/assets/81019633/d55404f7-86b5-42f1-ac57-8b5f8670d586">

# ROS 2 Installation
* Set Locale

ocale # check for UTF-8
sudo apt update && sudo apt install locales
sudo locale-gen en_US en_US.UTF-8
sudo update-locale LC_ALL=en_US.UTF-8 LANG=en_US.UTF-8 export LANG=en_US.UTF-8
locale # verify settings

* Setup Sources
apt-cache policy | grep universe
sudo apt install software-properties-common
sudo add-apt-repository universe

sudo apt update && sudo apt install curl gnupg lsb-release
sudo curl -sSL https://raw.githubusercontent.com/ros/rosdistro/master/ros.key -o /usr/share/keyrings/ros-archive-keyring.gpg

echo "deb [arch=$(dpkg --print-architecture) signed- by=/usr/share/keyrings/ros-archive-keyring.gpg] http://packages.ros.org/ros2/ubuntu $(source /etc/os-release && echo $UBUNTU_CODENAME) main" | sudo tee /etc/apt/sources.list.d/ros2.list > /dev/null
 * Update your apt repository

sudo apt update –y
sudo apt upgrade
* Desktop-Full Install: (Recommended) :
sudo apt install ros-humble-desktop
sudo apt install ros-humble-ros-base
• Then add the repository to your sources
* Testing ROS 2 Installation (C++ )

  source /opt/ros/humble/setup.bash ros2 run demo_nodes_py listener
# Week 4 

• Turtlesim
• ROS2 & RQT
• Understanding the basic concepts
• Colcon
• Creating a workspace
• Creating a package
• Activity session ( OS & ROS 2 Test)

Turtlesim

• • •
System is up-to-date
– sudo apt update
Install the turtlesim library
– sudo apt install ros-rolling-turtlesim
Check that the package is installed:
– ros2 pkg executables turtlesim

<img width="546" alt="Screenshot 2023-10-24 at 10 54 13 AM" src="https://github.com/Azizbek-Akhmadov/SM-202302-IGS3231-001/assets/81019633/d5209cd3-cf74-48d3-951e-3fd6c1abdf5c">

 Command should return a list of turtlesim’s executables:
turtlesim draw square
turtlesim mimic
turtlesim turtle_teleop_key
turtlesim turtlesim node

To Start Tyurlesim 

ros2 run turtlesim turtlesim_node

To control the turtle we need type the following command:

– ros2 run turtlesim turtle_teleop_key

At this point we should have three windows open:

a terminal running turtlesim_ node
a terminal running turtle_teleop_key
the turtlesim window

<img width="566" alt="Screenshot 2023-10-24 at 10 58 08 AM" src="https://github.com/Azizbek-Akhmadov/SM-202302-IGS3231-001/assets/81019633/307a7968-cafe-45f8-8490-0246c39aad50">

ROS2 & RQT 


