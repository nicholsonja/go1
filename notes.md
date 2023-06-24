# Notes on Working with the Unitree Go1

## Connection Info
1. Connect to Robot Wifi
   * Wirelessly connect to : UniTree Wifi Network
   * Default WiFi Password: 00000000 (8 zeros)
   * Once connected, IP Address: 192.168.12.x
1. Log in
   * ssh pi@192.168.12.1
   * Default Password: 123

## Robot Configuration
* Debian Linux, running on a Rasberri PI
* ROS Melodic with Python2
* Camera is RGBD or RGB camera and Ultrasonic
* The Ultrasonic can detect from 0.5 meters (~1.64ft) to 2 meters (~6.56ft) away
* Web server
  * Can connect to a web server running on the robot at http://192.168.12.1
  * The web server is nginx and the root directory is in ~/Unitree/autostart/Webmonitor/dist

WiFi connection to the robot may disconnect even in close proximity

## Joint Calibration
We calibrated the Unitree Go1 using the Unitree support video: https://www.youtube.com/watch?v=cOuoeAt8ka4
We ran into issues due to the video missing a few key details. Here is our list of instructions supplementing the video.
1. Power on Go1.
1. Press L2+A then L2+B to make the robot lie down in a dampening state.
1. Press L2+B three times in a row.
1. Now when you twist the the legs of the Go1, you should not feel resistance.
1. Symmetrically close the left and right legs without gaps.
1. Press L2+R2, the robots legs should open.
1. Hold the calibration ruler to the thigh and the correct angle of the upper and lower legs.
1. Make a leg match the angle of the calibration ruler and pull backwards until the heel of the Go1 is firmly touching the ground.
1. Repeat for each leg.
1. Press in sequence:
   * L1+L2
   * L2+R1
   * L1+R1+R2
1. Shutdown and restart.
1. Calibration complete.

## Development
* Linux Ubuntu 18.04
* Expecting Python3.  Ubuntu 18.04 sets /usr/bin/python to python2

### Setting up ubuntu_legged_sdk
* Repository is https://github.com/unitreerobotics/unitree_legged_sdk
* Also need to install messagepack : `sudo apt install libmsgpack-dev`

## TO DO
* Setup a Ubuntu 18.04 ros_real_thing in the Unitree Respository
