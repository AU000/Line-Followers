# Line Follower Robot

A 3-wheel line follower robot built with 5 IR sensors, a small motor driver, and an Arduino. Two front-mounted drive wheels handle propulsion and steering, with a rear caster wheel for balance.

## Features
- 5-sensor IR array for line detection
- Real-time left/right correction to stay on the line
- Small H-bridge motor driver for two DC drive wheels

## Hardware
| Component | Notes |
|---|---|
| Arduino (Uno/Nano) | Main controller |
| 5x IR line sensors | Digital input, pins 2–6 |
| Motor driver | Small H-bridge module |
| 2x DC motors | Left/right drive wheels, pins 10–13 |
| 1x caster wheel | Rear balance wheel |
| Battery pack | Powers driver and Arduino |

## Wiring
| Signal | Arduino pin |
|---|---|
| IR sensor 1 (a1) | 2 |
| IR sensor 2 (a2) | 3 |
| IR sensor 3 (a3, center) | 4 |
| IR sensor 4 (a4) | 5 |
| IR sensor 5 (a5) | 6 |
| Left motor forward | 10 |
| Left motor backward | 11 |
| Right motor forward | 12 |
| Right motor backward | 13 |

## How it works
- Center sensor (a3) low → drive straight forward.
- Left sensors (a1/a2/a3) low → right motor forward, left motor stopped (turns left).
- Right sensors (a3/a4/a5) low → left motor forward, right motor stopped (turns right).

## Getting started
1. Wire the sensors, motor driver, and motors to the Arduino as listed above.
2. Open the sketch in the Arduino IDE.
3. Select your board and port, then upload.
4. Power the robot from the battery pack and place it on a line to test.

## Code
See the main sketch for the full motor control logic based on the 5 IR sensor readings.

## Project docs
Full project documentation (architecture diagram, components table, firmware) is in `line-follower-robot-docs.docx`.
