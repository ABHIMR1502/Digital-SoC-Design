## Digital-SoC-Design
## DAY 1
 # Digital ASIC Design

![image](https://github.com/ABHIMR1502/Digital-SoC-Design/assets/79500348/bf20d9f7-0c33-447f-93c4-48d780fd91a4)

# Open Source Digital ASIC Design
![image](https://github.com/ABHIMR1502/Digital-SoC-Design/assets/79500348/334cdb8a-7d5d-4695-b962-22ffa7c1aa71)

#  RTL2GDS Flow
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

 # OpenLANE ASIC Flow
![image](https://github.com/ABHIMR1502/Digital-SoC-Design/assets/79500348/19f4b185-4152-44ab-b992-02a731bbe687)


# Exploring OpenLANE Directory 

->Working on sky130A(pdk) which contains libs.tech which has respective files on tools such as magic, netgen etc., and libs.ref which has files related to the specific 
  technology
  
![Screenshot from 2024-03-28 15-50-10](https://github.com/ABHIMR1502/Digital-SoC-Design/assets/79500348/27b7f093-f17b-4fc9-953c-6a5e3be6de1c)

![Screenshot from 2024-03-28 15-57-59](https://github.com/ABHIMR1502/Digital-SoC-Design/assets/79500348/5ea82939-c422-423f-827d-21d5b841a191)

# Running docker command

->commands used
   * ./flow.tcl -interactive
   * package required openlane 0.9
![Screenshot from 2024-03-28 16-11-46](https://github.com/ABHIMR1502/Digital-SoC-Design/assets/79500348/e8dc3af2-2f64-4fc6-ba19-3afef91ea990)

# Design setup stage and synthesis for picorv32a

->commands used

   * prep -design picorv32a
   * run_synthesis

![Screenshot from 2024-03-28 16-21-37](https://github.com/ABHIMR1502/Digital-SoC-Design/assets/79500348/e25bbf9f-5830-4d98-a669-fb2883a28669)

![Screenshot from 2024-03-28 19-04-05](https://github.com/ABHIMR1502/Digital-SoC-Design/assets/79500348/90e02a19-ad17-4063-943d-3081743cf160)
# Report generated after synthesis

![Screenshot from 2024-03-28 19-23-30](https://github.com/ABHIMR1502/Digital-SoC-Design/assets/79500348/3404756b-c8f9-4204-97ce-77a6c5dc0861)

->To calculate Flop Ratio

     Flop Ratio = No. of D FlipfLops/Total No. of cells

                 =1613/14876

                 =0.10842

      Percentage of D FF's = 10.842%

![Screenshot from 2024-03-28 19-24-09](https://github.com/ABHIMR1502/Digital-SoC-Design/assets/79500348/86430ad5-092f-499d-b5f8-53d6aad2c045)

->Chip area for the module = 147712.9184

-> Synthesis and Stat reports are below

   [Click here to view 1-yosys_4.stat.rpt](https://github.com/ABHIMR1502/Digital-SoC-Design/blob/main/DAY1/1-yosys_4.stat.rpt)
   
   [Click here to view picorv32a.synthesis.v](https://github.com/ABHIMR1502/Digital-SoC-Design/blob/main/DAY1/picorv32a.synthesis.v)
