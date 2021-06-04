# Headset Precision Analysis

Repos Guide:
- ExtractCoordinates_HTCVive -> Unity application of the Coordinate Extraction in HTC Vive
- Repeatability_tests_ROS -> ROS package of the Repeatability and Accuracy Tests

## Instructions on how to use
### HoloLens 2 application
1. The Unity application which is on the [*Operator4.0_HoloLens2* folder](https://gitlab.inesctec.pt/mirrorlabs/programming_by_demonstration) needs to be installed in the HoloLens2. The installation can be done through the Unity interface, and the version used for the application was 2019.4.2f1.
2. Therefore, you should open the Unity application through Unity Hub.
3. After opening the application in Unity, be careful to change the scene to *ExtractCoordinates*, and then, also alter the IP address (go to RosConnector object -> Inspector -> *Ros Bridge Server_IP*) to the IP of the computer where ROS will be running.
4. Then, you should install the application into the headset. To do that open the Build Window and go to Deploy Options. After connecting the HoloLens 2 to the computer, you should click on Test Connection to verify that it is indeed connected.
5. After that, just click on *Build all, then Install*. It may take a few minutes depending on the computer, but when finished, the application is ready to be launched in the headset.

### HTC Vive application
1. The Unity application which is on the [*ExtractCoordinates_HTCVive* folder](https://github.com/inesosoares6/ExtractCoordinates_HTCvive/README.md) needs to be installed in the HTC Vive. The installation can be done through the Unity interface, and the version used for the application was 2019.4.2f1.
2. Therefore, you should open the Unity application through Unity Hub.
3. After opening the application in Unity, be careful to change the IP address (go to RosConnector object -> Inspector -> *Ros Bridge Server_IP*) to the IP of the computer where ROS will be running.
4. Then, you should install the application into the headset. To do that open the Build Settings and choose the platform *PC, Mac & Linux Standalone*. Connect the HTC Vive Device to the computer and in Strem VR verify that the headset, the controllers and the base stations are being correctly detected.
5. After that, just click on *Build and Run*. It may take a few minutes depending on the computer, but when finished, the application will be launched in the headset.

### ROS package
1. Now, switching to the ROS environment, the ROS package included in the folder [*Repeatability_tests_ROS*](https://github.com/inesosoares6/Repeatability_tests/README.md) should be copied to the catkin workspace and then built. To do that through the terminal, type the following commands.
```
$ cd ~/catkin_ws/src
$ git clone https://gitlab.inesctec.pt/mirrorlabs/headset_precision_analysis.git
$ cd ~/catkin_ws
$ catkin_make
```

2. On a terminal type the following instruction to install the [rosbridge_server](https://github.com/RobotWebTools/rosbridge_suite):
```
$ sudo apt install ros-melodic-rosbridge-server
```

3. By this point, all the necessary software is installed and ready to run.


Notes: 
- The Unity application itself gives the necessary instructions on how to use it, however in [this page](../ExtractCoordinates_HTCVive/README.md) is done an overview on how it works.
- For further details on how the ROS package works, [this page](../Repeatability_tests_ROS/README.md) clarifies what scripts to execute and what they do.

## Author
Inês de Oliveira Soares (ines.o.soares@inesctec.pt | up201606615@up.pt)
- Master Student - Electrical and Computer Engineering @ FEUP
- Master Thesis Development @ INESC TEC
