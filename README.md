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
  
 # Over view 
 <p align="center"><img src="full_view.png"\></p>
  

# 3D print component   

[example 1 ->](https://github.com/AmzadHossainrafis/fun_3d_scanner-/blob/master/Base_body.stl)
[example 2 ->](https://github.com/AmzadHossainrafis/fun_3d_scanner-/blob/master/Coupler.stl)


  
# connection 

<p align="right"><img src="connection diagram.png"\></p>
   


# Methodology

<p>The push button is used to start the scanning process. We have connected Vref to 3.3V. Because maximum voltage of the sensor is 2.4V. To increase precision we use external voltage reference for thr Ac to DC conversion. We have connected all the components on a breadboard. There are two 47uF capacitors for each of the motor drivers.
This machine will be able to scan small 3D objects. We will place a small 3D object on a rotating table in its own axis. The table will rotate horizontally with the small 3D object on it by using a NEMA17 motor. Another NEMA17 motor will be used to move the IR sensor vertically while the table is rotating horizontally with the 3D object.
The distance between sensor and center of the turning table is 8cm. The turning table rotates 360/200 = 1.8 degree at a time to make 200 steps. The sensor measure the distance from the sensor to object point. If we subtract the measured distance from the distance between sensor and center of the turning table we get the distance between the object point and the center of the turning table. The IR sensor will give a direct analog output according to the measured distance between 0 and 1023. We can convert it to voltage by the following formula and then convert it to distance.
				Voltage = (Analog Output * 3.3)/1023
Distance = -5.40274*pow(Voltage, 3) + 28.4823*pow(Voltage, 2) – 49.7115*Voltage + 31.3444
We found these formula from the datasheet of the sensor. The distance can be thought of as hypotenuse of a triangle. So
					x = sin(1.8 degree) * Distance
					y = cos(1.8 degree) * Distance
The z axis will be measured from 0 to 12 cm adding 2mm each time.
	
	
# Results and discussion
	
The IR sensor will scan the 3D object during these motion and will save the data on a SD card. Four linear bearing, one threaded rod and two smooth rod will be used along with NEMA17 motor to move the IR sensor vertically. After completing the scanning we will remove the SD card and copy the text file of scanned data saved on SD card to a computer. We will import the text file in MESHLAB using MESHLAB we will generate the 3D image of the object in STL or OBJ format. Using that STL or OBJ file we can print the 3D object by a 3D printer..
	
### Output 	
<p align="center"><img src="tout.PNG"\></p>


### Output voltage 


<p align="center"><img src="voltage.PNG"\></p>


	
	
	

# References

I have to learn many thing about arduino around hole internet as I don’t have any basic knowledge about Arduino all the references links are given below    
*	https://www.makerguides.com/sharp-gp2y0a710k0f-ir-distance-sensor-arduino-tutorial/ (IR sensor) 
*	https://www.youtube.com/watch?v=0qwrnUeSpYQ (stepper motor )
*	https://www.arduino.cc/en/tutorial/stepperSpeedControl (stepper motor )

*	https://create.arduino.cc/projecthub/electropeak/sd-card-module-with-arduino-how-to-read-write-data-37f390(SD card )

* https://www.youtube.com/watch?v=d8_xXNcGYgo&list=PLGs0VKk2DiYx6CMdOQR_hmJ2NbB4mZQn-(arduino tutorial )

* https://www.youtube.com/watch?v=sS_oW81NweI (sd card module connection )

 




  

