# Belty V1.0
![Belty V1.0](./images/beltyv1.png)
A custom 3D conveyor belt printer with CoreXY gantry and Spider mainboard using Marlin firmware. 

## Goals
Basic Goal: To learn more about 3D printing and how to design a 3D printer. 
Ultimate Goal: Improve reliability and print quality of belt 3D printers, as well as exploring belt options. 

## To-do
- Crimp wires connected to power supply (waiting on crimper)
- Learn Klipper and prepare firmware
- Setup Octoprint with PiCam
- Explore linear/pressure advance and input shaping with belt printer

## Current Issues
- Y homing and bed leveling with inductive probe
- Electronics enclosure redesign needed
- Belt shifting along rollers

## Fixed Issues
- Redesigned Carriage belt tension bracket to tighten belts
- Re-flashed firmware and extruder is functioning properly
- Unclogged Micros Swiss heat break using heat gun and an allen key (heat it up and push out clogged filament) 
- Tested X and Y movement, no lost steps or jitter
- Switched X endstop to confirm to slicer standard