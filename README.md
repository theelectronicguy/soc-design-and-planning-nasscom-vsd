
# Digital VLSI SoC Design and Planning - Performed By Ashu Babbar

A 2 Week digital VLSI SoC design and planning workshop with complete RTL2GDSII flow organised by VSD in collaboration with NASSCOM

08/01/25 - 22/01/25

<details>
  <summary><strong>Section 1 - Sky130 Day 1: Inception of open-source EDA, OpenLANE and Sky130 PDK</strong></summary>


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
```
#Step-1: Design Preparation Stage
```
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

<img width="947" alt="Screenshot 2025-01-13 022842" src="https://github.com/user-attachments/assets/f1e60f8e-1d71-4f58-8564-2d77ac603958" />

This creates a 'runs' directory:

<img width="809" alt="Screenshot 2025-01-13 031020" src="https://github.com/user-attachments/assets/ef2710ee-d063-4159-817c-02c5ad0eb76f" />

note: Config.tcl shows all parameters that it may use to run

#step-2: run the synthesis using run_synthesis command
<img width="959" alt="Screenshot 2025-01-13 032513" src="https://github.com/user-attachments/assets/a6984555-b508-46fd-b3a3-16730e2f17fd" />

Calculating Flop Ratio and % DFF:

<img width="383" alt="Screenshot 2025-01-13 034544" src="https://github.com/user-attachments/assets/6d5718f4-b5b8-4908-9f93-fb9dc6c1d6a9" />

<img width="304" alt="Screenshot 2025-01-13 034406" src="https://github.com/user-attachments/assets/dca488db-3e1a-4306-ae22-e6cb44a9b7e7" />

After synthesis , we can go to results folder and see the synthesised report

![Screenshot 2025-01-13 035815](https://github.com/user-attachments/assets/af2e87fa-4fec-4f9b-8e03-5c628e7dca2e)

Synthesized Result File: 
<img width="952" alt="Screenshot 2025-01-13 035727" src="https://github.com/user-attachments/assets/a160fcf4-39fa-4ba2-a252-8184eb348fbb" />
</details>

<summary><strong>Section 2 - Good floorplan vs bad floorplan and introduction to library cells</strong></summary>
We execute the run_floorplan command as below:

<img width="914" alt="Screenshot 2025-01-15 022839" src="https://github.com/user-attachments/assets/18797e70-0a01-4710-b478-07ea71aa1a3b" />
<img width="959" alt="Screenshot 2025-01-15 023316" src="https://github.com/user-attachments/assets/5ad2d32d-ea5e-4519-a825-5a1c503a1dfd" />



