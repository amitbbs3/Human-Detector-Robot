# Human Detector-Robot


## COMPONENTS REQUIRED:

**1. Printed Circuit Board (PCB)**

A **printed circuit** board, or **PCB** , is used to mechanically support and electrically connect the electronic components using conductive pathways, tracks or signal traces etched from copper sheets laminated onto a non-conductive substrate.

Here in this project we are using a plain PCB, which will provide a platform to interconnect the different components as per the circuit and arrange the devices efficiently to make the product compact & attractive.

![](RackMultipart20221020-1-41bivy_html_6131ee3912bf2c0c.jpg)
![image](https://user-images.githubusercontent.com/57197424/197012363-12eb1d91-c0a1-4871-a789-b35151c40c82.png)
                 **Fig .01.** APlain PCB


**2. Arduino Uno**

Arduino is an open-source platform used for building electronics projects. Arduino consists of both a physical programmable circuit board and a piece of software, or IDE (Integrated Development Environment) that will run on our computer, used to write and upload computer code to the physical board.

This microcontroller board is based on the ATmega328P. It has 14 digital input/output pins (of which 6 can be used as PWM outputs), 6 analog inputs, a 16 MHz quartz crystal, a USB connection, a power jack, an ICSP header and a reset button. It contains everything needed to support the microcontroller; simply we will connect it to a computer

with a USB cable and power it with a battery to get started.

The Arduino platform has become quite popular nowadays just starting out with electronics, and for good reason. Here with Arduino unlike the most previous programmable circuit boards, it does not need a separate piece of hardware (called a programmer) in order to load new code onto the board -- we can simply use a USB cable. Additionally, the Arduino IDE uses a simplified version of C++, making it easier to learn to program.

**3. PIR Motion Detection Sensor HC-SR501**

The PIR Sensor module allows us to sense motion of a living thing radiating infra-red radiations. It is almost always used to detect the motion of a human body within the sensor's range. It is often referred to used "PIR", "Pyroelectric", "Passive Infrared" and "IR Motion" sensor.

The module has an on-board pyroelectric sensor, conditioning circuitry and a dome shaped Fresnel lens. The PIR sensor module provides an output "HIGH" when a human body is detected within its range and an automatic Delay "LOW" when the body leaves its range. The delay time is adjustableusing the potentiometer on-board. The minimum delay time that can be set is 5 seconds and maximum of 200 seconds.

The blocking time potentiometer is also provided on-board to set the blocking time during which the sensor does not respond to any change in motion. The minimum blocking time that can be set is 2.5 seconds and maximum of 10 seconds.

![image](https://user-images.githubusercontent.com/57197424/197013279-59a0122e-402c-4853-8ca5-b139fb471c58.png)


**Fig .02.** Fresnel lens & PIR sensor

**4. Motor Driver IC (L293D)**

L293D is a dual H-bridge motor driver integrated circuit (IC). Motor drivers act as current amplifiers since they take a low-current control signal and provide a higher-current signal. This higher current signal is used to drive the motors.

L293D contains two inbuilt H-bridge driver circuits. In its common mode of operation, two DC motors can be driven simultaneously, both in forward and reverse direction. The motor operations of two motors can be controlled by input logic at pins 2 & 7 and 10 & 15. Input logic 00 or 11 will stop the corresponding motor. Logic 01 and 10 will rotate it in clockwise and anticlockwise directions, respectively.

Enable pins 1 and 9 (corresponding to the two motors) must be high for motors to start operating. When an enable input is high, the associated driver gets enabled. As a result, the outputs become active and work in phase with their inputs. Similarly, when the enable input is low, that driver is disabled, and their outputs are off and in the high-impedance state.


**5. Buzzer**

A buzzer or beeper is an audio signaling device, which may be mechanical, electromechanical, or piezoelectric. Typical uses of buzzers and beepers include alarm devices, timers and confirmation of user input such as a mouse click or keystroke.

Herein our project it is connected to the Arduino and it beeps when Arduino outputs HIGH after detecting the humans' presence by the PIR sensor.


**6. LEDs**

The lighting emitting diode is a p-n junction diode. It is a specially doped diode and made up of a special type of semiconductors. When the light emits in the forward biased, then it is called as a light emitting diode or LED.

When the diode is forward biased, then the electrons & holes are moving fast across the junction and they are combining constantly, removing one another out. Soon after the electrons are moving from the n-type to the p-type silicon, it combines with the holes, then it disappears. Hence it makes the complete atom & more stable and it gives the little burst of energy in the form of a tiny packet or photon of light.




**THEORY**** :**

Our PIR sensor is an electronic sensor that measures infrared (IR) light radiating from objects in the field of view. They are often used in PIR-based motion detectors.

All the living things continuously emit heat energy in the form of radiation. Usually this radiation isn't visible to the human eye because it radiates at infrared wavelengths, but it can be detected by electronic devices designed for such a purpose.

Infrared radiation enters through the front of the sensor (Fresnel lens increases the coverage area), called as the 'sensor face'. At the core of a PIR sensor is formed of solid state sensor or set of sensors which is made from pyroelectric materials—the materials which generate energy when exposed to heat.

The term _passive_ in this context refers to the fact that PIR devices do not generate or radiate energy for detection purposes. The PIR sensors only detect infrared (IR) radiation emitted by or reflected from objects. They cannot detect or measure "heat".

We are also using L293D motor driver IC. This IC is required to drive the motor and also eliminates back EMF generated. This IC internally has H-bridge circuit. The IC has 16 pins out of which 4 input pins drive the motor. Enables are used to enable these input pins. A 9v power is supplied at the 16th pin to operate the IC.

So when the PIR sensor will face human being in its front coverage area, the irradiating IR waves will activate our sensor and the input will be high in the Arduino. Consequently, the Arduino will provide the HIGH signal to the LED and the motor driving IC. For input 00 or 11 the motors will be stopped and for the inputs 01 or 10 the corresponding motors will rotate in clockwise and anticlockwise directions respectively. Based on these instructions from Arduino our robot will continue to move in forward direction but as soon as it detects human presence it will retreat back and the LED, buzzer will signify it evidently which is purposeful to alert for different conditions.

**CIRCUIT DIAGRAM:**

![image](https://user-images.githubusercontent.com/57197424/197013700-18c93bd2-d1ea-4640-84e6-628d178ca778.png)
**Fig.** Circuit Diagram

**PROCEDURE:**

- Connect the Arduino to the computer via USB.
- As per the circuit diagram shown above connect the inputs and outputs on the Arduino. The input from the PIR is connected to digital pin 2.
- Pin 13 is used to give output to LED, Pin 10 is connected to buzzer as output.
- Pin 3,4 and 5,6 are used as output Pins for our DC motors.
- All the components are arranged compact on the chassis.
- Burn the code.
- While the robot is moving if any human detected by the PIR sensor robot stops moving and the buzzer and LED is switched on.


**WORKING:**

- We are implementing the PIR Human Detection in our project as a form of a robot.
- The robot will move forward with the help of the 300 RPM DC motors.
- The PIR Sensor will be attached in the front part of the robot and as soon as it detects a human or an animal in front, it will start moving backwards.
- It will also indicate the presence of a human by LEDs.
- All of these functions will be coded on our Arduino board and the board will control all the other components attached.
- We are using a Motor Driver IC instead of directly connecting the DC motors to the Arduino because DC motors work on high voltage (about 9V – 12V) and the Arduino works on 5V so if we connect a 9V battery directly to the Arduino, it will damage it.
- Hence L293D IC is used as motor driver IC to control the motors.

**ARDUINO CODE:**

![image](https://user-images.githubusercontent.com/57197424/197014006-5c6765e2-0b24-41c7-8dcc-8183c85a696e.png)


**Fig ** Arduino IDE Code - I

![image](https://user-images.githubusercontent.com/57197424/197014072-cd6424dd-781e-4f2e-b3d3-a3d8e5db0ab1.png)

**Fig.** Arduino IDE Code - II

**APPLICATIONS:**

**Dynamic Home Security Alarm**

![image](https://user-images.githubusercontent.com/57197424/197014165-5e4054a4-5ac6-4a36-a94d-cccfe3d610f3.png)


**Fig.** Home/Office Security System

**Home Automation**

![image](https://user-images.githubusercontent.com/57197424/197014287-21669f56-d39e-4bc1-bc17-395523dbfa96.png)
**Fig.** House appliances controlled using different sensors

**Disaster Management**

![image](https://user-images.githubusercontent.com/57197424/197014316-02a47e54-0bdf-4bad-8097-4375f592ab6a.png)
**Fig.** Rescue Operation going on after earthquake

**MODEL LAYOUT:**

- We are planning to showcase our project's capabilities in the scenario of a disaster like earthquake or tsunami.
- Human Detector Robot will move in debris and search for human signatures and show the presence of human being by blinking the LEDs and sounding the buzzer.
- After detection it will pause for sometime and move forward for detecting other people who need help.

**CONCLUSION:**

In the end this project was a great experience for all of us. It didn't only teach us about concepts of digital electronics it taught us teamwork, we learned how to work with other people forgetting our difference of opinions and made this project a successful one. We learned how the concept of human detection works and how can we use it in our daily lives. Finally we are presenting our project in which we have used PIR Sensor along with Arduino UNO to ease out the process of human detection and use it in disaster management.
