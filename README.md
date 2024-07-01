Accident Detection System using Arduino, GPS, and GSM
Overview:
Accidents pose a significant risk to life and often result in higher death rates than many diseases, including cancer. To address this issue, we have developed a user-friendly accident detection system. This system leverages Arduino technology, along with GPS and GSM modules, to detect accidents and notify emergency contacts instantly.
![accident detection](https://github.com/g0kul-sengottaian/Accident-Detection-using-arduino/assets/159171191/c40d922c-a387-498a-946d-480f43a36a32)


Components:

Arduino UNO: The central microcontroller that processes all inputs and controls outputs.
MPU6050: An accelerometer and gyroscope module used to detect the bike's tilt.
Force Sensing Resistor (FSR): Detects if the driver is on the seat or not.
GPS Module: Provides real-time location data.
GSM Module: Sends SMS notifications to emergency contacts.
Buzzer: Emits a sound alert when an accident is detected.
Project Description:
This system detects accidents by monitoring the bike's tilt and the driver's position. If an accident is detected, the system sends the bike's current location to predefined contacts, such as family members and an ambulance driver. Below are the three test cases that the system is designed to handle:

Test Case 1: Detecting Bike Tilt

Objective: To determine if the bike has fallen.
Method: The MPU6050 sensor monitors the bike's orientation. When the tilt exceeds a certain threshold value, the system predicts that the bike has tilted or fallen.
Outcome: If the tilt threshold is exceeded, the system proceeds to the next test case to determine the driver's status.

Test Case 2: Checking Driver's Position

Objective: To check if the driver is still on the seat after the bike has tilted.
Method: The Force Sensing Resistor (FSR) detects whether the driver is on the seat. If the driver is not on the seat, it indicates a potential accident where the driver might have been thrown off.
Outcome: If the driver is off the seat, the system sends the current GPS location to family members and the ambulance driver via the GSM module.

Test Case 3: Driver Response Check

Objective: To determine if the driver needs help when the bike is tilted, but the driver is still on the seat.
Method: When the bike tilts and the driver is on the seat, the system triggers a buzzer for 15 seconds. If the driver turns off the buzzer within this time, it indicates they are alright. If the buzzer is not turned off, it means the driver may need help.
Outcome: If the buzzer is not turned off, the system sends the current GPS location to family members and the ambulance driver.
This project aims to enhance road safety by providing immediate assistance during accidents, potentially saving lives by reducing the response time of emergency services.






