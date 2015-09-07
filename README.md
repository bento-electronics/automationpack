Automation Pack
===================

Your automation kit contains 9 different modules. Some are input (sensors), some are output, and the Bluetooth module is used for control from e.g. a smartphone or computer.

Pinouts, datasheets, and sample code are included in the folder for each module, and tutorial links are below!

----------

Ultrasonic Sensor HC-SR04
-------------
The HC-SR04 is a very widely used ultrasonic rangefinder. It times the reflection of transmitted ultrasonic waves to measure the open-air distance directly in front of it. Effective range is between 4cm and 4m, but has been tested up to 20m with reduced precision.

Note that there is a library provided for this sensor, but it is also possible to interface with the echo and triangulation pins manually, allowing a greater degree of control over the measurements. Tutorials for both are below.
> 
> http://arduinobasics.blogspot.com/2012/11/arduinobasics-hc-sr04-ultrasonic-sensor.html
> http://www.instructables.com/id/Simple-Arduino-and-HC-SR04-Example/step3/Upload-the-sketch/
> http://forum.arduino.cc/index.php?topic=106043.0
> http://randomnerdtutorials.com/complete-guide-for-ultrasonic-sensor-hc-sr04/
> http://playground.arduino.cc/Code/NewPing

--------

Bluetooth Serial Transceiver HC-05
-------------
HC-05 is a popular Bluetooth module used to emulate a UART (Universal Asynchronouse Receiver/Transmitter) interface over the Bluetooth wireless protocol. Operation is meant to be very simple; either side of the serial connection can simply write to and read bytes from the other side.

Hooking this module up to the existing TX/RX pins on an Arduino will allow you to immediately send and receive data using the built in hardware serial library. However, this connection is also used by the board when connected to your computer via USB, which means you will need to disconnect HC-05 everytime you upload new code. The solution is to use Arduino's SoftwareSerial library to create a UART connection on two other pins of your selection.

**NOTE:** Always remember to cross TX/RX wires when connecting UART devices. i.e., TX from one side connects to RX on the other side, and vice versa. 

> http://www.instructables.com/id/Arduino-AND-Bluetooth-HC-05-Connecting-easily/
> http://arduinofy.blogspot.com/2013/10/tutorial-programming-hc-05-at-mode-with.html
> http://www.martyncurrey.com/arduino-with-hc-05-bluetooth-module-in-slave-mode/
> https://www.arduino.cc/en/Reference/SoftwareSerial
> https://www.arduino.cc/en/Reference/Serial

----------

9g Microservo
-------------
Your automation kit comes with two small servos, good for building small robots or generally moving light loads. The included servo-horns allow you to screw in larger gears or fasteners.

These servos are controlled by the standard servo library, and can simply be set to any angle between 0 and 180 degrees.

> http://playground.arduino.cc/Learning/SingleServoExample
> https://learn.adafruit.com/adafruit-arduino-lesson-14-servo-motors/arduino-code-for-sweep
> http://www.adafruit.com/products/169

----------

Smoke/gas detector MQ-2
-------------
The MQ-2 smoke sensor is useful for building fire alarms into home automation projects, or for any other project where smoke is expected! It is also sensitive to certain gases like methane and carbon monoxide, so you can use it to detect those too.

This module has a simple analog output with voltage increasing whenever more smoke/gas is detected. The value can be read from the connected analog pin using analogRead(). There is also a digital output that is HIGH once a certain threshold of gas concentration is crossed.

**Warning:** This sensor gets hot after operating for a while, so avoid touching it!

> http://www.instructables.com/id/How-to-use-MQ2-Gas-Sensor-Arduino-Tutorial/#step1
> http://vanceance.blogspot.com/2013/04/gas-sensor-with-arduino.html


----------

Real Time Clock DS1302
-------------
This module can be used to track the exact date and time without any sort of internet syncing/connectivity, and includes a small coin battery to keep it operated for long periods of time. However, the communication protocol is quite involved so using the DS1302 library is recommended.

> http://playground.arduino.cc/Main/DS1302RTC


----------


PS2 Joystick
-------------
An X/Y joystick similar to those found in the PS2 controllers. There are two analog voltage outputs representing X and Y position, and should be hooked up to separate ANALOG IN inputs.
> https://www.sparkfun.com/tutorials/272


----------


Temperature sensor DS18B20
-------------
Based on the DS18B20 sensor, outputs exact measured temperature in Celsius over a custom digital protocol. Refer to the datasheet and Arduino library for specific details.
> https://www.sparkfun.com/products/245

----------

Humidity Sensor DHT11
-------------
> Based on the DHT11 sensor, outputs exact measured humidity over a custom digital protocol. Refer to the datasheet and Arduino library for specific details.
> https://www.adafruit.com/products/386

----------

5V Power Relay
-------------
> Can switch high-current loads on or off at 5V, controlled by a single digital pin from Arduino. Use this for high power outputs, e.g. DC motors or incandescent lamps, which usually require a separate power supply, and cannot safely be driven direct from Arduino pins.
> http://shop.evilmadscientist.com/productsmenu/tinykitlist/544
