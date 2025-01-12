
# Digital VLSI SoC Design and Planning

A 2 Week digital VLSI SoC design and planning workshop with complete RTL2GDSII flow organised by VSD in collaboration with NASSCOM

08/01/25 - 22/01/25


## Section 1
Sky130 Day 1 - Inception of open-source EDA, OpenLANE and Sky130 PDK

1. Run 'picorv32a' design synthesis using OpenLANE flow and generate necessary outputs.
Commands to invoke the OpenLANE flow and perform synthesis

```
vsduser@vsdsquadron:~/Desktop/work/tools/openlane_working_dir/openlane$ docker
bash-4.2$ ./flow.tcl -interactive
[INFO]: 
	___   ____   ___  ____   _       ____  ____     ___
	/   \ |    \ /  _]|    \ | |     /    ||    \   /  _]
	|     ||  o  )  [_ |  _  || |    |  o  ||  _  | /  [_
	|  O  ||   _/    _]|  |  || |___ |     ||  |  ||    _]
	|     ||  | |   [_ |  |  ||     ||  _  ||  |  ||   [_
	\___/ |__| |_____||__|__||_____||__|__||__|__||_____|


[INFO]: Version: v0.21
[INFO]: Running interactively
% package require openlane 0.9
0.9
% prep -design picorv32a 
[INFO]: Using design configuration at /openLANE_flow/designs/picorv32a/config.tcl
[INFO]: Sourcing Configurations from /openLANE_flow/designs/picorv32a/config.tcl
[INFO]: PDKs root directory: /home/vsduser/Desktop/work/tools/openlane_working_dir/pdks
[INFO]: PDK: sky130A
[INFO]: Setting PDKPATH to /home/vsduser/Desktop/work/tools/openlane_working_dir/pdks/sky130A
[INFO]: Standard Cell Library: sky130_fd_sc_hd
[INFO]: Sourcing Configurations from /openLANE_flow/designs/picorv32a/config.tcl
[INFO]: Current run directory is /openLANE_flow/designs/picorv32a/runs/12-01_20-40
[INFO]: Preparing LEF Files
[INFO]: Extracting the number of available metal layers from /home/vsduser/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.ref/sky130_fd_sc_hd/techlef/sky130_fd_sc_hd.tlef
[INFO]: The number of available metal layers is 6
[INFO]: The available metal layers are li1 met1 met2 met3 met4 met5
[INFO]: Merging LEF Files...
mergeLef.py : Merging LEFs
sky130_fd_sc_hd.lef: SITEs matched found: 0
sky130_fd_sc_hd.lef: MACROs matched found: 437
sky130_ef_sc_hd__fill_12.lef: SITEs matched found: 0
sky130_ef_sc_hd__fill_12.lef: MACROs matched found: 1
sky130_ef_sc_hd__decap_12.lef: SITEs matched found: 0
sky130_ef_sc_hd__decap_12.lef: MACROs matched found: 1
sky130_ef_sc_hd__fakediode_2.lef: SITEs matched found: 0
sky130_ef_sc_hd__fakediode_2.lef: MACROs matched found: 1
mergeLef.py : Merging LEFs complete
[INFO]: Trimming Liberty...
[INFO]: Generating Exclude List...
[INFO]: Storing configs into config.tcl ...
[INFO]: Preparation complete

```








