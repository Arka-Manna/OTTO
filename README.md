# OTTO
This project features an Otto DIY robot controlled by an Arduino Nano, with a touch sensor to switch between different movement modes.
Components:
Arduino Nano: The microcontroller used to control the robot.
Otto DIY Robot: A small, 3D-printed robot with four servos to control its legs and feet, allowing it to walk, dance, and perform other actions.
Touch Sensor: A sensor connected to the Arduino that detects when it is touched and changes the robot's mode accordingly.
Buzzer: A small speaker used to play sounds, providing audio feedback when the robot's mode changes.
Working Explanation:
Setup Phase:

Pin Definitions: The robot’s legs and feet are controlled by servos connected to specific pins on the Arduino Nano. These pins are defined at the beginning of the code (LeftLeg, RightLeg, LeftFoot, RightFoot).
Initialization: The setup() function initializes the Otto robot by specifying which pins control the servos and the buzzer. The touch sensor is also set up as an input.
Startup Sound: When the robot is powered on, it plays a sound using the buzzer to indicate it is ready.

# Main Loop:

Touch Detection: The robot continuously checks the touch sensor in the loop() function. If the sensor detects a touch, it triggers the changeMode() function to switch to the next movement mode.
Mode Execution: The robot performs different actions based on the current mode, which are predefined in the performMove() function. For example, it can walk, turn, bend, shake its leg, or perform specific dance moves.
Sound Feedback: Each time the mode changes, the robot plays a unique sound, providing feedback that the mode has switched.
Movement Modes:

# The robot has a total of 14 modes (totalModes = 14), each associated with a different action:
-Walking forward and backward.
-Turning left and right.
-Bending forward and backward.
-Shaking its leg.
-Moonwalking (left and right).
-Crusaito (a side-to-side motion).
-Flapping its arms (legs in this case).
-Jumping.
-Custom dance moves.

# Mode Control:

Each time the touch sensor is activated, the robot switches to the next mode in the sequence. When it reaches the last mode, it loops back to the first mode.
The movements in each mode are defined in the performMove() function. If a movement is triggered, it is performed, and the robot then waits for the next touch input to switch modes.
# How to Use:
Assembling the Robot:

Attach the four servos to the Otto robot’s legs and feet.
Connect the servos to the Arduino Nano using the pins defined in the code.
Attach the touch sensor to a suitable part of the robot where it can be easily touched.
Connect the buzzer to the Arduino for sound feedback.
Powering On:

When you power on the robot, it will play a startup sound to indicate it is ready.
Changing Modes:

Touch the sensor to change the robot’s mode. The robot will perform the corresponding action and play a sound to indicate the change.
You can continue touching the sensor to cycle through all the available modes.
Resetting:

The robot automatically resets to the home position when it completes a mode cycle, or if it’s in a mode with no specific action, ensuring it's ready for the next command.
