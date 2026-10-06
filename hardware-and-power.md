# ⚡ ScrapArm v1 — Hardware & Power Notes

This document records the hardware-side lessons from ScrapArm v1.

## System blocks

```text
Arduino Controller
      │
      ├── Base servo signal
      ├── Shoulder servo signal
      ├── Elbow servo signal
      └── Gripper servo signal

External regulated 5 V supply
      │
      └── Servo power rail

Controller ground ───────┐
                         ├── Common electrical reference
Servo supply ground ─────┘
```

## 4-DOF mechanical functions

| Function | Role |
|---|---|
| Base | Rotates the complete arm |
| Shoulder | Provides main lifting movement |
| Elbow | Changes reach/articulation |
| Gripper | Opens/closes the end effector |

## Power testing

The bench supply used during documented testing was configured to **5.00 V** with a **3.00 A current limit**.

![Bench power supply](../media/bench-supply.jpg)

The displayed current setting is a current limit, not a measurement of continuous system consumption.

### Why external servo power matters

Servo current can rise sharply when:
- starting;
- reversing direction;
- accelerating load;
- several joints move together;
- a mechanism pushes against a hard stop.

For that reason, multi-servo actuator power should not be treated the same way as microcontroller logic power.

## Common ground

The servo control signal is interpreted relative to ground. When the Arduino and servo power source are separate, they still need a common reference.

## Mechanical/electrical integration

The electrical design cannot be separated completely from mechanics.

Cable routing must account for:
- joint rotation;
- slack;
- connector strain;
- moving linkages;
- pinch points;
- reach at extreme positions.

## v2 electrical goals

- cleaner power distribution;
- stronger connectors;
- documented pin map;
- cable strain relief;
- cleaner routing;
- startup/home sequence;
- servo range calibration;
- dedicated driver/distribution hardware if required.
