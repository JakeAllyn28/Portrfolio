# Vehicle Physics System Architecture

**Context:** Visual Concepts (NBA 2K Series)  
**Stack:** C++, proprietary engine  
**Focus:** Real-Time Physics, Gameplay Systems  

---

## Overview

Designed and owned a modular vehicle physics system used across multiple NBA 2K titles. The system supports a wide range of vehicle types—including cars, bikes, skateboards, and air vehicles—while maintaining consistent gameplay feel and performance across platforms.

The primary goal was not strict physical realism, but controllable, responsive behavior that could be tuned by designers while remaining stable in multiplayer environments.

---

## Problem

- Traditional physics approaches were too rigid or expensive for gameplay use
- Different vehicle types required different handling models but needed a shared framework
- Systems had to remain stable under networked/multiplayer conditions
- Designers needed control without modifying code

---

## Solution

Built a modular vehicle physics architecture with:

- Shared base physics layer (forces, integration, collision)
- Vehicle-specific handling modules layered on top
- Parameter-driven tuning system for designers
- Tight integration with animation and input systems

Focused heavily on separating:
- simulation logic  
- tuning/configuration  
- presentation  

---

## Key Features

- Multi-vehicle support (ground + air)
- Arcade-style handling with physically-informed behavior
- Tunable parameters for traction, acceleration, suspension, and control response
- Stable behavior under variable framerates and network conditions
- Drift and turbo systems, compatible with a racetrack system

---

## Technical Details

- Custom force-based movement system (non-rigidbody driven in key areas)
- Per-frame force accumulation and constraint resolution
- Simplified contact modeling for performance and control
- Deterministic-friendly structure for multiplayer stability

---

## Results / Impact

- Shipped across multiple NBA 2K titles (2K24–2K27)
- Enabled expansion of vehicle-based gameplay systems (including the introduction of a racetrack venue starting in 2K25)
- Reduced iteration time for designers through tunable parameters
- Provided a scalable foundation for future vehicle systems

---

## Visuals and Links

![2K25 "The Track" Demo](https://www.youtube.com/watch?v=vmT1Lodl2bY)
![2K24 Skateboard Debut](https://youtu.be/q1M5nhhkLQE?si=z5NHkudwCEICCC2H&t=119)
![2K25 "The Track" Announcement](https://nba.2k.com/en-GB/2k25/courtside-report/the-city/)
![2k26 "The Track" Details](https://nba.2k.com/2k26/courtside-report/the-city/)
