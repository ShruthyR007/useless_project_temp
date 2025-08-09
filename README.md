<img width="3188" height="1202" alt="frame (3)" src="https://github.com/user-attachments/assets/517ad8e9-ad22-457d-9538-a9e62d137cd7" />


# [Where's my Ball?] 🎯


## Basic Details
### Team Name: [NaanMushroom]


### Team Members
- Member 1: [Shruthy R] - [College of Engineering Trivandrum]
- Membeer 2: [Nandana M] - [College of Engineering Trivandrum]

### Project Description
[2-3 lines about what your project does]

### The Problem (that doesn't exist)
[What ridiculous problem are you solving?]
Honestly, there's no problem here. It's just a ball in a box. But we were sick of not knowing its exact spot at all times. You know, just in case someone wanted to know the completely useless, precise location of a ball. It's a question that keeps nobody up at night, and we felt it was our duty to answer it.

### The Solution (that nobody asked for)
[How are you solving it? Keep it fun!]
We pretty much built a whole tracking system just for fun. We put three ultrasonic sensors around the box to measure the distance to the ball. Then we used an Arduino to send that data to a computer, where some math (called trilateration) figures out its exact x, y coordinates. To make it even more pointless, we built a Pygame program that visualizes the ball's movement... but instead of a ball, it shows a randomly selected picture of Leonardo DiCaprio. So, yeah, we can tell you where the ball is, but we'll show you where Leo is instead.

## Technical Details
### Technologies/Components Used
For Software:
- [Languages used]-Python,C
- [Frameworks used] - Pygame
- [Libraries used] - Pyserial,random,math, NewPing
- [Tools used] - Arduino IDE

For Hardware:
- Arduino Uno, 3 x HC-SR04 Ultrasonic Sensors, Jumper Wires, and a Breadboard
- Ultrasonic Sensor Range: ~2 cm to 400 cm (depending on model)
- Arduino: Standard 5V, 16 MHz clock speed
- USB cable (for programming the Arduino), a computer

### Implementation
For Software:
# Installation
[commands]

# Run
[commands]

### Project Documentation
For Software:

# Screenshots (Add at least 3)
![Screenshot1](Add screenshot 1 here with proper name)

<img width="1714" height="1408" alt="Screenshot 2025-08-09 at 3 13 44 PM" src="https://github.com/user-attachments/assets/9ade4355-4683-4730-bf74-85b168bf6276" />

This code is for an Arduino sketch that uses the NewPing library to measure distances from three ultrasonic sensors. The code defines the trigger and echo pins for each of the three sensors (sonar1, sonar2, sonar3) and sets a max_distance of 100cm. It also declares integer variables d1, d2, and d3 to store the distance readings.

The setup() function initializes serial communication at a baud rate of 115200. The loop() function continuously pings each of the three sensors, reads the distance in centimeters, and assigns the values to d1, d2, and d3, respectively. There is a delay(500) at the end of the loop, causing the readings to be taken every half second. The code is designed to get the distance of a ball from three sensors, with the measurements stored in variables for further use.

![Screenshot2](Add screenshot 2 here with proper name)
<img width="1746" height="1536" alt="Screenshot 2025-08-09 at 3 17 02 PM" src="https://github.com/user-attachments/assets/2113068f-3b28-48fe-8b59-025090c75cf8" />
The Python code snippet defines a function trilaterate that calculates the coordinates of a point using trilateration. It takes three distances (d1, d2, d3) as input and uses the coordinates of three known points (left-bottom, right-bottom, and top-middle corners) to solve for the unknown point's location. The code first defines the three reference points and then uses a system of equations to compute the x and y coordinates, returning them as a tuple. It also handles the case where the determinant of the system is zero, returning None in that scenario.

![Screenshot3](Add screenshot 3 here with proper name)
<img width="1746" height="1536" alt="Screenshot 2025-08-09 at 3 23 03 PM" src="https://github.com/user-attachments/assets/7ff43bbd-88e0-47c9-9d1b-33614c61a67e" />
This Python script uses the pygame library to create a visual representation of a ball's location. The script reads serial data, presumably from an Arduino, which contains three distance measurements. It then uses a trilaterate function (not shown in this snippet) to calculate the ball's (x, y) coordinates from these distances. If the trilateration is successful, it converts the real-world coordinates into screen pixel coordinates and adds them to a path list. The program continuously runs in a loop, updating the ball's position on the screen, and stops when the user closes the window. It also includes error handling for incomplete data or invalid distance values received from the serial por

# Diagrams
![Workflow](Add your workflow/architecture diagram here)
*Add caption explaining your workflow*

For Hardware: 

# Schematic & Circuit
![Circuit](Add your circuit diagram here)
<img width="597" height="621" alt="image" src="https://github.com/user-attachments/assets/d88b7516-884f-44b9-bd7e-f06fabfde42a" />

The three ultrasonic sensors are wired to the Arduino, with sensor 1's trigger and echo pins connected to Arduino pins 2 and 3, respectively. Sensor 2's trigger and echo pins are connected to pins 4 and 5, and sensor 3's trigger and echo pins are connected to pins 6 and 7. The VCC and GND pins for all three sensors are connected to the Arduino's 5V and ground pins via a breadboard for simplified power distribution.

# Build Photos
![Components](Add photo of your components here)
*List out all components shown*

![Build](Add photos of build process here)
*Explain the build steps*

![Final](Add photo of final product here)
*Explain the final build*

### Project Demo
# Video
[Add your demo video link here]
*Explain what the video demonstrates*

# Additional Demos
[Add any extra demo materials/links]

## Team Contributions
- [Name 1]: [Specific contributions]
- [Name 2]: [Specific contributions]
- [Name 3]: [Specific contributions]

---
Made with ❤️ at TinkerHub Useless Projects 

![Static Badge](https://img.shields.io/badge/TinkerHub-24?color=%23000000&link=https%3A%2F%2Fwww.tinkerhub.org%2F)
![Static Badge](https://img.shields.io/badge/UselessProjects--25-25?link=https%3A%2F%2Fwww.tinkerhub.org%2Fevents%2FQ2Q1TQKX6Q%2FUseless%2520Projects)



