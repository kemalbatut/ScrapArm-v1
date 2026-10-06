# 🏭 Industrial Robotics & Automation Training

ScrapArm v1 was built as a small hands-on robotics project, but my robotics learning also included invited practical sessions around industrial robots, collaborative robots, and automation equipment.

This document keeps those experiences separate from the prototype itself: the industrial equipment shown here is **training equipment I studied and interacted with**, not hardware that is part of ScrapArm.

## Training environment

![Industrial robot session](../media/industrial-robot-session.jpg)

![Robot instruction](../media/robot-instruction.jpg)

![Automation cell](../media/automation-cell.jpg)

## Concepts connected to the training

### Industrial robot axes and motion

Industrial manipulators use coordinated servo-controlled axes. A major conceptual difference from ScrapArm is that the controller manages the entire robot as one kinematic system rather than as unrelated motors.

### Coordinate systems

Robot programming requires thinking in multiple frames:
- joint/axis coordinates;
- world coordinates;
- base coordinates;
- tool coordinates.

This is a key next step beyond direct joint-angle commands.

### Motion types

Industrial robot work commonly distinguishes between:
- point-to-point motion;
- linear/tool-path motion;
- circular/path-based motion;
- controlled speed/acceleration behavior.

### Teach pendant workflow

Industrial robots are commonly commissioned and programmed using a teach pendant/controller interface to:
- jog axes;
- define points;
- inspect coordinate frames;
- build motion sequences;
- adjust speed;
- test robot programs.

### Collaborative robots

Cobot training adds a strong emphasis on the application around the robot:
- human interaction;
- safe speed/force behavior;
- risk assessment;
- emergency-stop concepts;
- cell layout;
- end-effector hazards.

A collaborative robot alone does not automatically make an application safe.

### Automation systems

The automation training environment also showed how robot arms fit into a larger system with:
- sensors;
- pneumatics;
- actuators;
- conveyors/transfer systems;
- industrial I/O;
- control panels;
- process sequencing.

That broader system view is one of the main lessons I want to bring into future versions of my own robotics projects.

## How this changed ScrapArm

Before this exposure, ScrapArm was mainly a goal of "make the arm move."

After seeing larger automation systems, the roadmap became more structured:
- calibrate joints;
- define safe ranges;
- create a home position;
- coordinate multiple joints;
- think in coordinate frames;
- separate power/control more cleanly;
- add feedback where useful;
- treat the robot as one part of a complete system.
