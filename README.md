# VSDIAT Training using OPENLANE
<p align="center">
<img src="./media/image1.png" style="width:7.2089in;height:3.65876in" />
</p>

# **Table of Contents**
- [Day – 1 Inception of Open-Source EDA, OpenLANE and Sky130 PDK](#day--1-inception-of-open-source-eda-openlane-and-sky130-pdk)
  - [Theory – Fundamentals of SoC](#theory--fundamentals-of-soc)
  - [Theory - Understanding RISC-V Architecture](#theory--understanding-risc-v-architecture)
  - [Theory - Understanding ASIC Design Flow](#theory--understanding-asic-design-flow) 
    - [Process Design Kits](#process-design-kits)
    - [Skywater 130nm Open PDK Example](#skywater-130nm-open-pdk-example)
   - [Overview of RTL2GDS ASIC Design Flow](#theory---overview-of-rtl2gds-asic-design-flow) 
   - [Theory – Introduction to OpenLane and Strive Chipset](#theory--introduction-to-openlane-and-strive-chipset)
   - [Theory - OpenLane ASIC Flow](https://github.com/nsehgal1301/VSDIAT_Training/blob/main/README.md#theory--openlane-asic-flow)
     - [OpenROAD App](https://github.com/nsehgal1301/VSDIAT_Training/blob/main/README.md#openroad-app--)
     - [Logic Equivalence Checking](https://github.com/nsehgal1301/VSDIAT_Training/blob/main/README.md#logic-equivalence-checking-)
     - [Antenna Rule Violation](https://github.com/nsehgal1301/VSDIAT_Training/blob/main/README.md#antenna-rule-violation-)
   - [Lab - Understanding OpenLane ASIC Flow](https://github.com/nsehgal1301/VSDIAT_Training/blob/main/README.md#lab--understanding-openlane-asic-flow)
 - [Day - 2 Good Floorplan vs Bad Floorplan and Introduction to Library Cells](https://github.com/nsehgal1301/VSDIAT_Training/blob/main/README.md#day--2-good-floorplan-vs-bad-floorplan-and-introduction-to-library-cells)
   - [Theory - Utilization Factor and Aspect Ratio](https://github.com/nsehgal1301/VSDIAT_Training/blob/main/README.md#theory--utilization-factor-and-aspect-ratio)
   - [Theory - Concept of Pre Placed Cells](https://github.com/nsehgal1301/VSDIAT_Training/blob/main/README.md#theory--concept-of-pre-placed-cells)
   - [Theory - Concept of Power Planning](https://github.com/nsehgal1301/VSDIAT_Training/blob/main/README.md#theory--concept-of-power-planning)
   - [Lab - Running Floorplan using RePlace](https://github.com/nsehgal1301/VSDIAT_Training/blob/main/README.md#lab--running-floorplan-using-openlane)
   - [Lab - Congestion Aware Placement using RePlace](https://github.com/nsehgal1301/VSDIAT_Training/blob/main/README.md#lab--congestion-aware-placement-using-replace)
   - [Theory - Circuit Design Step and 2.3.3 Layout Design Step](https://github.com/nsehgal1301/VSDIAT_Training/blob/main/README.md#theory--circuit-design-step-and-233-layout-design-step)
   - [Theory - Timing Characterization Parameters](https://github.com/nsehgal1301/VSDIAT_Training/blob/main/README.md#theory--timing-characterization-parameters)
 - [Day -3 Design Library Cell using Magic Layout and ngSpice Characterization](https://github.com/nsehgal1301/VSDIAT_Training/blob/main/README.md#day--3-design-library-cell-using-magic-layout-and-ngspice-characterization)
   - [Lab - IOPlacer Experiment for Equi-Distant Bumps](https://github.com/nsehgal1301/VSDIAT_Training/blob/main/README.md#lab--ioplacer-experiment-for-equi-distant-bumps)
   - [Lab - Steps to Gitclone vsdstdcelldesign](https://github.com/nsehgal1301/VSDIAT_Training/blob/main/README.md#lab--steps-to-gitclone-vsdstdcelldesign)
   - [Theory - CMOS Fabrication Process](https://github.com/nsehgal1301/VSDIAT_Training/blob/main/README.md#theory--cmos-fabrication-process)
   - [Lab - Introduction to Sky130 Basic Layers Layout and LEF using Inverter](https://github.com/nsehgal1301/VSDIAT_Training/blob/main/README.md#lab--introduction-to-sky130-basic-layers-layout-and-lef-using-inverter)
   - [Lab - Calculating the Characteristics of an Inverter using ngSpice](https://github.com/nsehgal1301/VSDIAT_Training/blob/main/README.md#lab--calculating-the-characteristics-of-an-inverter-using-ngspice)
     - [Falling Condition Delay Calculation](https://github.com/nsehgal1301/VSDIAT_Training/blob/main/README.md#falling-condition-delay-calculation-)
     - [Rising Condition Delay Calculation](https://github.com/nsehgal1301/VSDIAT_Training/blob/main/README.md#rising-condition-delay-calculation-)
   - [Lab - Introduction to DRCs and Downloading DRC Testcase](https://github.com/nsehgal1301/VSDIAT_Training/blob/main/README.md#lab--introduction-to-drcs-and-downloading-drc-testcase)
   - [Lab - Loading Sky130 Tech Rules in Magic](https://github.com/nsehgal1301/VSDIAT_Training/blob/main/README.md#lab--loading-sky130-tech-rules-in-magic)
   - [Lab - Generating the Poly9 Error](https://github.com/nsehgal1301/VSDIAT_Training/blob/main/README.md#lab--generating-the-poly9-error)
   - [Lab - Challenge Exercise to Describe DRC Error as Geometrical Construct](https://github.com/nsehgal1301/VSDIAT_Training/blob/main/README.md#lab---lab-challenge-exercise-to-describe-drc-error-as-geometrical-construct)
   - [Lab - Challegne to Find Missing or Incorrect rules and Fix them](https://github.com/nsehgal1301/VSDIAT_Training/blob/main/README.md#lab---lab-challenge-to-find-missing-or-incorrect-rules-and-fix-them)
 - [Day - 4 Pre Layout Timing Analysis and Importance of a Good Clock Tree](https://github.com/nsehgal1301/VSDIAT_Training/blob/main/README.md#day--4-pre-layout-timing-analysis-and-importance-of-a-good-clock-tree)
   - [Theory - Introduction to Delay Tables](https://github.com/nsehgal1301/VSDIAT_Training/blob/main/README.md#theory--introduction-to-delay-tables)
   - [Lab - Extracting LEF file from Layout File](https://github.com/nsehgal1301/VSDIAT_Training/blob/main/README.md#lab--extracting-lef-file-from-layout-file)
   - [Lab - Data Preparation for Including Custom LEF Inverter in OpenLane Flow](https://github.com/nsehgal1301/VSDIAT_Training/blob/main/README.md#lab--data-preparation-for-including-custom-lef-inverter-in-openlane-flow)
   - [Lab - Running OpenLane with including new Custom INV cell](https://github.com/nsehgal1301/VSDIAT_Training/blob/main/README.md#lab--running-openlane-with-including-new-custom-inv-cell)
   - [Lab - Resolving Huge Timing Violations Observed](https://github.com/nsehgal1301/VSDIAT_Training/blob/main/README.md#lab--resolving-huge-timing-violations-observed)
   - [Theory - Understanding Static Timing Analysis](https://github.com/nsehgal1301/VSDIAT_Training/blob/main/README.md#theory--understanding-static-timing-analysis)
   - [Lab - Setting up STA Analsyis for Picorv32a design using openSTA](https://github.com/nsehgal1301/VSDIAT_Training/blob/main/README.md#lab--setting-up-sta-analysis-for-picorv32a-design-opensta)
   - [Lab - Setting up STA Analsyis for Picorv32a design using openSTA](https://github.com/nsehgal1301/VSDIAT_Training/blob/main/README.md#lab--setting-up-sta-analysis-for-picorv32a-design-opensta-1)
   - [Theory - Clock Tree Synthesis](https://github.com/nsehgal1301/VSDIAT_Training/blob/main/README.md#theory--clock-tree-synthesis )
   - [Theory - Clock Tree Synthesis](https://github.com/nsehgal1301/VSDIAT_Training/blob/main/README.md#theory--clock-tree-synthesis)
   - [Theory - Clock Net Shielding and CrossTalks](https://github.com/nsehgal1301/VSDIAT_Training/blob/main/README.md#theory--clock-net-shielding-and-crosstalks)
   - [Lab - Running CTS on Passed STA design using TritonCTS](https://github.com/nsehgal1301/VSDIAT_Training/blob/main/README.md#lab--running-cts-on-passed-sta-design-using-tritoncts)
   - [Lab - Running STA again on Post CTS Netlist](https://github.com/nsehgal1301/VSDIAT_Training/blob/main/README.md#lab--running-sta-again-on-post-cts-netlist)
 - [Day -5 Final Steps for RTL2GDS using TritonRoute and openSTA](https://github.com/nsehgal1301/VSDIAT_Training/blob/main/README.md#day--5-final-steps-for-rtl2gds-using-tritonroute-and-opensta)
   - [Theory - Understanding Routing Algorithms](https://github.com/nsehgal1301/VSDIAT_Training/blob/main/README.md#theory--understanding-routing-algorithms)
   - [Theory - DRC Checks for Routing](https://github.com/nsehgal1301/VSDIAT_Training/blob/main/README.md#theory--drc-checks-for-routing)
   - [Lab - Creating Power Distriution Network on Post CTS Design](https://github.com/nsehgal1301/VSDIAT_Training/blob/main/README.md#lab--creating-power-distribution-network-on-post-cts-design)
     - [Created PDN Details and Statistics](https://github.com/nsehgal1301/VSDIAT_Training/blob/main/README.md#created-pdn-details-and-statistics)
   - [Theory - Understanding TritonRoute](https://github.com/nsehgal1301/VSDIAT_Training/blob/main/README.md#theory--understanding-tritonroute)
   - [Theory - Routing Algorithm of TritonRoute](https://github.com/nsehgal1301/VSDIAT_Training/blob/main/README.md#theory--routing-algorithm-of-tritonroute)
   - [Lab - Routing the Design using TritonRoute](https://github.com/nsehgal1301/VSDIAT_Training/blob/main/README.md#lab--routing-the-design-using-tritonroute)
     - [Logs and Reports from TritonRoute](https://github.com/nsehgal1301/VSDIAT_Training/blob/main/README.md#logs-and-reports-from-triton-route)


# **Day – 1 Inception of Open-Source EDA, OpenLANE and Sky130 PDK**

## **Theory – Fundamentals of SoC**

A simple package board can be represented using a simple block diagram
in which the main brain of the board is it’s Processor/SoC and the SoC
needs to communicate to different blocks like RAM, DRAM, IO’s,
ADC/DAC’s, UART/PCIe etc and for that it must have some output pins
getting connected to each component through a package.
<p align="center">
<img src="./media/image2.png" style="width:6.26806in;height:3.58264in"
alt="Graphical user interface Description automatically generated with medium confidence" />
</p>
<p align="center">
Fig – 1. Simple Block Diagram of a SoC
</p>
A simple chip can either be of FlipChip (BGA) or can be of Wirebond
Type. An example of Wirebond is shown in Fig 2(a). These bond wires
connect to the smaller pins of the actual die inside and directly
connect to the IO Pads present at the boundary of the Chip. After
zooming in further Fig 2 can be effectively presented as Fig 2(b) where
the centre region is called Core which contains all the logic and
functionality and the other counterpart is periphery region which
contains all the I/O pads, level shifters, ESD cells etc for
communicating to the outer world.
<p align="center">
<img src="./media/image3.png" style="width:7.0875in;height:2.81597in" />
</p>
<p align="center"> Fig 2 (a) Actual Structure of SoC with Wirebond (b) Zoomed version of
SoC for depicting connections of SoC to the Die inside marking different
zones of die </p>

Core contains most of the logic of the SoC and it consists of leaf level
instances (RTL Logic), Foundry IP’s and Custom Macro’s. Fig 3 represents
a simple RISC-V architecture based SoC. The chip is partitioned to
different tiles and each area has its own feature/process. Certain goals
and criteria’s like Area, Timing, Power etc are decided and the SoC is
worked thorough different processes in order to match and fine-tune the
top level requirements.
<p align="center">
<img src="./media/image4.png" style="width:3.60979in;height:3.0553in" />
</p>
<p align="center"> Fig 3. Depiction of different components of a RISC-V Architecture Core </p>

## **Theory – Understanding RISC-V Architecture**

RISC-V is an open instruction set architecture and is way through which
we can communicate with the computer. A computer code is initially
converted to its corresponding Assembly Language Program which is
nothing but Hexadecimal code conversion and that is done via RISC-V
Assembly language program which is further converted to 0’s and 1’s
binary language. And these 0’s and 1’s are nothing but digital signal
which can be implemented on the Layout/hardware. An intermediate step
between this conversion is a HDL code/ RTL code which implements the
RISC-V architecture and from which the actual layout can be mapped. Fig
5 explains the whole cycle of communication from Front-End to Binary
Conversion to actual Hardware implementation.
<p align="center">
<img src="./media/image5.png" style="width:7.0875in;height:4.12292in" />
</p>
<p align="center"> Fig 4 – Understanding RISC-V Architecture </p>

Flowchart below (Fig 5) explains the conversion of our day-to-day
applications from Human Understandable Format to Machine Understandable
Format.
<p align="center">
<img src="./media/image6.png" style="width:7.0875in;height:4.71042in" />
</p>
<p align="center"> Fig 5 – Flowchart defining all the steps performed for executing an
Instruction </p>

## **Theory – Understanding ASIC Design Flow**

ASIC design stands for Application Specific Integrated Circuits and it
is the methodology of reducing the cost and size of the an electronic
system or SoC. It consists of various components like –

1.  RTL’s or HDL Code – Contains information to represent functionality.

2.  PDK’s – Process Design Kit contains information for manufacturing
    the correct technology.

3.  EDA Tools – Required for simulation and connecting the simulation
    world to actual hardware.

### **Process Design Kits**

Process Design Kits is basically a collection of different type of
process data that will be required to manufacture the Hardware based on
the Implemented RTL code. This data is used by different EDA tools to
design an IC. It contains different type of information like –

1.  DRC , LVS , PEX rules

2.  Device Models

3.  Liberties for Cell Characterization

4.  Technology Files depicting the Manufacturing Technology Details

5.  I/O libraries

6.  Design Rule Manual etc.

### **Skywater 130nm Open PDK Example**

Skywater 130nm is an open-access PDK created by Google and skywater,
enabling complete ASIC design process to be open-source. Lower
Technology nodes are encrypted and are not openly available in market
yet but it doesn’t mean 130nm technology is redundant and is not in use.
Actual reality says that 130nm is still used by different companies to
perform automated tasks as manufacturing of 130nm is relatively much
cheaper and it can readily used in places which doesn’t operate at High
Speeds.

## **Theory - Overview of RTL2GDS ASIC Design Flow**

There are various components of a simple RTL2GDS ASIC design flow and it
converts the RTLs into corresponding GDSII format which is a must for
tapeout by foundries. Fig 6 represents the whole much compressed form of
RTL2GDS flow for simpler understanding. Every stage has its own
importance and functionality which is explained below.
<p align="center">
<img src="./media/image7.png" style="width:7.0875in;height:4.55625in" />
</p>

<p align="center"> Fig 6. RTL2GDS Flow </p>

1.  Synthesis – RTL is converted to the corresponding circuitry using
    the Standard Cell Libraries and the used language for describing the
    functionality is called HDL. Each standard cell used for synthesis
    has a regular layout which means that the height of each cell is
    discrete can be multiple of the fixed distance between VSS and VDD
    line whereas the width of each cell can be varied.
<p align="center">
<img src="./media/image8.png"
style="width:6.29375in;height:2.46422in" />
</p>
<p align="center"> Fig 7. Synthesis </p>

2.  Floorplanning / Powerplanning – Now all the standard cells need to
    be placed in within the chip bounds and in an unordered fashion for
    calculating the required area for producing the chip. Floorplanning
    and Powerplanning is done a very high block level based on tiling
    and detailed placement for logic in each tile is done in placement
    stage.
<p align="center">
<img src="./media/image9.png" style="width:6.36196in;height:2.37249in"
alt="Diagram Description automatically generated" />
</p> <p align="center">
<img src="./media/image10.png" style="width:6.36432in;height:2.32224in"
alt="Diagram, bar chart Description automatically generated" />
</p>
<p align="center"> Fig 8 (a) Floorplanning Process (b) Powerplanning process </p>

3.  Placement – Now the standard cells contained within the blocks will
    be placed on the standard PDN network so that they follow the VDD –
    VSS – VDD pitch and can be connected to the supply domains. It is
    generally done in two steps Global and Detailed Routing.
<p align="center">
<img src="./media/image11.png" style="width:6.41691in;height:2.1855in"
alt="Chart, bar chart, waterfall chart Description automatically generated" />
</p> <p align="center">
<img src="./media/image12.png"
style="width:6.40031in;height:2.35732in" />
</p>
<p align="center"> Fig 9 (a) Placement Example (b) Steps involved during  </p>

4.  Clock Tree Synthesis (CTS) – Now the clock tree synthesis needs to
    be done in such a manner that clock reaches to different sections
    with minimum skew and connects to all sequential elements. This can
    be achieved by adding different buffers and is usually of H or X
    format so the clock reaches all parts with min skew.
<p align="center">
<img src="./media/image13.png" style="width:6.50438in;height:2.28985in"
alt="Graphical user interface, text, application Description automatically generated" />
</p>
<p align="center"> Fig 10. Clock Tree Synthesis </p>

5.  Routing – After routing the clock, it’s time for the signal routing.
    Now each logic/sequential/macro data input and output pins needs to
    be connected to the right places with minimum amount of twists and
    turns. And also with minimum amount of metal used, it happens in two
    stages – Global Routing and Detailed Routing.
<p align="center">
<img src="./media/image14.png"
style="width:6.43283in;height:2.53002in" />
</p>
<p align="center"> Fig 11. Routing Procedure </p>

6.  Sign Off – After finalizing the design, now comes the step of
    verification of the die to test whether it performs the expected
    functionality with the required power/area constraints or not. A
    number of tests like Functionality verification, DFT, IR signoff,
    STA are performed in order to pre-simulate the chip and confirm its
    functioning before tapeout.
<p align="center">
<img src="./media/image15.png" style="width:6.49609in;height:2.27866in"
alt="Text Description automatically generated with medium confidence" />
</p>
<p align="center"> Fig 12. Sign Off Processes </p>

## **Theory – Introduction to OpenLane and Strive Chipset**

Users generally face quite a few challenges when using open source EDA,
problems like missing EDA tools for some steps, calibration or tool
qualifications are some challenges faced.

Openlane the open source EDA consists of different steps and is
streamlined flow and is a complete end-to-end solution for rtl2gds flow.
At Efabless, there is family of open access chip known as striVe. It is
complete chipset with everything as open access, open PDK, open RTL’s
and open EDA.
<p align="center">
<img src="./media/image16.png"
style="width:7.0875in;height:3.21528in" />
</p> <p align="center">
<img src="./media/image17.png" style="width:7.0875in;height:4.41042in"
alt="A picture containing graphical user interface Description automatically generated" />
</p>
<p align="center"> Fig 13 (a) Depiction of a General Die (b) striVe open access family of chips </p>

Main goal of OpenLane tool is to produce a GDS2 file automatically
without any human intervention and the die created must be clean, by
clean we mean that –

1.  The chipset should not have any LVS violations.

2.  The chipset should not have any DRC violations.

3.  The chipset should not have any Timing violations.

## **Theory – OpenLane ASIC Flow**

Openlane as discussed is an open-access end to end EDA solution and can
be used to harden chips or Macros. OpenLane has two modes of operation –

1.  Autonomous – It’s a push-button flow and automatically generated
    GDS2.

2.  Interactive – It’s a more controlled step by step implemented flow.

Openlane has a feature called Design Set Exploration by which it can
find the best set of parameters and constraints that can be used in the
flow. It basically sweeps through different configurations and suggest
the best solution to be used as constraints for the flow.

<p align="center">
<img src="./media/image18.png"
style="width:7.0875in;height:3.79167in" />
</p>
<p align="center"> Fig 14. OpenLane Design Exploration Step </p>

Figure below mentions the Flowchart of OpenLane ASIC Flow. This OpenLane
Flow consists of many different types of open-source tools like yosys,
openSTA, TritonRoute, Magic, Qflow, Fault etc. The flowchart below
effectively summarizes how each tool is being used and what is the
general flow deployed while using OpenLane.

<p align="center">
<img src="./media/image19.png" style="width:7.0875in;height:4.26319in"
alt="Diagram Description automatically generated" />
</p>
<p align="center"> 
<img src="./media/image20.png" style="width:7.0875in;height:5.0375in" />
</p>

### **OpenROAD App -**

OpenRoad app is automatic placement and routing tool and it performs the
following function –

1.  Floorplanning

2.  Powerplanning

3.  Placement: Global and Detailed

4.  Post Placement Optimization

5.  Clock Tree Synthesis

6.  Routing: Global and Detailed

### **Logic Equivalence Checking –**

After performing quite a few iterations LEC needs to be performed in
order to check whether updating the design has caused any effect on the
Functionality of the chip or not.

### **Antenna Rule Violation –**

When a metal wire segment is fabricated and it is long enough, it can
act as antenna. If charge gets accumulated on it, it can damage our
transistor during fabrication. So, length of wire must be limited, this
is the job of router.
<p align="center">
<img src="./media/image21.png"
style="width:3.61576in;height:2.37791in" />
</p>
In order to resolve this we can perform two solutions –

1.  Bridging – This is performed using top metal layer and the
    parallelization is terminated by going up till the top metal layer
    and then coming back to the original layer as shown in figure below.
<p align="center">
<img src="./media/image22.png" style="width:5.17973in;height:2.17167in"
alt="A picture containing application Description automatically generated" />
</p>
2.  Inserting and Antenna Diode – This diode protects from the surges
    automatically.
<p align="center">
<img src="./media/image23.png" style="width:3.80044in;height:2.21763in"
alt="Chart Description automatically generated" />
</p>
In openlane we take a preventive approach, and we insert Fake antenna
diode next to every cell after placement. And then we run the Antenna
Checker if it reports a violation, we replace the fake cell by original
cell else keep it as it is.

## **Lab – Understanding OpenLane ASIC Flow**

Openlane is thewrapper which contains all the tool and is a streamline
flow for running RTL2GDS full flow. Directory structure of OpenLane are
as follows-

PDKS –
<p align="center">
<img src="./media/image24.png" style="width:6.26806in;height:0.93056in"
alt="Text Description automatically generated with medium confidence" />
</p>
Sky130A PDK has –
<p align="center">
<img src="./media/image25.png" style="width:6.26806in;height:0.97986in"
alt="Text Description automatically generated" />
</p>
Under Libs.tech
<p align="center">
<img src="./media/image26.png" style="width:6.26806in;height:1.90694in"
alt="Table Description automatically generated" />
</p>
Under OpenLane directory we can find the following files shown below –
<p align="center">
<img src="./media/image27.png" style="width:7.02311in;height:2.52026in"
alt="Text Description automatically generated with medium confidence" />
</p>
Flow.tcl is the file that will be used to invoke openlane apart from
that we can see a folder called design which contains numerous different
designs shown below, We will be using picorv32a as a base for flow
flushing the whole openlane flow.
<p align="center">
<img src="./media/image28.png" style="width:7.12268in;height:1.08979in"
alt="Text Description automatically generated" />
</p>
To run openlane first run the docker command and then use the flow.tcl
for interactive mode as shown below-

`Docker

./flow.tcl -interactive`
<p align="center">
<img src="./media/image29.png" style="width:7.21578in;height:2.38314in"
alt="A screenshot of a computer Description automatically generated with medium confidence" />
</p>
Now we will load the required packages to run openlane using the command
–

`Package require openlane 0.9`
<p align="center">
<img src="./media/image30.png" style="width:3.78125in;height:0.53125in"
alt="Text Description automatically generated" />
</p>
Afterwards, we will load the picorv32a design for flow flushing
openlane, for loading the design use the command –

`prep -design picorv32a`
<p align="center">
<img src="./media/image31.png" style="width:7.13731in;height:4.83702in"
alt="Text Description automatically generated" />
</p>
A directory with respect to the time stamp is created automatically when
this command is run, the contents of the same directory is shown below –
<p align="center">
<img src="./media/image32.png"
style="width:7.18495in;height:1.83007in" />
</p>
Now its time to run synthesis using yosys in openlane. To perform
synthesis use command run_synthesis.This command is controlled by
various different settings corresponding to Yosys and we can alter these
to change the nature of synthesis according to our needs.
<p align="center">
<img src="./media/image33.png"
style="width:7.18284in;height:3.17681in" />
</p>
Various other config and tcl used for procedure defining and settings
definitions are shown below –
<p align="center">
<img src="./media/image34.png" style="width:7.29785in;height:3.63033in"
alt="Text Description automatically generated" />
</p><p align="center">
<img src="./media/image35.png" style="width:7.24459in;height:1.95281in"
alt="Text Description automatically generated" />
</p>

# **Day – 2 Good Floorplan vs Bad Floorplan and Introduction to Library Cells**

## **Theory – Utilization Factor and Aspect Ratio**

Initial requirement of creating any chip is to define its area and
aspect ratio along with the utilization factor.

Utilization factor – It is %age of the core which will be covered with
standard cell w.r.t to the original area defined. It needs to kept in a
nominal range not too low and not too high to avoid congestion.

If all the cells in core takes up all the available space, then that is
100% utilization and utilization factor become 1.

UF can be represented as = `(Area Utilized by Netlist) / (Area of the
total chip)`

<p align="center">
<img src="./media/image36.png" style="width:7.0875in;height:5.26458in"
alt="image" />
</p>

Suppose there is a netlist as shown below, that is, 2 flops and 2 logic
gates only.

<p align="center">
<img src="./media/image37.png" style="width:7.0875in;height:2.26806in"
alt="image" />
</p>

Now each of the cell can be represented in square dimension for ease of
calculating the width and height of each cell. Give rough dimensions to
each of the cell and calculate the dimension of netlist.

Each cell irrespective of the type of cell can be represented as
rectangular block which is made up of some area and that area is overall
calculated and added and finally utilization factor is applied to it for
calculating the approximate area of a chip.

<p align="center">
<img src="./media/image38.png" style="width:3.46528in;height:2.74167in"
alt="image" />
</p>

Now imagine a silicon wafer with many dies. Die has core inside it which
contains all the logic. Die is a silicon material on which fabrication
happens.

<p align="center">
<img src="./media/image39.png" style="width:3.56897in;height:2.7179in"
alt="image" />
</p> <p align="center">
<img src="./media/image40.png" style="width:3.05139in;height:2.81042in"
alt="image" />
</p>

## **Theory – Concept of Pre-Placed Cells**

Pre-placed cells: If there is large combinational circuit within our
complete chip, like circuit of 50k - 100k gates, we can implement that
separately as a different module and then re-use it in our chip multiple
times if needed. Or we can break that circuit further into sub circuits
and create small blocks of it and use them separately. Using the
periphery pins of these modules we can make the connections.

<p align="center">
<img src="./media/image41.png" style="width:7.0875in;height:1.59236in"
alt="image" />
</p>
<p align="center">
<img src="./media/image42.png" style="width:7.0875in;height:2.10694in"
alt="image" />
</p>

- Similarly, there are certain IP's available, like, memory,
  clock-gating cell, comparator, mux etc.

- The arrangement of these IPs in a chip is referred to as
  floorplanning.

- These IP's/blocks have user-defined locations, and hence are placed in
  chip before automated PnR and are called as pre-placed cells.

- Automated PnR tools places the remaining logic cells in the design
  onto chip.

- Locations of these pre-placed cells must be very well defined as
  cannot be changed later.

Now suppose if we have these 3 pre-placed cells, these are placed based
on the IO placement of the chip. All the pre-placed cells are surrounded
by decoupling capacitors, reasoning for that can be that whenever a cell
switches it will correspondingly charge and discharge the internal
capacitor respectively. But due to voltage drop across power grid this
charging and discharging doesn't happen completely to 1 and 0
respectively. We want the charging and discharging to be within the
noise margin to interpret the logic correctly as 1 and 0 respectively.

<p align="center">
<img src="./media/image43.png" style="width:7.0875in;height:4.51042in"
alt="image" />
</p> 
<p align="center">
<img src="./media/image44.png" style="width:7.0875in;height:4.28333in"
alt="image" />
</p>

Noise Margin: If we refer to the below image, we say that for any signal
to be treated as 1 or 0 it should be in the NMh and NMl ranges
respectively. These undefined ranges are known as noise margins.

<p align="center">
<img src="./media/image45.png" style="width:7.0875in;height:3.19167in"
alt="image" />
</p>

Now decoupling capacitors are bug capacitors sitting next to our cell,
these are charged to full VDD initially, when nearby circuit switches it
takes the required charge from this decoupling capacitor, similarly it
can load off it's charge to this decoupling capacitor in case of 1 -\> 0
switching. Therefore we surround the pre-placed cells with decoupling
capacitors.

<p align="center">
<img src="./media/image46.png" style="width:7.0875in;height:4.24514in"
alt="image" />
</p> 
<p align="center">
<img src="./media/image47.png" style="width:7.0875in;height:5.32986in"
alt="image" />
</p>

## **Theory – Concept of Power Planning**

All the standard cells are placed in certain rows in an orderly fashion
and parallel lines of VDD and VSS run alternatively through the base
metal layer. These are called as Power Rails; these power rails are
further then connected to the IO pad cell where the Power actually comes
in to the die.

Now concept of panning out these lings, rings etc and checking the bump
distribution to reduce load are considered under the concept of
PowerPlanning. Need for power needs to be identified within the chip and
correspondingly decap cells or rails networks are placed to keep the IR
drop minimum.

<p align="center">
<img src="./media/image48.png" style="width:7.0875in;height:4.40903in"
alt="image" />
</p>

We cannot utilize the whole chip area some area needs to be kept for IO
pad cells where the external signal and power will get connected. These
are also active devices and the rails run within the core.

<p align="center">
<img src="./media/image49.png" style="width:6.02934in;height:4.10345in"
alt="image" />
</p>

## **Lab – Running Floorplan Using OpenLane**

Reviewing the configuration filed, go to ***openlane -\>
configuration*** there will lots of file containing the configuration
parameters.

<p align="center">
<img src="./media/image50.png" style="width:7.19613in;height:1.98838in"
alt="A picture containing text Description automatically generated" />
</p>

Open ReadMe and understand different variables that can be altered for
design changes-

<p align="center">
<img src="./media/image51.png" style="width:7.366in;height:3.45205in" />
</p>

Setting used for defining different proc and parameters of floorplan are
kept in floorplan.tcl shown below -

<p align="center">
<img src="./media/image52.png"
style="width:6.98589in;height:5.38454in" />
</p>

Further another set of settings are defined in config.tcl and
sky130_hs_fd_hd_config.tcl. Please note that all three tickles have
different precedence order. Flow.tcl has the lowest precedence and it
increase in the following order –

`Flow.tcl \< config.tcl \< sky130_hs_fd_hd_config.tcl`

All the logs of the Floorplan are kept under the following directory –

<p align="center">
<img src="./media/image53.png"
style="width:7.15321in;height:0.49893in" />
</p>

Floorplan will generate a very rough DEF file with only tap cells or
decap cells as placement is not done and that is present under the
results folder which can be viewed in Magic correspondingly using the
command -

`magic -T \<tech file\> read lef \<lef file\> read def \<def file\>`

<p align="center">
<img src="./media/image54.png"
style="width:7.05389in;height:0.31885in" />
</p> 
<p align="center">
<img src="./media/image55.png"
style="width:6.98921in;height:3.98864in" />
</p>

On further zooming into the region of lines we see that these are
various tap cells and decap cells created during the floorplan however
no standard cells are present in area for def because placement is still
not complete and tool doesn’t know where to place the standard cells.

<p align="center">
<img src="./media/image56.png" style="width:4.79167in;height:4.625in"
alt="Table Description automatically generated with medium confidence" />
</p>

Further, we zoom in to the bottom left corner and found that all the
standard cells are kept at the corner since their placement information
is not known. It is shown in the figure below –

<p align="center">
<img src="./media/image57.png" style="width:6.26806in;height:5.03194in"
alt="Diagram Description automatically generated" />
</p>

## **Lab – Congestion Aware Placement using RePlace**

After running floorplan and viewing it in Magic, next steps are obvious
we need to run placement in order to place the standard cells in correct
rows and cells.

In order to perform placement use the following command in openlane –

`Run_placement`

Various Logs and Reports generated from run_placement are described
below –

<p align="center">
<img src="./media/image58.png"
style="width:7.16995in;height:0.92067in" />
</p>
<p align="center">
<img src="./media/image59.png"
style="width:7.20032in;height:0.88628in" />
</p>

After placement another DEF is generated which contains the previous
floorplan DEF and adds the standard cells positions to it accordingly.

<p align="center">
<img src="./media/image60.png" style="width:6.94943in;height:6.85319in"
alt="A picture containing text, electronics, circuit Description automatically generated" />
</p>

Various results that can be frawn out of the logs/ reports from
Placement are like it mentioned a first cut slack information although
its not correct but it can give a very coarse value for the same.

<p align="center">
<img src="./media/image61.png" style="width:7.04377in;height:3.66391in"
alt="A picture containing text Description automatically generated" />
</p>

## **Theory – Circuit design step and 2.3.3 Layout design step**

Design steps

- Circuit design

- Implement the function using transistor/gates.

- Model the transistors such a way to meet library requirements. (Mostly
  based on SPICE simulation)

- Output of circuit design --\> CDL (circuit descriptive language)

Layout design

- Once you know W/L values of pmos and nmos, next step is to implement
  these values in layout.

- Derive pmos and nmos network graph.

<p align="center">
<img src="./media/image62.png" style="width:6.25833in;height:5.96528in"
alt="image" />
</p>

Get the euler's path for the graph

<p align="center">
<img src="./media/image63.png" style="width:7.0875in;height:4.08264in"
alt="image" />
</p>

After getting the euler's path create stick diagram. Convert the stick
diagram to layout while we adhere to the rules given by foundary.

<p align="center">
<img src="./media/image64.png" style="width:7.0875in;height:3.36181in"
alt="image" />
</p>
<p align="center">
<img src="./media/image65.png" style="width:4.12083in;height:4.72431in"
alt="image" />
</p>

Output of this step are:

1.  GDSII --\> Layout file

2.  LEF --\> width and height of cell

3.  Extracted SPICE netlist (.cir) --\> Have parasitics (R and C) of
    each element

## **Theory – Timing Characterization Parameters**

Characterization helps to get timing, noise and power
information.Outputs of this steps are timing, noise and power.libs, and
functions. Steps for the same are explained below -

1.  Read the models.

2.  Read the extracted SPCIE netlist

3.  Define/recognize behavior of your cell

4.  Read sub-circuit used in making cell

5.  Attach necessary power sources

6.  Apply stimulus

7.  Necessary output capacitance

8.  Provide necessary simulation command (like .trans .dc .ac etc.)

We will define some variables which are used. These are based on input
and output waveform. Let's take inverter waveform.

<p align="center">
<img src="./media/image66.png" style="width:5.72431in;height:6.18958in"
alt="image" />
</p>

- slew_low_rise_thr --\> 20% from 0 for rising

- slew_high_rise_thr --\> 20% from 1 that is 80% from 0 for rising

- slew_low_fall_thr --\> 20% from 0 for falling

- Slew_high_fall_thr --\> 20% from 1 that is 80% from 0 for falling

All 4 are used to calculate slew. Rise variables use to calculate rise
slew and fall for fall slew.Now let's assume another waveform of buffer,
red is input and blue is output

<p align="center">
<img src="./media/image67.png" style="width:5.68958in;height:6.06875in"
alt="image" />
</p>

- in_rise_thr --\> generally 50%.

- out_rise_thr --\> generally 50%

Now consider fall waverofrm

<p align="center">
<img src="./media/image68.png" style="width:5.87917in;height:6.13819in"
alt="image" />
</p>

- in_fall_thr --\> generally 50%

- out_fall_thr --\> generally 50%

All 4 are used to calculate delay. Rise variables use to calculate rise
delay and fall for fall delay.

In case we have negative delay coming, it is because of wrong threshold
pick. So, picking right value of threshold is necessary (Not always
50%).

Another reason for negative delay is, if you have huge wire delays, so
output waveform curve will be very odd. It can lead to negative slew.

# **Day – 3 Design Library Cell using Magic Layout and ngspice Characterization**

## **Lab – IOPlacer Experiment for Equi-distant Bumps**

In openLANE we can make changes on the fly. In current floorplan, all
pins at equidistant (As seen in magic). We can change it by "FP_IO_MODE"
variable.

Currently, this variable set to 1. Change it to 2.

We can see in the below image that when we change the variable to 2 all
the pins adjusted in lower left corner only instead of around whole
design.

<p align="center">
<img src="./media/image69.png" style="width:7.0875in;height:3.13542in"
alt="image" />
</p>

## **Lab – Steps to Gitclone vsdstdcelldesign**

Before proceeding ahead we need to clone the whole directory containing
the std cell design into our local directory and for that we will use
git clone method.

<p align="center">
<img src="./media/image70.png" style="width:7.20568in;height:0.90051in"
alt="Text Description automatically generated" />
</p>

Afterwards, we will run Magic and try to visualize the std cell layout.
The command used for the same is-

`magic -T \<Tech File Path\> \<Path to Layout File\>`

<p align="center">
<img src="./media/image71.png"
style="width:7.67236in;height:0.18701in" />
</p>

This will open the Magic Viewer and we can see the inverter layout
corresponding to different layers.

<p align="center">
<img src="./media/image72.png" style="width:4.34742in;height:4.51118in"
alt="A picture containing treemap chart Description automatically generated" />
</p>

## **Theory – CMOS Fabrication Process**

- Mask 1 : Used for creation of Isolation between wells to protect
  active regions. SiO2-\>Si3N4-\>Mask over active region-\>Oxidation
  (LOCOS)-\>Etch Si3N4

- Oxide not under Si3N4 grows more leading to formation of Bird's beak
  (isolation between wells)

- Mask 2 & 3 : Used to shield parts of substrate and do Ion implantation
  to create NWELL & PWELL, allow dopants to penetrate more into
  substrate by keeping in high temp furnace.

- Mask 4 & 5 : Used to implant dopants into channel region alternatively
  in NWELL and PWELL. Etch damaged SiO2 (due to implantation) and grow
  new SiO2. Deposit Poly and dope it for increased conductivity

- Mask 6 : Used to create poly geometries in the layout

- Mask 7 & 8 : Used to create LDD (P+P-N & N+N-P) using Si3N4
  anisotropic etching spaces to create P- and N- regions of LDD profile.

- Mas 9 & 10 : Used to achieve P+ and N+ of LDD profile due to keeping
  Si3N4 side wall around gate. and do annealing to allow dopants
  penetrate more into substrate.

- Mask 11 : Deposit Ar treated Ti as contacts and heat with N2 creating
  TiN local interconnects. Use mask 11 to etch away TiN in regions where
  contacts need not be brought to upper level.

- Mask 12-16 : Deposit SiO2 and do CMP and use masks 12 to 16 created
  drilling contacts to local interconnects to form higher level routing.

## **Lab – Introduction to Sky130 basic layers layout and LEF using Inverter**

We can view different layers in the magic layout and by over hover a
particular element and pressing ***‘s’*** selects the object and we can
do what over it to understand what it is made of more details.

<p align="center">
<img src="./media/image73.png"
style="width:5.13542in;height:1.64583in" />
</p> 
<p align="center">
<img src="./media/image74.png"
style="width:5.64583in;height:2.05208in" />
</p>

To extract the spef from the current layout we need to use the command
mentioned below –

`- extract all : to extract all data

- ext2spice cthresh 0 rthresh 0 : to extract all parasitic R and C

- ext2spice : generates spice netlist \[.spice\]`

<p align="center">
<img src="./media/image75.png"
style="width:4.76042in;height:0.48958in" />
</p>
<p align="center"> 
<img src="./media/image76.png" style="width:4.40625in;height:1.13542in"
alt="Graphical user interface Description automatically generated with low confidence" />
</p>

Now we can see the spice file getting generated after using the
above-mentioned commands -

<p align="center">
<img src="./media/image77.png" style="width:7.04927in;height:1.43157in"
alt="Text Description automatically generated with low confidence" />
</p>

Sample ext file and spice file are shown in the figure below-

<p align="center">
<img src="./media/image78.png" style="width:6.91936in;height:2.93609in"
alt="Text Description automatically generated" />
</p>
<p align="center"> 
<img src="./media/image79.png" style="width:6.91816in;height:2.65505in"
alt="Text Description automatically generated" />
</p>

Now the SPICE file generated is very rudimentary and in initial stages
this needs to be linked with correct transistor model in order for it to
work. Also we need to create a testbench setup so that we can simulate
the model and see it’s functioning. After updating the spice file by
linking correct libs and setting up the testbench the final file look
like-

<p align="center">
<img src="./media/image80.png" style="width:7.0334in;height:5.2583in"
alt="Text Description automatically generated" />
</p>

Now we can simulate this file using the following command –

`ngspice \<path to the spice model created with testbench\>`

<p align="center">
<img src="./media/image81.png" style="width:7.088in;height:3.66808in"
alt="Text Description automatically generated" /> 
</p>

Now we can plot the timing characteristics of the following inverter
using the command -

`***plot y vs time a***`

<p align="center">
<img src="./media/image82.png" style="width:7.09304in;height:4.275in"
alt="Graphical user interface Description automatically generated" />
</p>

## **Lab – Calculating the Characteristics of an Inverter using ngspice**

We can now effectively calculate the different characteristics of this
inverter using by zooming in the plot and noting down the values for 20%
and 80% output respectively when the input rise or fall is happening.

`Rise Transition– 20% to 80% output

Fall Transition – 80% to 20% output`

20% - ‌<img src="./media/image83.png"
style="width:3.74941in;height:0.36798in" />

80% - <img src="./media/image84.png"
style="width:3.57292in;height:0.32292in" />

On calculating the `***Rise Transition = Fall Transition = 2.23433ns –
2.17797ns = 0.05636ns***`

Now we will calculate the Cell Delay which can be calculated for two
different conditions mentioned below –

- Propagation delay when input is falling

- Propagation delay when input is rising

### **Falling Condition Delay Calculation –**

<p align="center">
<img src="./media/image85.png" style="width:2.64435in;height:2.63017in"
alt="Graphical user interface Description automatically generated" />
</p>

Values 50 % a - <img src="./media/image86.png"
style="width:3.48958in;height:0.3125in" />

Value 50% y - <img src="./media/image87.png"
style="width:2.99173in;height:0.39153in" />

`***Cell Propagation Delay when Input is falling equals to = 2.203ns –
2.152ns = 0.05ns***`

### **Rising Condition Delay Calculation –**

<p align="center">
<img src="./media/image88.png" style="width:2.96856in;height:2.99237in"
alt="Graphical user interface Description automatically generated" />
</p> 
<p align="center">
<img src="./media/image89.png" style="width:2.97613in;height:0.74789in"
alt="Graphical user interface, text Description automatically generated" />
</p>

`***Cell propagation delay when input is rising = 4.0723ns – 4.05ns =
0.023ns***`

## **Lab – Introduction to DRC’s and Downloading DRC Testcase**

We can download the testcase for DRC testing using the wget command
shown below –

<p align="center">
<img src="./media/image90.png"
style="width:6.26806in;height:0.18056in" />
</p>

Once we have downloaded it, please extract the tar using the command,
this will automatically list out and create a dirtectory of all the
files –

`tar – xvf \<tar file name\>`

<p align="center">
<img src="./media/image91.png" style="width:7.00264in;height:3.93579in"
alt="Text Description automatically generated" />
</p>

## **Lab – Loading Sky130 Tech Rules in Magic**

We will launch an emoty magic window using the command mentioned below –

`magic -t sky130.tech`

<p align="center">
<img src="./media/image92.png"
style="width:7.06094in;height:4.11093in" />
</p>

Once launched we can go to File and Open any corresponding file we want
to open, for this example we will open met3.mag for demonstration
purposes.

<p align="center">
<img src="./media/image93.png"
style="width:6.9467in;height:4.01671in" />
</p>
<p align="center">
<img src="./media/image94.png" style="width:6.88178in;height:3.98908in"
alt="A picture containing calendar Description automatically generated" />
</p>
We can use the command `***‘drc why’***` and it can report various DRC
errors which there are in the tool, we can hover our mouse and click s
to select the object and writing dry why will list out all the drc
errors corresponding to that object which is demonstrated in the
snapshot below.

<p align="center">
<img src="./media/image95.png" style="width:7.0875in;height:2.55903in"
alt="Graphical user interface, text, application Description automatically generated" />
</p>

There are some standard commmand / rules provided for the skywater 130nm
Technological process at the following link we can review all the DRC
rules specified by the foundry converned with 130nm process -
<https://skywater-pdk.readthedocs.io/en/main/>

Further, below mentioned snapshot shares the different DRC rules there
are corresponding to the Metal 3 layer which is opened in Magic for
reviewing. All the `***DRC why***` that are mentioned in the terminal have
a code corresponding to any one of the laws/rules mentioned below.

<p align="center">
<img src="./media/image96.png" style="width:6.26806in;height:3.19931in"
alt="Graphical user interface, text, application, email Description automatically generated" />
</p>

Now we will generate a metal island on this layout by left clicking and
right clicking and then pressing p while selecting the metal1 layer. Now
type in the terminal window -

`cif see VIA2`

This will automatically generate via cuts and via on metal3 layer based
on different DRC rules and it will automatically change the pitch or via
design based on DRC regulations.

<p align="center">
<img src="./media/image97.png" style="width:7.0875in;height:3.52917in"
alt="image" />
</p>
<p align="center">
<img src="./media/image98.png" style="width:6.26806in;height:4.05556in"
alt="Square Description automatically generated" />
</p>

Once this is done, we will use a command know as snap int which
basically helps in aligning the selection with the boundary of the
actual design. After turning the snap on we will measure the distance
between the boundary and the via cut and confirm whether that is being
honoured or not. The DRC rule specifies that the distance between last
via cut and metal3 layer should be greater than \> 0.065um.

On checking the box properties, we found that the distance it
automatically kept is 0.1um which is \> 0.065um and honours the DRC
rules automatically.

<p align="center">
<img src="./media/image99.png" style="width:7.0875in;height:2.45625in"
alt="image" />
</p>

## **Lab – Generating the Poly.9 Error**

This lab is for generating the Poly.9 error and understanding how it can
be fixed if such kind of errors are popping out in DRC checks. Currently
the design is DRC proven as shown below and we are using poly.mag as a
sample layout here.

<p align="center">
<img src="./media/image100.png"
style="width:7.11508in;height:4.13299in" />
</p>

Currently there is incorrectly defined rule in DRC with respect to the
Poly.9 error because poly.9 signifies that difference between diff/tap
and poly should be equal to 0.48um and not under it.

<p align="center">
<img src="./media/image101.png"
style="width:7.33893in;height:0.50818in" />
</p>

But in our case currently the distance between ppolyres and poly is less
than 0.48um. We can calculate it by using the box property command.

<p align="center">
<img src="./media/image102.png" style="width:3.36134in;height:3.3768in"
alt="A picture containing chart Description automatically generated" /><img src="./media/image103.png" style="width:3.64948in;height:2.77815in"
alt="A picture containing rectangle Description automatically generated" />
</p> 
<p align="center">
<img src="./media/image104.png" style="width:3.47853in;height:1.37584in"
alt="Text Description automatically generated with medium confidence" /><img src="./media/image105.png" style="width:3.55601in;height:1.64246in"
alt="Graphical user interface, text, application Description automatically generated" />
</p>

Box property stated that the distance between poly and ppolyres is
0.21um which is less than 0.48um and actually this should have been
reported as a DRC violation but it is not.

<p align="center">
<img src="./media/image106.png" style="width:7.15616in;height:1.52463in"
alt="Text Description automatically generated" />
</p>

Now in order to fix it we will open the sky130.tech and update the
conditions there, on opening the sky130.tech file we found two lines
corresponding to poly.9 DRC rules. Both the rules are mentioned below -

<p align="center">
<img src="./media/image107.png" style="width:7.20851in;height:1.594in"
alt="Text Description automatically generated" />
</p>
<p align="center">
<img src="./media/image108.png" style="width:7.19585in;height:3.27669in"
alt="Text Description automatically generated" />
</p>

The main problem seem here was the rule was defined between poly and
other layers but the rule didn’t consider other npolyres or ppolyres
which are very near to the poly metal. So we will add the rules
corresponding to \*poly layers so that these also get reported as
violations.

<p align="center">
<img src="./media/image109.png" style="width:7.25714in;height:1.84901in"
alt="Text Description automatically generated" />
</p>
<p align="center">
<img src="./media/image110.png"
style="width:7.44152in;height:0.81406in" />
</p>

We have used allpolynonres because it covered all the \*poly layers and
creating DRC rules w.r.t them is the goal here. So we have created two
different goals at both the places where epoly.9 was earlier defined.

Now we will load the skytech130.tech file again by using the following
command –

`load tech sky130.tech`

As soon as it is loaded now we are able to see DRC violations being
flagged automatically.

<p align="center">
<img src="./media/image111.png" style="width:2.14499in;height:2.25383in"
alt="Chart, bar chart Description automatically generated" />
</p>

We were able to fix the wrong DRC error and updated it with the correct
definition, so tool automatically flags the poly layer DRC errors.

## **Lab - Lab challenge exercise to describe DRC error as Geometrical Construct**

We will first load the nwell.mag in to the Magic Window, we will use the
same method defined earlier.

<p align="center">
<img src="./media/image112.png"
style="width:7.21788in;height:4.2023in" />
</p>

On further checking we can find that a DRC error is being flagged in the
following layout under the impression of nwell.6. This error basically
says that nwell should be enclosed within deepnwell should be atleast
1.030um.

<p align="center">
<img src="./media/image113.png"
style="width:7.0875in;height:0.38333in" />
</p>

In our case all the three directions, left, right and bottom are showing
exact value of 1.030um measured using the box command. Nwell to deep
nwell overlap is around 1.03um and non-overlap extension is around
0.68um.

<p align="center">
<img src="./media/image114.png" style="width:7.24348in;height:2.81521in"
alt="Text Description automatically generated" />
</p>
<p align="center">
<img src="./media/image115.png" style="width:7.05995in;height:3.49165in"
alt="Graphical user interface Description automatically generated" />
</p>

However, on measuring the top overlap between nwell and deep newel we
found that is only 0.56um which is less than the defined DRC value of
1.03um.

<p align="center">
<img src="./media/image116.png" style="width:7.05881in;height:3.15636in"
alt="Graphical user interface, application Description automatically generated" />
</p>

In order to view these internal layers we have to use the following
commands –

`***Cif ostyle drc***

***Cif see dnwell_shrink***

***Cif see nwell_missing***`

<p align="center">
<img src="./media/image117.png" style="width:7.22969in;height:3.14707in"
alt="Graphical user interface, text Description automatically generated" />
</p>
<p align="center">
<img src="./media/image118.png" style="width:7.20551in;height:3.66742in"
alt="Graphical user interface, text Description automatically generated" />
</p>

We have understood the error and this can be fixed by increasing the
size of nwell region overlap with the deep nwell region and then
re-iteration will resolve the issue.

## **Lab - Lab challenge to find missing or incorrect rules and Fix Them**

Now, it is common knowing that a nwell must have a substrate contact and
it should be tapped atleast at one place. But it was not mentioned as a
DRC rules so in this lab we will be defining those DRC rules in order to
flag a DRC violation whenever a nwell is untapped.

<p align="center">
<img src="./media/image119.png" style="width:7.22724in;height:3.76816in"
alt="Text Description automatically generated" />
</p>

We can see in the below snapshot that no DRC violation error is flagged
for the nwell even if doesn’t have any tap contact.

<p align="center">
<img src="./media/image120.png"
style="width:7.09987in;height:5.01302in" />
</p>
<p align="center">
<img src="./media/image121.png" style="width:7.16247in;height:2.28221in"
alt="Text Description automatically generated" />
</p>

For defining the DRC rule, we will create a templayer and use a command
bloat-all on nwell. Afterwards another temp layer which is nanded with
the nwell-tapped and if the area is equal zero then the max cif style
error will pop up. We are giving it a constraints so that it only runs
when DRC (full) is ran on the design.

<p align="center">
<img src="./media/image122.png" style="width:7.18463in;height:2.08232in"
alt="Graphical user interface, text Description automatically generated" />
</p>
<p align="center">
<img src="./media/image123.png" style="width:7.19047in;height:1.66896in"
alt="Text Description automatically generated" />
</p>
<p align="center">
<img src="./media/image124.png" style="width:7.15257in;height:2.30917in"
alt="Text Description automatically generated" />
</p>

After defining the rule its time to test them, we will load the latest
tech and write drc check, no errors should pop up because the custom DRC
check created will only work when DRC style full is used. To perform
that kindof checks use the command –

`***Drc style drc(full)***`

<p align="center">
<img src="./media/image125.png" style="width:6.26806in;height:1.76875in"
alt="Text Description automatically generated" />
</p>

As soon as the command was run all the nwell not containing the tap
contact are getting flagged as DRC errors.

<p align="center">
<img src="./media/image126.png"
style="width:7.04001in;height:4.43257in" />
</p>
<p align="center">
<img src="./media/image127.png" style="width:7.05106in;height:4.05596in"
alt="Graphical user interface, text Description automatically generated" />
</p>
<p align="center">
<img src="./media/image128.png" style="width:7.0137in;height:4.05234in"
alt="Graphical user interface, text, application Description automatically generated" />
</p>

We have successfully demonstrated and created a custom DRC rule which
runs only when full style DRC is run and is functioning as per
expectations.

# **Day – 4 Pre-Layout Timing Analysis and Importance of a Good Clock Tree**

## **Theory – Introduction to Delay Tables**

Clock Gating – We can imagine 2 different types of clock gating one with
‘and’ and other with ‘or’. When using the ‘and’ gate ‘EN’ signal needs
to be always ‘High’ whereas in ‘or’ gate the ‘EN’ signal needs to be
always ‘Low’.

<p align="center">
<img src="./media/image129.png"
style="width:4.60166in;height:3.36535in" />
</p>

Now the question arises can be replace the pre-existing buffers in out
CTS with an AND gate for performing effective clock gating ? To answer
that we need to investigate certain timing characteristics of the cell
replaced and the Buffer cell.

<p align="center">
<img src="./media/image130.png" style="width:2.90751in;height:2.49538in"
alt="Diagram, schematic Description automatically generated" />
</p>
<p align="center">    
<img src="./media/image131.png" style="width:3.0448in;height:2.47599in"
alt="Diagram, schematic Description automatically generated" />
</p>

In order to replace the cell we need to characterize them and to
characterize them VLSi engineers came up with a solution called as Delay
Tables.

Delay tables are nothing but delay values of the cell when the input
transition time and output load are varied within certain ranges and
those are then characterized and saved in the liberty.

<p align="center">
<img src="./media/image132.png" style="width:3.89834in;height:1.86968in"
alt="A picture containing text, scoreboard, black Description automatically generated" />
</p>

So, if the delay tables are effectively matching with the updated cell,
we can replace the current cells with new ones to which can have a
variety of advantages.

## **Lab – Extracting LEF File from Layout File**

Till now we have completed the cell extraction and characterization now we will convert the corresponding cell to LEF. 
In order to do so initially we will launch a Inverter GUI in a Magic Shell by
using the following command –

`magic -T \<Tech File Path\> \<Mag File\>`

<p align="center">
<img src="./media/image133.png"
style="width:7.0875in;height:0.15694in" />
</p>

Now for proceeding ahead the only information we need as an input are -

1.  Input / Output Pins Location

2.  Cell Area/Boundary Coordinates

3.  Power and Ground Rail Information

We don’t need the logic functioning of the cell and therefore here the
LEF file comes into picture. LEF file in turn protect our IP’s and
doesn’t mention the functioning of the cell but just mentions the above
information.

<p align="center">
<img src="./media/image134.png" style="width:6.30028in;height:5.29221in"
alt="Text Description automatically generated with medium confidence" />
</p>

Our objective for this Lab session will be to extract a LEF file out of
the Mag File. Certain conditions we need to confirm before proceeding
ahead is –

1.  **Rule – 1:** Both Input and Output Pins should lie on the
    intersection of both Horizontal and Vertical Tracks.

2.  **Rule – 2:** The width of the standard cell should be an odd
    integral multiple of the x-pitch defined during floorplan.

3.  **Rule – 3:** The Height of the standard cell should be integral
    multiple of the y-pitch defined floorplan.

We need to find the exact dimensions of the grid where the tracks will
be running to check whether this cell can be placed and routed
effectively or not. The track information can be found under the
following directory –

<p align="center">
<img src="./media/image135.png" style="width:7.0875in;height:1.27778in"
alt="Text Description automatically generated" />
</p>
<p align="center">
<img src="./media/image136.png" style="width:1.88504in;height:2.16363in"
alt="A picture containing text Description automatically generated" />
</p>

This suggests that li1 layer has Horizontal Tracks of Pitch 0.46 with
the origin from 0.23. Similarly, we can understand for the vertical li1
layer Pitch is 0.34 and Origin is at 0.17. We will try to replicate this
grid on Magic so that we can verify the above mentioned two conditions.
To do so we will have to use `***grid***` command in magic shell shown
below –

<p align="center">
<img src="./media/image137.png" style="width:7.0875in;height:6.03819in"
alt="Graphical user interface, application, Excel Description automatically generated" />
</p>

The above-mentioned Figure clearly depicts that Rule Number 1 mentioned
above stating that both input and output pin must lie over a crossing
Horizontal and Vertical tracks is honoured.

Also, Rule 2 and Rule 3 are being honoured as the Standard cell in X
direction is 3 times the grid-x and Y direction is 8 times the grid-y
value.

Now for successful conversion of Layout File in LEF file we need to
define the Ports which will be treated as pins in LEF File. To do so
please follow the Step-by-Step procedure mentioned below –

1.  Step – 1. Hover you mouse over the place where you want a port
    assignation. Press s until the required metal/place is selected.

2.  Step – 2. Now after selection go to ***Edit \>\> Text***, this will
    pop-up a dialogue box.

<p align="center">
<img src="./media/image138.png" style="width:6.26806in;height:3.61389in"
alt="Chart Description automatically generated" />
</p>

3.  Step – 3. Fill the Name of the Pin, Size of the Text Label, Change
    the Attach to Layer (locali in our case) option Sticky and Provide a
    Port number corresponding to each pin which should be unique.

4.  Step – 4. Perform this same thing for rest of the ports as well, Z ,
    VPWR and VGND.

<p align="center">
<img src="./media/image139.png" style="width:2.51172in;height:3.30315in"
alt="Graphical user interface, application Description automatically generated" />
</p>

<p align="center">
<img src="./media/image140.png" style="width:2.34755in;height:3.28557in"
alt="Diagram Description automatically generated with medium confidence" />
</p>

5.  Step – 5. Now we need to provide characteristics for each and every
    type of pin, every port can have a class Input, Output or InOut,
    whereas different use cases can be defined for each pin. Please
    follow the steps mentioned in the figure below for assigning
    characteristics to every pin in the layout.

<p align="center">
<img src="./media/image141.png" style="width:5.55024in;height:4.66353in"
alt="Text Description automatically generated" />
</p>

6.  Step – 6. Now we will save the following file as sky130_vsdinv.mag
    to mark it as customized inv.

7.  Step – 7. Open the new Layout file and in the terminal write `'***lef
    write***'` this will output a LEF file from the layout file.  

<p align="center">    
    <img src="./media/image142.png" style="width:4.03226in;height:1.33609in"
    alt="Text Description automatically generated" />
</p>

Just for reference, we will open the LEF generated to understand the
steps of Port creation done in the previous stage. An example LEF
generated after the above operations is shown in the figure below –

<p align="center">
<img src="./media/image143.png" style="width:4.73636in;height:4.18525in"
alt="Text Description automatically generated" />
</p>

We can see that the LEF retains the characteristics defined by us in the
Magic and also retains the geometry of selection where the text was
defined and now all the ports defined are changed to corresponding Pins.
The port number defined in the previous stage controls the definition
order of the Pins in the custom LEF.

## **Lab – Data Preparation for Including Custom LEF inverter in openlane Flow**

To include the LEF file into the current openlane flow copy the newly
generated custom LEF into the src folder for out particular design.
Apart from that we also need to copy the required liberties for the same
cell so that the tool will understand the functionality of these lefs.
Please note that the libs should contain the information for the
following custom cell ***‘sky130_vsdinv’***.

<p align="center">
<img src="./media/image144.png"
style="width:7.0875in;height:1.05903in" />
</p>
<p align="center">
<img src="./media/image145.png" style="width:3.33596in;height:4.28804in"
alt="Text Description automatically generated" />
</p>

There are 3 different libraries present which need to be copied, please
note that all of them are characterized for a different process corner.

## **Lab – Running OpenLane with including New Custom INV cell**

Beforee we run the docker command and start a new synthesis with custom
INV cell we need to set the configuration parameters so that the tool
understands and pick these files during synthesis. For that please go
the design section and open config.tcl.

<p align="center">
<img src="./media/image146.png"
style="width:7.0875in;height:1.20694in" />
</p>

Under config.tcl add the new liberties and the lef’s path so that they
can be used/selected during the synthesis and become a part of the
openlane flow.

<p align="center">
<img src="./media/image147.png" style="width:7.0875in;height:2.87014in"
alt="Text Description automatically generated" />
</p>

Now we will run the docker command again and launch a Openlane shell.
But we need to override the current work done with the pre-existing inv
cell. For launching overwriting in a pre-generated run please use the
following command –

`prep -design picorv32a -tag \<directory name\>`

After running this, we need to set the lef’s again so that openlane
takes our Lef files –

<p align="center">
<img src="./media/image148.png"
style="width:6.26806in;height:0.775in" />
</p>

Next step is to finally run the synthesis again using
`***‘run_synthesis’***` command. While the run is progressing it will
generate a table which will list out the total number of used cell for
each type of cell. Verify the number of cells used for the custom
inverter ***“sky130_vsdinv”***.

<p align="center">
<img src="./media/image149.png" style="width:4.25717in;height:2.11868in"
alt="Text Description automatically generated with low confidence" />
</p>

We have successfully incorporated the custom INV cell into our picrv32a
design. But we can still see that there is a big violation in terms of
min and max slew.

<p align="center">
<img src="./media/image150.png" style="width:4.07453in;height:0.92271in"
alt="Text Description automatically generated" />
</p>

Afterwards, we will run the run_floorplan and run_placement command to
generate a post-placed lef and def, which can be viewed in Magic. We can
verify that the cells we generated are being used or not in the def by
finding the sky130_vsdinv cell in magic. Currently there is no way of
searching the cell so we will have to do it manually.

<p align="center">
<img src="./media/image151.png" style="width:5.28333in;height:3.632in"
alt="Timeline Description automatically generated" />
</p>

## **Lab – Resolving Huge Timing Violations Observed**

In our previous lab we observed very high timing violation but a good
news was our custom LEF cell is getting picked by yosys automatically.
Now in order to correct the timing violation we shall alter a few
settings in order to make our synthesis run based on updated
configurations. In order to make our setting more timing aware we will
have to make our peace with some area penalty and for telling that to
openlane we will use the following settings -

<p align="center">
<img src="./media/image152.png" style="width:3.57591in;height:2.08118in"
alt="Text Description automatically generated" />
</p>

Before running the synthesis do make sure we delete the previous RTL
file generated by run_synthesis. And then run the command
`***‘run_synthesis’***`

<p align="center">
<img src="./media/image153.png" style="width:4.51099in;height:1.52132in"
alt="Text Description automatically generated" />
</p>

This basically shows that our slack has drastically reduced and is only
slightly negative now. But it comes with a Area Penalty, and also this
time usage for our custom Inv has increased automatically.

<p align="center">
<img src="./media/image154.png" style="width:4.43358in;height:1.56742in"
alt="Text Description automatically generated" />
</p>

`%age Area Increase = (209181.872 – 147950.6464) / 147950.6466 \* 100 =
**41.3%**`

`%age decrease in slack = (-26.53 – (-2.95)) / (-26.53) \* 100 =
**88.88%**`

Now we will again `***‘run_floorplan’***` and `***‘run_routing’.***` We can
confirm from the DEF that the custom cell should be present in the
updated def from the floorplan. In our case the cell is present and it
is being used by yosys during synthesis effectively.

<p align="center">
<img src="./media/image155.png" style="width:3.74135in;height:1.80684in"
alt="Text Description automatically generated" /><img src="./media/image156.png" style="width:2.44673in;height:1.79893in"
alt="Text Description automatically generated" />
</p>

We can also view the same in Magic and confirm it from there as well.
After selecting the cell in magic, if we use command ***‘expand’,***
Magic will show the LEF view for the cell showing the connectivity to
the VDD & VSS Rails.

<p align="center">
<img src="./media/image157.png" style="width:6.472in;height:3.80492in"
alt="Graphical user interface, application Description automatically generated" />
</p>

## **Theory – Understanding Static Timing Analysis**

Hold Time: Hold time is defined as the minimum amount of time after the
clock's active edge during which data must be stable.

Setup Time: Setup time is the minimum amount of time the data signal
should be held steady before the clock event so that the data are
reliably sampled by the clock.

In real cases the combination delay should be less than `***Time Period –
Setup Time***` for the Next Flop

STA is relatively easy to resolve when the clocks are assumed as ideal
but in real case clocks there are lot of uncertainties involved like
clock Jitter, clock delays, buffer uncertainties etc. So due to which
the actual start point of the clock can either shift in forward or
backward direction known as clock jitter. Clock Jitter is accurately
represented by the below figure.

<p align="center">
<img src="./media/image158.png" style="width:7.0875in;height:1.49861in"
alt="Graphical user interface Description automatically generated" />
</p>

Now the formulation of combination delay changes to `***Time Period –
Setup Time – Setup Uncertainty***` in which setup uncertainty is driven
from the clock jitter.

<p align="center">
<img src="./media/image159.png" style="width:7.0875in;height:3.37431in"
alt="Graphical user interface Description automatically generated" />
</p>

## **Lab – Setting up STA Analysis for Picorv32a design \[OpenSTA\]**

After performing the routing we saw that out design still is prone to
STA issues, now we will be running the STA tool in this lab in order to
resolve the upcoming issue. But before running STA we need to feed
different configuration parameters to the tool so that it calculates STA
on our latest design generated till now.

For that we will create a file called pre_sta.conf and we need to define
different parameters in it so we know what are we reading and on what
the tool functions.

<p align="center">
<img src="./media/image160.png" style="width:7.21397in;height:1.85824in"
alt="Text Description automatically generated" />
</p>

Please note that we also need to define a new input here which is the
Synopsys Design Constraints File (SDC) which is required for
understanding the clocks that will be traced through the design. It
defines various characteristics of the clock present in the design like
name, frequency, port address, delay , critical paths etc.

Please note that we need to define the correct Driving Cell that will be
used for performing CTS. Along with correct characteristics for the
same.

`***‘Create_clock’***` is the main command which will generate the clock
at a certain position in the design.

<p align="center">
<img src="./media/image161.png"
style="width:6.99633in;height:3.80589in" />
</p>

## **Lab – Setting up STA Analysis for Picorv32a design \[OpenSTA\]**

Next step will be to run STA on the design in order to do so, go to your
linux shell an type the following command –

`sta pre_sta.conf`

<p align="center">
<img src="./media/image162.png" style="width:6.91896in;height:1.51089in"
alt="Text Description automatically generated" />
</p>

Now after this is run, it will report the slack values, if the slack
values are still negative we might have to do some tweaking. In our case
min and max slew were both reported to be 0 therefore no further
tweaking of setup is required to resolve it.

<p align="center">
<img src="./media/image163.png" style="width:6.26806in;height:4.59444in"
alt="A picture containing text Description automatically generated" />
</p>

## **Theory – Clock Tree Synthesis**

Clock tree synthesis mean to create such a network for the clock so that
the slew should be as close to 0 as possible throughout the design. The
routing needs to be done in such a manner that slew can be minimized.

<p align="center">
<img src="./media/image164.png" style="width:7.0875in;height:3.47986in"
alt="Graphical user interface Description automatically generated" />
</p>

If we randomly do clock tracing by connecting clock paths anywhere the
wirelength for the clock will change which will increase the capacitance
and the there will be slew violations. We need to make the clock paths
consistent and equivalent so that the cap seen by the clock path is
uniform in all direction. In order to achieve so there is a strategy
called as Mid – Point Strategy or H shaped clock in which a mid-point is
chosen for a number of flops connecting and that midpoint delivers the
clock path uniformly in each direction as shown in figure below.

<p align="center">
<img src="./media/image165.png"
style="width:7.0875in;height:3.49861in" />
</p>

Second step after planning the path is clock buffer insertion, this is a
very important aspect because the clock nets are getting connected to
thousand of registers at once and this could lead to very high cap
values, due to input pin caps and long wire-length. So, to improvise the
situation clock buffers are inserted at different places in a uniform
manner so that the clock slew remain unaffected and all signal integrity
issues are resolved.

<p align="center">
<img src="./media/image166.png"
style="width:7.0875in;height:3.46181in" />
</p>

## **Theory – Clock Net Shielding and Crosstalk’s**

When multiple different nets are running parallel to each they can have
a coupling capacitance among them due to which the other net can get
triggered. This phenomenon is called as crosstalk.

Crosstalks can be of two types Near End Crosstalks and Far End
Crosstalks, which are depiced using the diagram below –

<p align="center">
<img src="./media/image167.png" style="width:5.07361in;height:3.424in"
alt="Generation of NEXT and FEXT | Download Scientific Diagram" />
</p>

Now due to these crosstalk a phenonmenon known as glitch can happen,
which basically is just unintentional switching of a line due to
crosstalk, due to coupling capacitance when there is a sudden transition
in one of the wires, it cause it’s neighbouring wires to get affected
and cause a small change in their waveform which if is greater than the
voltage threshold can cause glitch and false triggering which can be
veru harmful to the design.

<p align="center">
<img src="./media/image168.png"
style="width:5.69509in;height:2.75101in" />
</p>

In order to avoid these Crosstalk’s and glitches in the design we have
to apply a strategy known as clock shielding. Main idea behind this
shielding is to keep a parallel VSS/VDD ground running near between the
clocks so that the coupling cap reduces. Because VDD and VSS generally
don’t switch and therefore the actual glitch appearing due them will be
almost nil and wont harm the circuitry as well as logic.

## **Lab – Running CTS on Passed STA design using TritonCTS**

There are only few settings which are provided to Openlane for
performing the CTS. We can use the default values as it is to run Clock
Tree Synthesis.

<p align="center">
<img src="./media/image169.png"
style="width:7.0875in;height:1.25208in" />
</p>

To run CTS now we need to use the following command in the openlane
shell–

`run_cts`

<p align="center">
<img src="./media/image170.png"
style="width:7.18612in;height:1.75712in" />
</p>

The basic setting from which the CTS picks the proc values are
openroad/or_cts.tcl under scripts or from the

<p align="center">
<img src="./media/image171.png" style="width:3.43864in;height:2.66413in"
alt="Text Description automatically generated" />
</p>
<p align="center">
<img src="./media/image172.png" style="width:3.24761in;height:2.66256in"
alt="Text Description automatically generated" />
</p>
We can verify the same values from the openlane shell as well by echoing
each and every variable accordingly –
<p align="center">
<img src="./media/image173.png"
style="width:6.26806in;height:0.91597in" />
</p> 
<p align="center">
<img src="./media/image174.png" style="width:6.26806in;height:1.16806in"
alt="Text Description automatically generated" />
</p>
After running CTS, a new def will be generated which will contain all
the clock buffers inserted and the CTS routed. Now due to this process
the slack can be effected which can cause more STA violations. So
basically we need to perform STA over the Post-CTS netlist and confirm
whether the slack values are violating or not.

## **Lab – Running STA again on POST CTS Netlist**

In order to perform STA on the Post CTS netlist we need to launch
openROAD under openLANE shell. Which is easy we have to write the
following command in the shell to launch it –

`openroad`

It will perform the basic checks and load the design and set the LEF and
DEF for us to perform further actions.

<p align="center">
<img src="./media/image175.png"
style="width:6.65992in;height:2.22022in" />
</p>
Now since this step might require some iterations we will do it by
saving the design each time in a db and then re-checking again and again
until we have resolved the STA issues.

To create a db and set different variables, please use the commands
shown below, we need to generate the reports in order to get values of
min and max slack.

<p align="center">
<img src="./media/image176.png" style="width:7.17891in;height:2.82989in"
alt="Text Description automatically generated" />
</p>

After checking the reports again, we observed min and max slack
violations. Min slack now observed was `-2.153` and Max Slack now observed
was `-3.1580`.

<p align="center">
<img src="./media/image177.png" style="width:6.26806in;height:1.85139in"
alt="Text Description automatically generated" />
</p>
<p align="center">
<img src="./media/image178.png" style="width:6.26806in;height:3.50833in"
alt="Text Description automatically generated" />
</p>

Now we will alter the library and use the typical library to
characterize the cell and recalculate the slack values based on that.
For that we just need to reload the db and change the parameters
accordingly which were not saved in the db.

<p align="center">
<img src="./media/image179.png"
style="width:6.96636in;height:2.4613in" />
</p>

After library change we observed that the min slack value changed to
`-0.0672` and Max slack value changed to `5.1873.`

<p align="center">
<img src="./media/image180.png" style="width:7.0458in;height:1.82351in"
alt="Text Description automatically generated" />
</p>
<p align="center">
<img src="./media/image181.png" style="width:7.00643in;height:2.99166in"
alt="Text Description automatically generated" />
</p>

Now since one of the slacks has improved, we will do some other changes
like replacing the buffer_1 with other buffers and re-calculating the
slack. In order to remove the buffer from the used buffer list please
use the following commands -

<p align="center">
<img src="./media/image182.png"
style="width:7.10811in;height:1.80498in" />
</p>
<p align="center">
<img src="./media/image183.png" style="width:7.09143in;height:1.19186in"
alt="Text Description automatically generated" />
</p>

Now we have verified that the DEF used is correct and the buffer cell
list is also correct so we will run the openroad again and recalculate
the reported slacks.

<p align="center">
<img src="./media/image184.png" style="width:7.17134in;height:4.17997in"
alt="Text Description automatically generated" />
</p>
<p align="center">
<img src="./media/image185.png" style="width:7.18354in;height:1.33706in"
alt="Text Description automatically generated" />
</p>

After this the new final min updated slack is `0.2397` and maximum slack
is `5.4044.` Since both the slacks are positive now we can stop these
iterations and generate a final Post-CTS def for further procedures.
<p align="center">
<img src="./media/image186.png" style="width:7.17348in;height:2.94776in"
alt="Text Description automatically generated" />
</p>
<p align="center">
<img src="./media/image187.png" style="width:7.14504in;height:1.92598in"
alt="A screen shot of a computer Description automatically generated with low confidence" />
</p>

Finally we will check the reported skew values as well, which are
mentioned in the below figure –
<p align="center">
<img src="./media/image188.png" style="width:4.3375in;height:2.52532in"
alt="A picture containing text Description automatically generated" />
</p>

# **Day – 5 Final Steps for RTL2GDS using TritonRoute and openSTA**

## **Theory – Understanding Routing Algorithms**

Routing Algorithm basically tends to find the best way to connect from
one pin (source) to another (destination) with least number of twists
and turns. To do this, there are number of algorithms which can be
implemented –

1.  Maze Routing (Lee’s Algorithm)

2.  Line Search Algorithm

3.  Stainer Tree Algorithm

We will discuss more about Maze Routing in detail as rest of the
algorithms also work on the same principle of minimum routing with a
little tweak.

Steps for performing Maze Routing –

1.  Step 1. Creates a grid around the whole design.

2.  Step 2. Mark the two Standard Cells as Source (X) and Target (Y).

3.  Step 3. Tool marks all the nearby unit grid around the source pin
    as 1. Please note that only the clear adjacent one (no diagonals)
    are marked.

4.  Step 4. Next it takes each adjacent unit grid blocks for the block
    marked as 1 and mark them as 2.

5.  Step 5. Keep a note of the places where there is macro blockage or
    any placement/routing blockage and don’t propagate/overlap/mark
    those unit grid boxes.

6.  Step 6. Keep repeating this pattern till the pin neighbour is
    reached.

7.  Step 7. Algorithm tracks down all the paths which are reaching from
    Source to Destination.

8.  Step 8. Chooses the smallest paths with least number of twists and
    turns.

<p align="center">
> <img src="./media/image189.png"
> style="width:6.07707in;height:4.84212in" />
</p>

> Limitation of Maze Algorithm –

1.  The method performs this kind of step for every instance pin
    connection which in turn is a bulky and time-consuming method.

2.  For bigger design with millions of pins the memory requirement will
    go up and it can’t be performed for very big designs.

## **Theory – DRC Checks for Routing**

There are a thousand of rules involved while routing a particular
design. Design rules can vary based on the Layer of routing, structure,
and orientation of the routing, technology of manufacturing etc. One of
the simplest DRC’s that are appliable to the design are showcased in the
below figure. DRC rules are also specified by the foundry based on the
methodology of Optical lithography because of which them they have
physical boundaries which need to be reflected and respected in the GDS
design else the chip wont fabricate as per expectations. Three different
rules that are applicable to this type of routing are –

1.  Minimum Width of the Wire for a layer

2.  Optimal Wire Pitch between two adjacent parallel wires.

3.  Minimum Wire Spacing

<p align="center">
<img src="./media/image190.png"
style="width:6.20093in;height:3.20254in" />
</p>
<p align="center">
<img src="./media/image191.png"
style="width:3.19633in;height:2.704in" />
</p>
<p align="center">
<img src="./media/image192.png" style="width:3.1532in;height:2.76097in"
alt="A screenshot of a video game Description automatically generated" />
</p>

## **Lab – Creating Power Distribution Network on Post-CTS design**

To run routing over the design, we need to reload our post-cts database.
To do so launch openlane shell under docker and use the following
command –

`*./flow.tcl -interactive*

*Package require openlane 0.9*

*Prep -design picorv32a -tag \<run_area name\>*`

After loading the run-area, to check the correctness, we need to confirm
whether the selected def is correct or not. For performing routing, we
need to use a post-cts def.

<p align="center">
<img src="./media/image193.png"
style="width:6.26806in;height:0.51597in" />
</p>

### **Created PDN Details and Statistics**

Next steps would be to generate the PDN rails before performing signal
routing. But in our case the PDN was already pre-generated during the
floorplan itself. We can review the pitch and width of the rails
generated for PDN from the log and all the standard cells must adhere to
integral multiples of the pitch defined in the log.

<p align="center">
<img src="./media/image194.png" style="width:7.0875in;height:4.02569in"
alt="Text Description automatically generated" />
</p>

We can check the statistics for pdn creation under the log generated
under results/7-pdn.log. Number of nodes for Vpwr and Vgnd created for
this design are shown below –

<p align="center">
<img src="./media/image195.png"
style="width:7.0875in;height:0.71389in" />
</p>
<p align="center">
<img src="./media/image196.png"
style="width:7.0875in;height:0.52014in" />
</p>

Example of PDN is shown in the figure below, power basically enter the
die through IO Pads and then reaches the ring/rails ultimately from
their connecting to each standard cell. So from the IO pads present in
Met4 and Met5 eventually from there the metal lines are dropped down to
metal1 and finally gets connected to the Rails.

<p align="center">
<img src="./media/image197.png"
style="width:6.26806in;height:4.15208in" />
</p>

## **Theory – Understanding TritonRoute**

In actual industry the routing process is very complicated as the
insertion space is huge that’s why TritonRoute works as a twostep
process.

1.  Fast Route – It is coarse global route in which the whole die is
    divided into tiles and very basic routing is performed. Here in this
    demonstration Global Routing Is performed by FastRoute. Output of
    Fast Route is basically fed to Detail route it only creates grid
    cells and tiles in which the TritonRoute will use its algorithm for
    having the best routing with least twists and turns.

2.  Detail Route – This is a more detailed routing while goes till cell
    level and has higher optimizations to get the best routing possible.
    In our case this is performed by TritonRoute.

<p align="center">
<img src="./media/image198.png" style="width:7.0875in;height:2.96319in"
alt="Diagram Description automatically generated" />
</p>

TritonRoute (Detailed Routing) takes in inputs like LEF/DEF and
preprocessed route and outputs a wirelength and Via optimized routed
def. It basically works on different constraints either provided by the
users or by the design technologies. Few features of Triton Route are
discussed below –

1.  Performs initial detailed route.  
      
    Figure shown below how transitioning happens from FastRoute to
    Triton Route. Initial route guide has 4 metal structures, but it
    will post process it finally so that each metal layers is consistent
    i.e. M1 is in vertical direction and M2 is in Horizontal direction
    which should be orthogonal to each other.

<p align="center">
<img src="./media/image199.png"
style="width:6.31914in;height:3.89575in" />
</p>

2.  Honours the pre-processed routed guides from Fastroute.

3.  Assumes route guides for each net satisfy inter-guide connectivity.

<p align="center">
<img src="./media/image200.png" style="width:6.34772in;height:3.13219in"
alt="Text Description automatically generated" />
</p>
<p align="center">
<img src="./media/image201.png" style="width:1.60838in;height:2.43885in"
alt="Chart Description automatically generated with medium confidence" />
</p>
<p align="center">
<img src="./media/image202.png"
style="width:1.70833in;height:2.51042in" />
</p>

4.  Works on MILP based panel routing scheme with Intra-Layer parallel
    and inter-layer sequential routing framework.

It basically means that routing is done sequential like M1 then M2 then
M3 so on but when M1 is happening it will happen in parallel for
different even and odd tiles. But once M1 finished then only M2 will
start till and thereby following the chain like this.

<p align="center">
<img src="./media/image203.png" style="width:6.28087in;height:3.63769in"
alt="Graphical user interface, text Description automatically generated" />
</p>

## **Theory – Routing Algorithm of TritonRoute**

The algorithm used for TritonRoute is fairly simple and it basically
stores the Point 1 to Point 2 multiple routes and their corresponding
cost (could be a factor of wire length) and once the matrix is defined
it basically runs a Minimum Spanning Tree in order to reduce the cost
which basically reduces the total wire length. But note that few other
complications like tweaking and turning are also handled during this
process.

<p align="center">
<img src="./media/image204.png" style="width:6.62547in;height:3.89894in"
alt="Text Description automatically generated" />
</p>

## **Lab – Routing the Design using TritonRoute**

Next steps after connecting the Power and Ground Rails and generating
the complete PDN is to connect the rest of the design for which
TritonRoute is used. Before proceeding with routing the DEF selected
should be post PDN def. In order to run TritonRoute for routing the
design perform the following command –

`*Run_routing*`

<p align="center">
<img src="./media/image205.png"
style="width:6.26806in;height:0.50417in" />
</p>

This run_routing is controlled by using the following configuration
parameters. These parameters can control the routing layers, number of
iterations, routing engine etc. for performing detailed routing. As
explained in tutorial there are about 4 different TritonRoute engines.
Here we have used ROUTING_STRATEGY 0 for demonstration purposes.

<p align="center">
<img src="./media/image206.png" style="width:7.0875in;height:3.1in"
alt="Text Description automatically generated" />
</p>

### **Logs and Reports from Triton Route**

After running run_routing tool will perform a lot of iterations for
optimizing the routing through which it will obtain the best solution
for routing. Please note that tighter the optimization constraints
higher will be the run-time.

<p align="center">
<img src="./media/image207.png" style="width:6.26806in;height:2.15in"
alt="Text Description automatically generated" />
</p>

In our case we see 0 violations, if there are some violations then in
that case a DRC file will be generated. That DRC needs to be validated
and the errors needs to be fixed manually.

This completes the whole process from synthesis to routing and now the
die is functional, and signoff needs to be performed to test the chip
whether it’s performing the required functionality within the Power and
Area boundaries or not.
