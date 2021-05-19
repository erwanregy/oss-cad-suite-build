# OSS CAD Suite

[![linux-x64](https://github.com/YosysHQ/oss-cad-suite-build/actions/workflows/linux-x64.yml/badge.svg)](https://github.com/YosysHQ/oss-cad-suite-build/releases/latest)
[![darwin-x64](https://github.com/YosysHQ/oss-cad-suite-build/actions/workflows/darwin-x64.yml/badge.svg)](https://github.com/YosysHQ/oss-cad-suite-build/releases/latest)
[![windows-x64](https://github.com/YosysHQ/oss-cad-suite-build/actions/workflows/windows-x64.yml/badge.svg)](https://github.com/YosysHQ/oss-cad-suite-build/releases/latest)

[![linux-arm](https://github.com/YosysHQ/oss-cad-suite-build/actions/workflows/linux-arm.yml/badge.svg)](https://github.com/YosysHQ/oss-cad-suite-build/releases/latest)
[![linux-arm64](https://github.com/YosysHQ/oss-cad-suite-build/actions/workflows/linux-arm64.yml/badge.svg)](https://github.com/YosysHQ/oss-cad-suite-build/releases/latest)
[![linux-riscv64](https://github.com/YosysHQ/oss-cad-suite-build/actions/workflows/linux-riscv64.yml/badge.svg)](https://github.com/YosysHQ/oss-cad-suite-build/releases/latest)

# Introduction

OSS CAD Suite is software distribution for number of [open source software](https://en.wikipedia.org/wiki/Open-source_software) used in digital logic design. 
You will find tools for RTL synthesis, formal hardware verification, place & route, FPGA programming, testing with support for HDL like Verilog, Migen and nMigen.

### RTL Synthesis 
 * [Yosys](https://github.com/YosysHQ/yosys) RTL synthesis with extensive Verilog 2005 support
 * [nMigen](https://github.com/nmigen/nmigen) refreshed Python toolbox for building complex digital hardware
 * [Migen](https://github.com/m-labs/migen) Python toolbox for building complex digital hardware
 
### Formal Tools
 * [SymbiYosys](https://github.com/YosysHQ/SymbiYosys) a front-end driver program for Yosys-based formal hardware verification flows.
 * [mcy](https://github.com/YosysHQ/mcy) Mutation Cover with Yosys
 * [sby-gui](https://github.com/YosysHQ/sby-gui) GUI for SymbiYosys
 * [avy](https://bitbucket.org/arieg/extavy) Interpolating Property Directed Reachability tool
 * [Boolector](https://github.com/Boolector/boolector) SMT solver
 * [Yices 2](https://github.com/SRI-CSL/yices2) a solver for Satisfiability Modulo Theories (SMT) problems
 * [Super prove](https://github.com/sterin/super-prove-build) SMT solver
 * [Pono](https://github.com/upscale-project/pono) an SMT-based model checker built on [smt-switch](https://github.com/makaimann/smt-switch)
 * [Z3](https://github.com/Z3Prover/z3) Theorem Prover

### PnR
 * [nextpnr](https://github.com/YosysHQ/nextpnr) a portable FPGA place and route tool (generic, ice40, ecp5, machxo2, nexus)
 * [Project IceStorm](https://github.com/cliffordwolf/icestorm) tools for working with Lattice ICE40 bitstreams
 * [Project Trellis](https://github.com/SymbiFlow/prjtrellis) tools for working with Lattice ECP5 bitstreams
 * [Project Oxide](https://github.com/gatecat/prjoxide) tools for working with Lattice Nexus bitstreams
 
### FPGA board programming tools
 * [openFPGALoader](https://github.com/trabucayre/openFPGALoader) universal utility for programming FPGA
 * [dfu-util](http://dfu-util.sourceforge.net/) Device Firmware Upgrade Utilities
 * [ecpprog](https://github.com/gregdavill/ecpprog) basic driver for FTDI based JTAG probes, to program ECP5 FPGAs
 * [ecpdap](https://github.com/adamgreig/ecpdap) program ECP5 FPGAs and attached SPI flash using CMSIS-DAP probes in JTAG mode
 * [fujprog](https://github.com/kost/fujprog) ULX2S / ULX3S JTAG programmer
 * [openocd](http://openocd.org/) Open On-Chip Debugger
 * [icesprog](https://github.com/wuxx/icesugar/tree/master/tools/src) iCESugar FPGA board programmer
 * [TinyFPGA](https://github.com/tinyfpga/TinyFPGA-Bootloader) USB Bootloader
 * [TinyFPGA-B](https://github.com/tinyfpga/TinyFPGA-B-Series) TinyFPGA B2 Board programmer
 * [iceFUN](https://github.com/pitrz/icefunprog) iceFUN Programmer
 
### Simulation/Testing
 * [GTK Wave](https://github.com/gtkwave/gtkwave) fully featured GTK+ based wave viewer
 * [verilator](https://github.com/verilator/verilator) Verilog/SystemVerilog simulator
 * [iverilog](https://github.com/steveicarus/iverilog) Verilog compilation system

### SoC
 * [LiteX](https://github.com/enjoy-digital/litex/) Migen/MiSoC based Core/SoC builder

### Support libraries
 * [Python 3](https://github.com/python/cpython) language interpretter is provided in all supported platforms.
 * [Python 2](https://github.com/python/cpython) language interpretter is provided in Linux platforms in form of library only.
 * [Ubuntu 20.04](https://ubuntu.com/) distribution development packages are used and shared libraries used are provided in package.
 * [macports](https://www.macports.org/) distribution system for macOS is used to obtain all libraries used, and they are provided in package.
 * [MinGW](https://sourceforge.net/projects/mingw) Minimalist GNU for Windows library packages from Fedora 32 are used in compilation and provided in package.
 
# Installation

1. Download an archive matching your OS from [the releases page](https://github.com/YosysHQ/oss-cad-suite-build/releases/latest).
2. Extract the archive to a location of your choice (for Windows it is recommended that path does not contain spaces)
3. To use OSS CAD Suite 

Linux and macOS
```
export PATH="<extracted_location>/oss-cad-suite/bin:$PATH"

or

source <extracted_location>/oss-cad-suite/environment
```
Windows
```
from existing shell:
<extracted_location>\oss-cad-suite\environment.bat

to create new shell window:
<extracted_location>\oss-cad-suite\start.bat
```

# Supported architectures

## linux-x64
Any personal Linux based computer should just work, no additional packages are needed to be installed on system to make OSS CAD Suite working.
Distributed libraries are based on Ubuntu 20.04, but everything is packaged in such a way so it can be used on any Linux distribution.

## darwin-x64
Any macOS 10.14 or later with Intel CPU should use this distribution package.

## windows-x64
This architecture is supported for Windows 10, but older 64-bit version of Windows 7, 8 or 8.1 should work. 

## linux-arm
ARM based Linux devices such as Raspberry Pi 3, 4 or 400 can use this distribution package.

## linux-arm64
ARM64 based Linux devices using 64bit CPU as in Raspberry Pi 4 and 400 (with 64bit version of OS installed), and also laptops as MNT Reform 2 can use this distribution package.

## linux-riscv64
RiscV-64 based Linux devices should use this distribtuion package, but please note that this is currently **untested**

# Contributing

To be able to build OSS CAD Suite yourself need to install `docker` and `python 3.6` or higher, with `click` library.


After that just running ```./builder.py``` should work fine.

To build default build:
```
./builder.py build 
```

To skip update of source code you can always:
```
./builder.py build --no-update
```

To build specific target and architecture:
```
./builder.py build --target=yosys --arch=linux-arm64
```

