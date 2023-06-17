# MobileRobot-Openloopcontrol
## Aim:

To develop a python control code to move the mobilerobot along the predefined path.

## Equipments Required:
1. RoboMaster EP core
2. Python 3.7

## Procedure:

Step1:
Initiate the MobileRobot.

Step2:
Connect your PC with the MobileRobot through Wi-Fi.

Step3:
Open batter_level.py file and check the battery.

Step4:
Open the other Python files and Program the movements of the robot using python.

Step5:
Execute the python program and record the movements.

## Program:
```
#Developed by: VASUNDRA SRI R
#Register number: 212222230168

from robomaster import robot
import time
from robomaster import camera

if _name_ == '_main_':
    ep_robot = robot.Robot()
    ep_robot.initialize(conn_type="ap")

    ep_chassis = ep_robot.chassis
    ep_led = ep_robot.led
    ep_camera = ep_robot.camera
          
    print("Video streaming started.....")
    ep_camera.start_video_stream(display=True, resolution = camera.STREAM_360P)
    ''' 
    x = x-axis movement distance,( meters) [-5,5]
    y = y-axis movement distance,( meters) [-5,5] 
    z = rotation about z axis ( degree)[-180,180]
    xy_speed = xy axis movement speed,( unit meter/second)  [0.5,2]

    '''
    ep_chassis.move(x=5.3, y=0, z=0, xy_speed=1).wait_for_completed()
 
    ep_chassis.move(x=0, y=0, z=-90, xy_speed=1).wait_for_completed()
    # ep_led.set_led(comp="all",r=255,g=100,b=0,effect="on")  
    ep_chassis.move(x=4, y=0, z=0, xy_speed=1).wait_for_completed() 
    ep_chassis.move(x=0, y=0, z=-90, xy_speed=1).wait_for_completed() 
    ep_chassis.move(x=5, y=0, z=0, xy_speed=1).wait_for_completed() 
    ep_chassis.move(x=0, y=0, z=-90, xy_speed=1).wait_for_completed() 
    ep_chassis.move(x=3, y=0, z=0, xy_speed=1).wait_for_completed() 
    ep_chassis.move(x=0, y=0, z=-90, xy_speed=1).wait_for_completed() 
    ep_chassis.move(x=2, y=0, z=0, xy_speed=1).wait_for_completed() 
    ep_chassis.move(x=3, y=0, z=-360, xy_speed=1).wait_for_completed() 
    








    '''
    x = speed in x direction( meter/second) [-3.5,3.5]
    y = speed in y direction( meter/second) [-3.5,3.5]
    z = rotation about z axis ( degree/second)[-300,300]
    '''
'''   ep_led.set_led(comp="all",r=0,g=0,b=255,effect="on")  
    ep_chassis.drive_speed(x=0.4,y=0,z=-20)
    time.sleep(12)
    ep_led.set_led(comp="all",r=0,g=255,b=0,effect="on") 
    ep_chassis.move(x=2.95, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp="all",r=100,g=255,b=0,effect="on") 
    
    
    ep_chassis.move(x=0.1, y=0, z=60, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp="all",r=0,g=0,b=255,effect="on") 
    ep_chassis.move(x=0.8, y=0, z=0, xy_speed=1).wait_for_completed()

    ep_chassis.drive_speed(x=0.2,y=0,z=-20.5)
    time.sleep(4)
    
    ep_chassis.move(x=2.8, y=0, z=0, xy_speed=1).wait_for_completed()

    
    
'''   
ep_camera.stop_video_stream()
print("Stopped video streaming.....")
ep_robot.close()
```

## MobileRobot Movement Image:

![robo](./img/robomaster.png)

## Initial Position:

![initial](https://github.com/vasundrasriravi/mobilerobot-openloopcontrol/assets/119393983/1724f8fc-1310-4b7b-b919-0953ce709d76)

## Final Position:

![final](https://github.com/vasundrasriravi/mobilerobot-openloopcontrol/assets/119393983/21aedecd-c7d3-41d6-bc32-652033a32468)


## MobileRobot Movement Video:

https://youtu.be/xkAumdRbGyU

## Result:
Thus the python program code is developed to move the mobilerobot in the predefined path.

```
Mobile Robotics Laboratory
Department of Artificial Intelligence and Data Science/ Machine Learning
Saveetha Engineering College
```
