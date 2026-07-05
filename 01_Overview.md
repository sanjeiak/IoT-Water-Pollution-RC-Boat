# IoT Water Pollution Monitoring in Rivers and Lakes using RF Signal-Controlled RC Boat

An IoT-based Unmanned Surface Vehicle (USV) that monitors water quality in rivers, lakes, and reservoirs in real time. The boat carries a full sensor array (pH, turbidity, temperature, dissolved oxygen, and conductivity), a GPS module for location tagging, and an Arduino UNO R4 WiFi–based control system that pushes every reading both online to a live web dashboard and offline to a local SD card, so no data is ever lost regardless of network availability. The boat itself is remotely piloted over a dedicated RF link, giving operators the ability to sample water quality at any point across a large body of water instead of relying on a single fixed monitoring station.

## Problem Statement

Water pollution from industrial growth, agriculture, and weak environmental regulation is a growing threat to drinking water sources and aquatic ecosystems. Existing monitoring approaches typically rely on **fixed sensor stations**, which have three major limitations:

- They only capture data from one location, even though pollution levels can vary significantly across different points of the same river or lake.
- Manual sampling is slow, labor-intensive, and often impractical for large or hard-to-reach water bodies.
- In many regions, monitoring infrastructure is either absent or provides no way to check water quality without physically travelling to each site — and there's often no reliable network connection out on the water itself.

As a result, pollution incidents can go undetected until they have already impacted public health, wildlife, or drinking water supplies.

## Solution

This project replaces the fixed-station approach with a **cost-effective, remotely-operated RC boat** that carries the entire sensing and communication system directly to the point of interest.

- A mild-steel hull with sponge floats carries five water-quality sensors, a GPS module, and an Arduino UNO R4 WiFi–based control system.
- The operator drives the boat to any location on the water using a 2-channel RF link, and the onboard sensors take readings on demand.
- Every reading is GPS- and time-tagged, then sent down **two independent data paths simultaneously**: over Wi-Fi to a live web dashboard when internet access is available, and to an onboard SD card so nothing is lost when it isn't.
- A local LCD display also shows the current status directly on the boat, so readings are visible even without a phone or laptop nearby.

This gives a single low-cost boat the ability to do what would otherwise require many fixed sensor stations — while still working reliably in remote or offline areas.

## Features

- **Mobile, on-demand monitoring** — pilot the boat to any point on a river, lake, or reservoir instead of relying on one fixed location
- **Multi-parameter sensing** — pH, turbidity (NTU), temperature, dissolved oxygen (DO), and conductivity
- **GPS-tagged readings** — every measurement is stamped with its exact location for pollution mapping
- **Dual data path (online + offline)** — readings are sent live to a web dashboard over Wi-Fi and simultaneously logged to an SD card, so data is never lost in areas with no network coverage
- **Independent RF control link** — boat steering works over a dedicated 2-channel RF connection, separate from Wi-Fi
- **On-board local display (HMI)** — an LCD on the boat shows live status without needing a separate device
- **Low-cost, durable build** — mild-steel hull with sponge floats, driven by two 12V servo motors via a servo motor driver
- **Centralized power management** — a single 12V battery and power management unit (PMU) regulate and distribute power to every subsystem
