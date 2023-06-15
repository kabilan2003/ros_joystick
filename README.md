# ros_joystick using turtlesim

# Install the package 

sudo apt-get install ros-noetic-joy

# connect joystick with user system and Configuring the Joystick

ls /dev/input/

# The output in terminal like this 

by-id    event0  event10  event12  event14  event16  event18  event2   event21  event23  event3  event5  event7  event9  mice
by-path  event1  event11  event13  event15  event17  event19  event20  event22  event24  event4  event6  event8  js0     mouse0



As you can see above, the joystick devices are referred to by js0 .Let's make sure that the joystick is working. 

 sudo jstest /dev/input/js0
 
 output in terminal
 
 Driver version is 2.1.0.
Joystick (ShanWan PC/PS3/Android) has 6 axes (X, Y, Z, Rz, Hat0X, Hat0Y)
and 13 buttons (BtnA, BtnB, BtnC, BtnX, BtnY, BtnZ, BtnTL, BtnTR, BtnTL2, BtnTR2, BtnSelect, BtnStart, BtnMode).
Testing ... (interrupt to exit)
Axes:  0:     0  1:     0  2:     0  3:     0  4:     0  5:     0 Buttons:  0:off  1:off  2:off  3:off  4:off  5:off  6:off  7:off  8:off  9:off 10:off 11:off 12


# Lets start joystick node 

roscore 

# Now we can start the joy node

rosrun joy joy_node


