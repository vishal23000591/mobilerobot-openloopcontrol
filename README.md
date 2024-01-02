# MobileRobot-Openloopcontrol
## Aim:

To develop a python control code to move the mobilerobot along the predefined path.

## Equipments Required:
1. RoboMaster EP core
2. Python 3.7

## Procedure

Step1:

Use from robomaster import robot.

Step2:

Choose the x,y,z - axis movement distance(meters).

Step3:

Give ep_chassis.move to move straight.

Step4:

Give time.sleep() for a break.

Step5:

Give ep.chassis.drive_speed to have a circular movement.

## Program
```
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

    ep_chassis.move(x=0.6, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=0,b=0,effect="on")


    ep_chassis.move(x=0, y=0, z=-45, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=0,b=0,effect="on")

    ep_chassis.move(x=0.45, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=100,b=0,effect="on")

    ep_chassis.move(x=0, y=0, z=-30, xy_speed=1.5).wait_for_completed()
    ep_led.set_led(comp = "all",r=128,g=0,b=0,effect="on")
    
    ep_chassis.move(x=0.75, y=0, z=-30, xy_speed=1.5).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=0,b=255,effect="on")

    ep_chassis.move(x=0, y=0, z=-20,).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=255,b=255,effect="on")

    ep_chassis.move(x=0.6, y=0, z=20, xy_speed=1.5).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=128,b=255,effect="on")
    
    ep_chassis.move(x=0.5, y=0, z=50, xy_speed=1.5).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=0,b=128,effect="on")

    
    ep_chassis.move(x=1.4, y=0, z=25, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=128,g=0,b=0,effect="on")
    
    ep_chassis.move(x=0.55, y=0, z=0, xy_speed=1.5).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=204,b=255,effect="on")
    

    ep_chassis.move(x=0, y=0, z=-150, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=51,g=204,b=153,effect="on")
    
    ep_chassis.move(x=0, y=-1.6, z=0, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=153,g=204,b=0,effect="on")
    
    ep_chassis.move(x=0, y=0, z=30, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=102,g=102,b=0,effect="on")
    
    ep_chassis.move(x=1, y=0, z=-45, xy_speed=1.5).wait_for_completed()
    ep_led.set_led(comp = "all",r=184,g=69,b=128,effect="on")
    
    ep_chassis.move(x=0, y=0, z=-110, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=50,g=50,b=0,effect="on")\
    
    ep_chassis.move(x=0, y=-3.2, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=153,g=51,b=0,effect="on")

    ep_chassis.move(x=0, y=0, z=-35, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=255,b=153,effect="on")

    ep_chassis.move(x=0, y=-0.5, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=184,g=69,b=128,effect="on")
    
    ep_chassis.move(x=0, y=0, z=-95, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=51,g=204,b=204,effect="on")
    
    ep_chassis.move(x=-0.5, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=51,g=153,b=102,effect="on")
    
    ep_chassis.move(x=0, y=0, z=-20, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=51,g=51,b=51,effect="on")
    
    ep_chassis.move(x=-0.5, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=51,g=153,b=102,effect="on")
    
    
    ep_chassis.move(x=0, y=0, z=45, xy_speed=1.5).wait_for_completed()
    ep_led.set_led(comp = "all",r=184,g=69,b=128,effect="on")
    
    ep_chassis.move(x=0, y=-1.2, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=204,b=204,effect="on")

    ep_chassis.move(x=0, y=0, z=50, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=184,g=69,b=128,effect="on")

    ep_chassis.move(x=0, y=-1.2, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=151,g=153,b=102,effect="on")
    
   
    ep_chassis.move(x=0, y=0, z=45, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=184,g=69,b=128,effect="on") 


    ep_chassis.move(x=0.4, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=255,b=204,effect="on")


    ep_chassis.move(x=0, y=0, z=-45, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=128,g=128,b=0,effect="on")


    ep_chassis.move(x=0.7, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=192,g=192,b=192,effect="on")
    
    time.sleep(4)
    
    
    ep_camera.stop_video_stream()
    print("Stopped video streaming.....")


    ep_robot.close()
```

## MobileRobot Movement Image:

![robo](./img/robomaster.png)



## MobileRobot Movement Video:

Upload your video in Youtube and paste your video-id here

https://youtu.be/qihCu7dUxtE?si=j9rv9gHlcI6MLgw6

## Result:
Thus the python program code is developed to move the mobilerobot in the predefined path.




```
Mobile Robotics Laboratory
Department of Artificial Intelligence and Data Science/ Machine Learning
Saveetha Engineering College
```
