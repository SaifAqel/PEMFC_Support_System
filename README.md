# PEMFC Support System: Hydrogen & Thermal Control Design

A complete design project focused on the hydrogen delivery and thermal management subsystems for a Proton Exchange Membrane Fuel Cell (PEMFC), with emphasis on hydrogen preheating and water-based cooling cycle integration.

## Overview

This individual engineering project aims to enhance the performance and efficiency of PEMFCs by designing robust and controllable hydrogen and cooling support systems. The study explores the selection of a real commercial PEMFC unit, determines optimal operating conditions, and implements a detailed design using thermal feedback and PID-based control strategies.

## Project Objectives

- Select an industrial-grade PEMFC (EH81 by EH Group Engineering AG)
- Determine optimal operating temperature based on electrochemical and humidification parameters
- Design and implement a complete hydrogen preheating cycle using both active (electric heater) and passive (heat exchanger) elements
- Design a water-based cooling cycle to stabilize cell temperature and reuse waste heat
- Develop a dynamic control model using thermostats and PID controllers to regulate flow and temperature across both cycles

## System Components

### Hydrogen Supply System

- **Hydrogen Tank** – fuel source
- **Expansion Valve** – pressure/temperature regulation
- **Electric Heater** – active heating
- **Heat Exchanger** – passive heating from PEMFC waste heat
- **Three-Way Modulating Valves** – flow control
- **Humidifier** – moisture control to prevent membrane dehydration
- **Thermostats** – temperature measurement and control trigger

### Cooling System

- **Three-Way Modulating Valve** – water flow splitting and regulation
- **Heat Exchanger** – shared with hydrogen cycle
- **Radiator** – final cooling stage
- **Check Valve** – prevents backflow
- **Thermostats** – monitor and stabilize cooling loop

## Control Strategy

- PID-based feedback loops regulate gas and water temperature
- Thermostats serve as sensors for real-time monitoring
- Modulating valves balance flows from hot/cold branches
- Control equation (PID controller):

```
u(t) = Kp · e(t) + Ki · ∫ e(t) dt + Kd · d(e(t))/dt
```

Where:
- `Kp`: Proportional gain  
- `Ki`: Integral gain  
- `Kd`: Derivative gain  
- `e(t)`: Error between measured and desired temperature  
- `u(t)`: Control signal to the valve  

This formula governs how the valve position responds dynamically to thermal deviations in both hydrogen and cooling loops.

## Results & Impact

- Optimized hydrogen temperature: **62.8°C**
- Integrated control logic ensures thermal stability and fuel efficiency
- System contributes to improved PEMFC performance, cold-start behavior, and membrane longevity
- Promotes scalable, clean hydrogen-based energy generation

## Author

**Saif-Aldain Ahmad Deeb Aqel**  
Student ID (Neptun): QTY3S6  
Consultant: Levai Emese  
Budapest University of Technology and Economics  
Faculty of Mechanical Engineering – Department of Energy Engineering

## License

This repository is provided for academic and educational purposes.  
All designs and calculations belong to the author unless otherwise cited.
