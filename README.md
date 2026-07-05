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


