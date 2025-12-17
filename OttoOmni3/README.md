<h1>HP Otto: OttoOmni3</h1>

link to printables  
rc.py is a modified version of rc.py enabling control of Otto Omni3 via the new HP Otto phone app (currently (Dec 2025) in beta test and only available to purchasers of the HP Otto Starter)  

otto3wd.py is a required library for Otto Omni3, it contains the code for 3 wheel drive movement  

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

