# SLAMTEC LIDAR ROS2 Package | [Chinese](./README.zh-CN.md)

ROS2 node for SLAMTEC LIDAR

Visit following Website for more details about SLAMTEC LIDAR:

SLAMTEC LIDAR roswiki: http://wiki.ros.org/rplidar

SLAMTEC LIDAR HomePage: http://www.slamtec.com/en/Lidar

SLAMTEC LIDAR SDK: https://github.com/Slamtec/rplidar_sdk

SLAMTEC LIDAR Tutorial: https://github.com/robopeak/rplidar_ros/wiki


Supported SLAMTEC LIDAR
-------------------
| Lidar Model    | 
| ---------------------- | 
|RPLIDAR A1              | 
|RPLIDAR A2              | 
|RPLIDAR A3              | 
|RPLIDAR S1              | 
|RPLIDAR S2              | 
|RPLIDAR S2E             | 
|RPLIDAR T1              | 


## How to [install ROS2](https://index.ros.org/doc/ros2/Installation)
[rolling](https://docs.ros.org/en/rolling/Installation.html),
[humble](https://docs.ros.org/en/humble/Installation.html),
[galactic](https://docs.ros.org/en/galactic/Installation.html),
[foxy](https://docs.ros.org/en/foxy/Installation.html)


## How to configuring your ROS 2 environment
[Configuring your ROS 2 environment](https://docs.ros.org/en/foxy/Tutorials/Configuring-ROS2-Environment.html)

## How to Create a ROS2 workspace
[Create a workspace](https://docs.ros.org/en/foxy/Tutorials/Workspace/Creating-A-Workspace.html)

## Compile & Install rplidar_ros package

1. Clone rplidar_ros package from github : 

   ```bash
   git clone -b ros2 https://github.com/Slamtec/rplidar_ros.git
   ``` 

2. Build rpidar_ros package :

   ```bash
   cd <your_own_ros2_ws>
   colcon build --symlink-install
   ```
   if you find output like "colcon:command not found",you need separate [install colcon](https://docs.ros.org/en/foxy/Tutorials/Colcon-Tutorial.html#install-colcon) build tools. 


3. Package environment setup :
    ```bash
    source ./install/setup.bash
    ```

    Note: Add permanent workspace environment variables.
    It's convenientif the ROS2 environment variables are automatically added to your bash session every time a new shell is launched:
    ```bash
    $echo "source <your_own_ros2_ws>/install/setup.bash" >> ~/.bashrc
    $source ~/.bashrc
    ```

## Run rplidar_ros

### Run rplidar node and view in the rviz

The command for RPLIDAR A1/A2 is : 

```bash
ros2 launch rplidar_ros view_rplidar_launch.py
```

The command for RPLIDAR A3 is : 

```bash
ros2 launch rplidar_ros view_rplidar_a3_launch.py
```

The command for RPLIDAR S1 is : 

```bash
ros2 launch rplidar_ros view_rplidar_s1_launch.py
```

The command for RPLIDAR S2 is : 

```bash
ros2 launch rplidar_ros view_rplidar_s2_launch.py
```

```bash
ros2 launch rplidar_ros view_rplidar_s2e_launch.py
```

The command for RPLIDAR T1 is : 

```bash
ros2 launch rplidar_ros view_rplidar_t1_launch.py
```

The command for RPLIDAR S1(TCP connection) is : 

```bash
ros2 launch rplidar_ros view_rplidar_s1_tcp_launch.py
```

Notice: the different is serial_baudrate between A1/A2 and A3/S1

## RPLIDAR frame
RPLIDAR frame must be broadcasted according to picture shown in rplidar-frame.png
