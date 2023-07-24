
# YDlidar X3 Ros2 Foxy by Phuwaset Sibta

Jul 23 2023


## Used By Phuwaset 
http://www.yahboom.net/study/EAI-X3

This project is used by the following companies:

- equipment：pc；X3
- environment：Ubuntu20.04；ROS2（Foxy）


## Running Tests

new workspace

```bash
   mkdir -p X3_ws/src
```


When using this radar, you need to enter the workspace every time you execute a command

```bash
  cd ~/X3_ws
```

Unzip the [X3_ws_src.zip] function package and put it into the src folder of the X3_ws workspace, and open the terminal in the workspace

```bash
  colcon build               # compile
  source install/setup.bash  # update environment
```

Note: Every time you modify the code in the function package, you need to [compile] and then [update environment].

Add the workspace to the .bashrc of the environment variable,

```bash
   echo "source ~/X3_ws/install/setup.bash" >> ~/.bashrc
```
sudo nano ~/.bashrc
gedit ~/.bashrc

Remap the USB serial port

```bash
  cd ~/X3_ws/src/ydlidar_ros2_driver-master/startup

  sudo chmod 777 *
  
  sudo ./initenv.sh
```

After binding, unplug the radar again.

Use the following command to view modified remap

```bash
  ll  /dev/ydlidar
```
source package

```bash
  . install/setup.bash
```
terminal test

```bash
  ros2 launch ydlidar_ros2_driver ydlidar_launch.py
```

## Support

For support, email phuwaset204@gmail.com or join our Slack channel.

