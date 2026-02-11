<h1>HP Otto: OttoOmni3</h1>

<img width="224" height="259" alt="Omni3" src="https://github.com/user-attachments/assets/8c5d614f-9c14-4652-89f1-eaff81cdd27e" />

STL files and build instructions can be found on [printables.com](https://www.printables.com/model/1501370-hp-otto-otto-omni3)


**otto3wd.py** is a required library for Otto Omni3, it contains the code for 3 wheel drive movement  

**rc.py** is a modified version of rc.py enabling control of Otto Omni3 via the new HP Otto phone app (currently (Mar 2026) in beta test and only available to purchasers of the HP Otto Starter https://www.facebook.com/groups/ottodiy/posts/3923882564421879/)  

<img width="512" height="229" alt="omni phone control" src="https://github.com/user-attachments/assets/fef739b8-49ea-45c7-babf-a410c796d6e8" />

The joystick control controls movement in any given direction, the D-pad control controls rotation of the robot.

<h3>Principle of three wheel omni movement</h3>

<img width="538" height="503" alt="omni movement" src="https://github.com/user-attachments/assets/04ccad06-3a8e-4de9-9a62-428a96484ca7" />

v1 = -Vx + angle_v  
v2 = cos60 Vx - sin60 Vy + angle_v  
v3 = cos60 Vx + sin60 Vy + angle_v  

so for a desired speed in a given direction(dir_angle) with a given speed of rotation(angular_v)  

vx = -speed * sin(dir_angle)  
vy = speed * cos(dir_angle)  
v1 = -vx + angular_v  
v2 = 0.5 vx - √3 / 2 * vy + angular_v  
v3 = 0.5 vx +√3 / 2  * vy + angular_v


<h3>Instructions</h3>  
Just drop rc.py and otto3wd.py in Otto's root directory.
