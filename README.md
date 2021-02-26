# velodyne_plugin
- Gazebo tutorial - control plugin and connect ROS.

- The velodyne is a 3-D LiDAR.

* Your need install ros melodic package.

  - ``` $ sudo apt install libgazebo8-dev ```

``` bash
$ sudo yum install gazebo-devel
```

- create build dir in velodyne_plugin.

``` bash
$ cd velodyne_plugin
```

``` bash
$ mkdir build
```

- Compile the plugin.

``` bash
$ cmake ..
```

``` bash
$ make
```

- add plugin build library position to written into ~/.bashrc file.

``` bash
$ sudo gedit ~/.bashrc
```

``` bash
Add content "export LD_LIBRARY_PATH=${LD_LIBRARY_PATH}:~/velodyne_plugin/build" into ~/.bashrc file.
```

- run velodyne_plugin simulation under Gazebo.

``` bash
$ gazebo --verbose ../velodyne.world
```

- run velodyne_plugin z-axis rotation velocity command.

``` bash
$ ./vel 2
```
