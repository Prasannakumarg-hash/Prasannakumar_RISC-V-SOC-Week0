# Introduction 🚀

This repository serves as a personal log of my journey into the world of **VLSI (Very Large-Scale Integration)**. It documents the initial steps of setting up a development environment using a virtual machine and installing key open-source tools required for digital design and simulation. The purpose is to create a transparent, reproducible, and easy-to-follow guide for others who are starting out.

***

### Objective 🎯

The primary objective of this project is to:

- **Set up a robust VLSI design environment** on a virtual machine.
- **Install essential open-source tools** like Yosys, Icarus Verilog, and GTKWave.
- **Document the entire process** from system configuration to tool verification.
- **Create a reproducible setup** that can be easily replicated by others, serving as a foundational guide for more complex VLSI projects.
# 🚀 VLSI Tools Installation and Setup

This repository documents the process of setting up a Virtual Machine for VLSI (Very Large Scale Integration) design and installing essential open-source tools. The steps are based on the Day 0 - Tools Installation guide.

-----

## 💻 System Configuration

To get started, a virtual machine with the following specifications was set up:

  - **OS:** Ubuntu 20.04+ 🐧
  - **RAM:** 6 GB
  - **HDD:** 50 GB
  - **CPU:** 4 vCPU

The virtual machine was created using Oracle VirtualBox. You can download it from the [VirtualBox Downloads page](https://www.virtualbox.org/wiki/Downloads).

-----

## 🔧 Tools Installation and Verification

The following open-source VLSI tools were installed and verified. Snapshots of the verification process are included.

### 1\. Yosys

**Yosys** is a framework for Verilog synthesis. It transforms your Verilog code into a gate-level netlist.

**Installation Steps:**

1.  Update your package list:
    ```bash
    $ sudo apt-get update
    ```
2.  Clone the Yosys GitHub repository:
    ```bash
    $ git clone https://github.com/YosysHQ/yosys.git
    ```
3.  Navigate into the Yosys directory:
    ```bash
    $ cd yosys
    ```
4.  Install the required dependencies:
    ```bash
    $ sudo apt install make
    $ sudo apt-get install build-essential clang bison flex libreadline-dev gawk tcl-dev libffi-dev git graphviz xdot pkg-config python3 libboost-system-dev libboost-python-dev libboost-filesystem-dev zlib1g-dev
    ```
5.  Configure the build environment:
    ```bash
    $ make config-gcc
    ```
6.  Compile Yosys:
    ```bash
    $ make
    ```
7.  Install Yosys to your system:
    ```bash
    $ sudo make install
    ```
   

**Verification:**
After installation, the tool was verified by running the `yosys` command in the terminal.

<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/b9698a4f-078e-4ac7-860a-34a179f9a26c" />

### 2\. Icarus Verilog (Iverilog)

**Iverilog** is a Verilog compiler that compiles Verilog HDL into a format suitable for simulation.

**Installation Steps:**

1.  Update your package list:
    ```bash
    $ sudo apt-get update
    ```
2.  Install Iverilog using `apt-get`:
    ```bash
    $ sudo apt-get install iverilog
    ```

**Verification:**
The installation was verified by checking the tool's version with `iverilog -v`.

<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/d736a2c7-f48b-4c7c-b9de-abe950aa345e" />

### 3\. GTKWave

**GTKWave** is a waveform viewer used to visualize simulation results from tools like Iverilog.

**Installation Steps:**

1.  Update your package list:
    ```bash
    $ sudo apt-get update
    ```
2.  Install GTKWave using `apt`:
    ```bash
    $ sudo apt install gtkwave
    ```

**Verification:**
The tool was verified by checking its version with `gtkwave -v`.

<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/dc9ce83c-f469-459a-817a-5d4797ca1c9c" />

-----
### Conclusion 🎉

Successfully setting up the VLSI toolchain on a virtual machine is the crucial first step in any digital design project. By following these documented steps, we have established a complete and verified open-source environment using **Yosys**, **Icarus Verilog**, and **GTKWave**.


