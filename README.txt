
#### installation and settings ####

# install rosbridge-server on the computer that is running the simulation 
sudo apt-get update
sudo apt-get install ros-noetic-rosbridge-server

# download roslib to the computer that is running the website
sudo apt-get install npm 
npm i roslib


# if web and simulation both are not on the same computer 
{
# give necessary permisions for ip connection on the computer that is running the simulation 
sudo ufw allow 9090 
sudo ufw enable 

# check the ip address of the computer that is running the simulation 
ifconfig 
# replace localhost part with this ip address,  ws_address: 'ws://192.168.198.21:9090'  
}


#### Run ####
roslaunch go1_config gazebo.launch
roslaunch rosbridge_server rosbridge_websocket.launch

open the html file 
click on the connect button 
