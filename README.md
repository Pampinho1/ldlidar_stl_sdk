# Instructions
> This SDK is only applicable to the following product models:
> - LDROBOT LiDAR LD19
## 0. get LiDAR Linux SDK
```bash
$ cd ~

$ mkdir  ldlidar_ws

$ cd ldlidar_ws

$ git clone  https://github.com/DFRobotdl/ldlidar_stl_sdk.git
```
## step 1: system setup
- Connect the LiDAR to your system motherboard via an onboard serial port or usB-to-serial module (for example, CP2102 module).

- Set the -x permission for the serial port device mounted by the radar in the system (for example, /dev/ttyUSB0)

  - In actual use, the LiDAR can be set according to the actual mounted status of your system, you can use 'ls -l /dev' command to view.

``` bash
$ cd ~/ldlidar_ws/ldlidar_stl_sdk

$ sudo chmod 777 /dev/ttyUSB0
```

## step 2: build

``` bash
$ cd ~/ldlidar_ws/ldlidar_stl_sdk

$ ./auto_build.sh
```

## step 3: run

  ``` bash
  $ ./build/ldlidar_stl <serial_number>
  # eg ./build/ldlidar_stl /dev/ttyS0
  ```
