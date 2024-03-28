## Digital-SoC-Design
# Digital ASIC Design

![image](https://github.com/ABHIMR1502/Digital-SoC-Design/assets/79500348/bf20d9f7-0c33-447f-93c4-48d780fd91a4)

# Open Source Digital ASIC Design
![image](https://github.com/ABHIMR1502/Digital-SoC-Design/assets/79500348/334cdb8a-7d5d-4695-b962-22ffa7c1aa71)

# RTL2GDS Flow
![image](https://github.com/ABHIMR1502/Digital-SoC-Design/assets/79500348/4e966e81-3d32-41c2-8eb4-90b090d7682b)
1. Synthesis: HDL code is converted into an optimized gate-level netlist based on the standard cell library provided.
2. FLoor and power planning:
   * Chip floor planning: This includes partitioning of the chip die into different building blocks and also placing of the I/O pads.
   * Macro floor planning: This includes defining of the dimensions, pin locations, row etc.
   * Power Planning: ->Power planning defines the power required by the all the macros, standard cells and other cells 
                     ->Power Distribution Levels: Power Rings, Power Straps, and Power Rails are the three levels that 
                       distribute power across the chip. They each carry VDD and VSS.
3. Placement: Using a post-synthesis netlist and floor-planning/physical design limitations, arranging the standard cells on the chip to create a 
              physical layout.
4. Clock Tree Synthesis: Involves providing clock signals to all the sequential elements in the design to obtain minimum skew usually in the form of a 
                         tree(H, X, pi tree, Fish Bone).
5. Routing:  Includes making wires to connect the various cells to create a physical layout.
6. SignOff: This includes timing (STA) and physical(DRC, LVS) verifications

# OpenLANE and strive chipset
![image](https://github.com/ABHIMR1502/Digital-SoC-Design/assets/79500348/d2e51da5-aac9-40ed-85a0-ba3663614956)
![image](https://github.com/ABHIMR1502/Digital-SoC-Design/assets/79500348/99207e59-6973-4cbd-b8b3-be26df3393f5)

#  OpenLANE ASIC Flow
![image](https://github.com/ABHIMR1502/Digital-SoC-Design/assets/79500348/19f4b185-4152-44ab-b992-02a731bbe687)
