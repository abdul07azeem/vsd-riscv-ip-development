# vsd-riscv-ip-development

# 🚀 Task-1: Environment Setup & RISC-V Reference Bring-Up

## 📌 Overview

This repository documents the successful completion of **Task-1: Environment Setup & RISC-V Reference Bring-Up** as part of the VSD Internship program.

The objective of this task was to establish a stable development baseline, validate the RISC-V reference execution flow, and prepare for upcoming FPGA and IP development work.

This phase focuses on:

* Toolchain readiness
* Understanding RISC-V execution flow
* Multi-repository workflow management
* System-level awareness before hardware integration

This is **not yet an FPGA programming task**. It is a foundation-building exercise aligned with real semiconductor industry onboarding practices.

---

## 🧠 Task Objectives

✔ Set up official GitHub Codespace environment
✔ Build and run RISC-V reference design
✔ Clone and validate VSDFPGA labs
✔ Understand system architecture and execution flow
✔ Prepare for future FPGA and IP integration tasks

---

## 🛠 Environment Used

* GitHub Codespaces (Primary environment)
* VS Code
* GNU Make
* RISC-V GCC Toolchain
* Linux build environment

Reference repository:

* `vsd-riscv2`
* `vsdfpga_labs`

---

## 🔄 Execution Flow Validated

### Step 1 —  Github Codespace Setup

* Forked the official `vsd-riscv2` repository
* Launched GitHub Codespace from fork in VS Code Desktop Environment
* Verified the setup using the commands

<pre>riscv64-unknown-elf-gcc --version
spike --version
iverilog -V </pre>
![Screenshot for verification](https://github.com/abdul07azeem/vsd-riscv-ip-development/blob/84c699795e6dd21253bf277039282b4d9cd1fe07/images/Setup_verification.png)
* The codespace is build without successfully any errors and issues.
* This ensured a known-good, reproducible development baseline.

---

### Step 2 — RISC-V Reference Bring-Up

* Followed repository README instructions
* Compiled provided RISC-V firmware using command
  <pre>riscv64-unknown-elf-gcc -o sum1ton.o sum1ton.c</pre>
*  Run it with spike:
   <pre>spike pk sum1ton.o</pre>
* Executed the program successfully
* Verified console output on VS code
  ![](https://github.com/abdul07azeem/vsd-riscv-ip-development/blob/7831ba60aa18831c3334bf2bd738116990f8796f/images/RISCV_reference_program.png)
  
  ## Exploring GUI Desktop(noVNC)
  ### Navigate the sample programs
  <pre>cd /workspaces/vsd-riscv2
  cd samples
  ls -ltr</pre>
  ### Compiled and executed the same program USing Native GCC(x86)
  <pre>gcc sum1ton.c
   ./a.out</pre>
   ### Compile and Run using RISC-V GCC and Spike
  <pre>riscv64-unknown-elf-gcc -o sum1ton.o sum1ton.c
  spike pk sum1ton.o</pre>
![](https://github.com/abdul07azeem/vsd-riscv-ip-development/blob/7831ba60aa18831c3334bf2bd738116990f8796f/images/riscv_refernce_program_novnc.png)

### In the image below the value of n is changed to 14 and executed to verify:
![](https://github.com/abdul07azeem/vsd-riscv-ip-development/blob/7831ba60aa18831c3334bf2bd738116990f8796f/images/riscv_refernce_program_novnc1.png)

This confirmed:

* Working toolchain
* Correct compilation flow
* Proper runtime behavior
---

### Step 3 — VSDFPGA Labs Integration

* Cloned `vsdfpga_labs` inside same Codespace
* Built basic labs not requiring FPGA hardware
* Verified successful execution via logs/simulation

This validated:

* Multi-repository workflow
* Cross-project integration readiness
* Preparation for SoC-level development

---

## 🏗 System Understanding

During this task, the following architectural concepts were analyzed:

* Location of RISC-V firmware in repository
* Compilation and linking flow
* Memory loading process
* Memory-mapped IO interaction
* Logical integration point for new FPGA IP blocks

This ensures readiness for future RTL/IP integration tasks.

---

## 🎯 Key Learning Outcomes

* Industry-style environment onboarding
* Toolchain validation before modification
* Understanding before implementation
* Structured system-level debugging
* Controlled, reproducible development workflow

---

## 🧪 Optional Validation Performed

* Modified firmware constant/message
* Rebuilt and re-executed program
* Observed correct behavioral change

This confirmed full control over the build and execution pipeline.

---

## 📌 Environment Confirmation

✔ GitHub Codespace used for execution
✔ Local environment preparation initiated (Dockerfile reviewed for tool requirements)

---

Successful completion confirms readiness for upcoming:

* RTL modifications
* Custom IP integration
* FPGA bring-up tasks
* SoC-level development

Tell me what style you want 🚀
