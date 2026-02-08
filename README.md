# 🚀 VSD RISC-V FPGA Labs

> **Learn to Think Like a Chip**  
> *Bringing RISC-V to the VSD Classroom*

---

## 📌 Overview

This repository showcases a complete **RISC-V development workflow** using **GitHub Codespaces**, the **RISC-V GNU toolchain**, and the **Spike simulator**.  
It is part of the **VSD RISC-V / FPGA IP Development Labs**, covering environment setup, program execution, and firmware generation for FPGA integration.

---

## 🛠️ Development Environment

The entire setup is hosted on **GitHub Codespaces**, enabling a cloud-based Linux development environment with zero local installation.

### 🔧 Tools & Technologies
- GitHub Codespaces
- RISC-V GNU Toolchain (`riscv64-unknown-elf-gcc`)
- Spike RISC-V ISA Simulator
- Proxy Kernel (`pk`)
- Visual Studio Code (Web)

---

## 🧪 RISC-V Program Execution

A sample C program is used to compute the **sum of numbers from 1 to N**, validating both native and RISC-V execution flows.

### ▶️ Execution Flow
- Compile and run on host system
- Cross-compile for RISC-V
- Execute on Spike simulator

Commands used:
gcc sum1ton.c  
./a.out  

riscv64-unknown-elf-gcc -o sum1ton.o sum1ton.c  
spike pk sum1ton.o  

---

## 🧠 Firmware Build & BRAM HEX Generation

The **Basic RISC-V core firmware** is compiled to generate a **BRAM-compatible HEX file**, which can be directly used for FPGA memory initialization.

Steps followed:
cd vsdfpga_labs/basicRISCv/Firmware  
make riscv_logo.bram.hex  

Generated outputs:
- riscv_logo.bram.elf  
- riscv_logo.bram.hex  

---

## ☁️ GitHub Codespaces Workflow

- Launch Codespaces from GitHub dashboard
- Open repository in VS Code (Web)
- Build and run RISC-V programs via terminal
- Verify successful execution and firmware generation

---

## 🖼️ Screenshots

The following screenshots are included to document the workflow:
- GitHub Codespaces dashboard
  <img width="1920" height="1080" alt="Screenshot 2025-12-19 124100" src="https://github.com/user-attachments/assets/ea475d63-c496-404b-93b7-00ed2a00391c" />

- RISC-V build and execution flow
  
- Spike simulator output
- BRAM HEX file generation
- VSD RISC-V welcome banner

---

## ✅ Conclusion

This project demonstrates a **complete end-to-end RISC-V development pipeline**, from cloud-based environment setup to FPGA-ready firmware generation, using industry-standard open-source tools.


