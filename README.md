# Correlated Double Sampling (CDS) Technique for Resistive Data Acquisition

## Project Overview
This repository contains the design, implementation, and simulation of a **Correlated Double Sampling (CDS)** block tailored for the analog and digital VLSI domain. 
The primary objective of this architecture is to completely cancel the amplifier's DC offset while simultaneously achieving a high overall voltage gain of approximately $A^2$ (where $A$ is the intrinsic gain of the core amplifier).
The core of this design relies on a discrete-time switched-capacitor architecture operating under a two-phase non-overlapping clock scheme ($\phi_1$ and $\phi_2$):

* **Precise Charge Transfer (V Mode):** During $\phi_1$, the input voltage ($V_{IN}$) is sampled onto the input capacitor $C_1$. During $\phi_2$, this charge is transferred to the feedback capacitor $C_2$.
* **Transfer Function:** The fundamental output voltage relationship is defined by the capacitor ratio, governed by the equation: 
  $$V_{O1} = \frac{\Delta Q_{C1}}{C_2} = \frac{C_1 \cdot V_{IN}}{C_2}$$
* **Offset Cancellation:** Inherent DC offset and low-frequency $1/f$ noise are sampled and subtracted across the two clock phases, resulting in a clean output signal.
* **Squared Gain (A²):** The system architecture leverages the core op-amp to square the intrinsic gain, ensuring the weak sensor inputs are adequately amplified after offset removal.

## Tools & Technologies
* **Design & Simulation:** Cadence Virtuoso, Tanner EDA

