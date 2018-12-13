---
layout: page
title: Phase Change Memory Simulations
subtitle: Determining Effects of Selector Diode Quantity on Array Size</br></br>2018
---
GST is the phase change material commonly used in phase change memory (PCM). It has a high-resistance amorphous phase and a low-resistance crystalline phase.
<img src="/img/PCM1.png" alt="GST Phases" width="700">.

In addition to being low power and low cost, phase change memory can be used in a cross point architecture, allowing for increased density and scalability.
<img src="/img/PCM2.png" alt="Cross Point Architecture" width="700">

During the non-ideal operation of a 1R cross-point PCM array, current may flow through non-target cells if there is a path of lower resistance. 
<img src="/img/sneakPaths.png" alt="1R Sneak Paths" width="700">

Selectors, which can be either transistors or diodes, can mitigate these sneak paths by limiting where current can flow. 1D1R PCM, which uses diodes as selectors, offers further increased density compared to its 1T1R counterpart, which is already commercially available. However, diodes leak some current in reverse bias and this leakage may limit bitline swing.
<img src="/img/1T1R.png" alt="1T1R" width="300">
<img src="/img/1D1R-leakage.png" alt="1D1R" width="400">

The ultimate goal of the simulation framework is thus to **quantify the effects of diode leakage on maximum array size** and determine the quality of diodes necessary for ideal performance.

Verilog-A models the hardware of the PCM device and selector diode, and HSPICE describes the netlist of the full array model for simulation. The resulting full array model includes drivers, PCM devices, selector diodes, and wire parasitics.
<img src="/img/full-array-with-drivers.png" alt="Full Array Model" width="700">

Credit: *Carla Becker, Hamzah Khan, Josephine King, Matthew Spencer*
