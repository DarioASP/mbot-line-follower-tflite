This project implements an autonomous mobile robot using an mBot Mega and two Raspberry Pi 4 boards, combining computer vision, neural networks, and embedded systems.
The system detects and follows road lines, classifies traffic signs, and sends movement commands to the mBot via serial communication.

System Overview:

Raspberry Pi #1:
Runs a pre-trained neural network to recognize traffic signs (e.g., Stop, Turn). Sends a character via Bluetooth to Raspberry Pi #2 based on the detected sign.

Raspberry Pi #2:
Processes images with OpenCV to detect lines and calculate driving angle and direction. Combines this with the signal from Raspberry Pi #1, then sends commands via serial to the mBot Mega.

mBot Mega (Arduino + FreeRTOS):
Receives angle and direction data to control the motors. Uses FreeRTOS with multiple tasks and interrupts for real-time motor control.

Communication:
Bluetooth between Raspberry Pi #1 and Raspberry Pi #2, serial (UART) between Raspberry Pi #2 and mBot Mega

Technologies Used:
Python · OpenCV · TensorFlow Lite,
FreeRTOS · Arduino (mBlock libraries),
Raspberry Pi · Bluetooth · Serial communication

![image](https://github.com/user-attachments/assets/753b07a7-8b27-4b0b-8bdc-279a3f101c7d)

![image](https://github.com/user-attachments/assets/95a9baac-1395-4850-8135-41c0786ed940)
