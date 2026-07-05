# IoT-Water-Pollution-RC-Boat
An IoT-based water quality monitoring system built on a radio-controlled (RC) boat. The boat carries multiple sensors, and streams live readings wirelessly to a handheld remote fitted with an LCD display — giving a low-cost, mobile way to check water quality at any point in a reservoir, instead of relying on a single fixed monitoring station.
Overview

Water pollution from industrial growth, agriculture, and weak regulation is a growing threat to drinking water and aquatic ecosystems. Fixed monitoring stations can't capture how pollution varies across a large body of water — parameters like pH and turbidity can differ significantly from one spot to another.

This project solves that with a boat that can be driven to any location on the water and take readings on demand. It combines:


A radio-controlled boat platform (hull, servo motors, propeller shaft, rudder)
A sensor unit (pH, turbidity, temperature) mounted on the boat
An Arduino-based control and data-acquisition system
An RF transmitter–receiver link for both boat movement and sensor data
A handheld remote with an LCD screen for real-time readings


Key Features


Mobile monitoring — the boat can be piloted to any point on a river, lake, or reservoir
Multi-parameter sensing — pH, turbidity (NTU), and temperature
Wireless data transfer — readings are sent over RF to the remote, no manual sampling needed
Real-time display — values shown instantly on an LCD at the controller
Low-cost & repeatable — readings are taken automatically every ~10 seconds while the boat is in the water
Durable hull design — mild-steel hull shaped to reduce water resistance, with buoyant sponge fittings for stable floating


System Architecture

The system is built in two independent halves that are then integrated together: the boat/propulsion unit and the water-quality sensing unit. Both share the same RF link back to the operator's remote.

1. Propulsion & Control Path
The operator uses an RF transmitter to send movement commands (left, right, forward, reverse). These are picked up by a two-channel RF receiver mounted on the boat. The receiver forwards the decoded signal to two 12V, 500 RPM servo motors, which drive the propeller shaft and rudder to steer and move the boat across the water.

2. Sensing & Data Path
Mounted on a plywood deck on top of the boat sits the sensing package: pH sensor, turbidity sensor, temperature sensor, an Arduino microcontroller, a transistor/switch circuit, and a second RF module. The Arduino polls all three sensors at a fixed interval (roughly every 10 seconds), computes the pH and turbidity readings, and pushes the combined result out over RF back to the remote control.

3. Remote/Display Unit
The handheld remote contains the RF transmitter (for boat control) and an LCD screen. As sensor packets arrive from the boat's RF module, the display updates with the current pH, turbidity, and temperature values — giving the operator an immediate read on water quality at that exact location.

4. Power
Both the propulsion system and the sensor/Arduino system draw from a 12V battery carried on the boat.
