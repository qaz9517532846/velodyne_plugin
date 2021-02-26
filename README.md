# velodyne_plugin
- Gazebo tutorial - control plugin and connect ROS.

- The velodyne is a 3-D LiDAR.

- Your need install ros melodic package.

  ``` $ sudo apt install libgazebo8-dev ```

  ``` $ sudo yum install gazebo-devel ```

- Create build dir in velodyne_plugin.

  ``` $ cd velodyne_plugin ```
  
  ``` $ mkdir build ```

- Compile the plugin.

  ``` $ cmake .. ```
  
  ``` $ make ```

- Add plugin build library position to written into ~/.bashrc file.

  ``` $ sudo gedit ~/.bashrc ```

  ``` Add content "export LD_LIBRARY_PATH=${LD_LIBRARY_PATH}:~/velodyne_plugin/build" into ~/.bashrc file. ```

- Run velodyne_plugin simulation under Gazebo.

  ``` $ gazebo --verbose ../velodyne.world ```

- Run velodyne_plugin z-axis rotation velocity command.

  ``` $ ./vel 2 ```
