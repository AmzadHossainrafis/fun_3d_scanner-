# Project Title: Small 3D Object Modeling

This is an university  fun project .  main perpose of this project is to  create and prototype that  only try to scan any object(not so big ) by using ir distance sensor any try to plot it in 3d dimension space 


# Objectives

1.	To scan a small 3D object.
2.	To remake the 3D object after scanning.


# Components

3* 1 x Arduino Uno/Nano
* 2 x NEMA17 Stepper Motors
* 1 x IR Sensor
* 2 x Stepper Motor Drivers
* 1 x SD Card
* 1 x SD Card Reader Module
* 1 x PCB/Bread Board
* 1 x 12 volt Power Adapter/Battery
* 1 x 8 mm Threaded Rod
* 2 x 8 mm Smooth Rod
* 4 x Linear Bearing
* Connecting Wires
* Zip Ties
* Nuts and Screws
* MESHLAB/MATLAB

# Descriptions

<p>To print or make a 3D object, we first need the 3D image or design file. When we have the image or design file, we can print the object. In this project we will not make new 3D object. We will scan a 3D object to get a copy of 3D image or 3D design file which can be used to reprint or remake that object later. To do this we will make a machine using Arduino to scan 3D object. This machine will be able to scan small 3D objects with dimensions up to 13cm in the X and Y directions. We will place a small 3D object on a rotating table in its own axis. The table will rotate horizontally with the small 3D object on it by using a NEMA17 motor. Another NEMA17 motor will be used to move the IR sensor vertically while the table is rotating horizontally with the 3D object. The IR sensor will scan the 3D object during these motion and will save the data on a SD card. The IR sensor will give a direct analog output according to the measured distance. Four linear bearing, one threaded rod and two smooth rod will be used along with NEMA17 motor to move the IR sensor vertically. After completing the scanning we will remove the SD card and copy the text file of scanned data saved on SD card to a computer. We will import the text file in MESHLAB or MATLAB and using MESHLAB or MATLAB we will generate the 3D image of the object in STL or OBJ format. Using that STL or OBJ file we can print the 3D object by a 3D printer. A rough picture drawn by hand of our planned machine structure is given below. We will take it to any 3D print servicing shop and describe it to the shopkeeper to design the structure in STL or OBJ format with suitable software and get it printed by a 3D printer.</p>
  
  
  
# connection 
  
<p align="right"><img src="result2.jpg"\></p>
<p align="right"><img src="Front_motor_top.stl"\></p>
  
# 3D print component 


   
# demo result 

<p align="right"><img src="result2.jpg"\></p>
  

