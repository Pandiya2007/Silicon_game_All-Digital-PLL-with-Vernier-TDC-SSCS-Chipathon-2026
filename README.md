# ADPLL-TDC: All-Digital PLL with Vernier TDC

**Team:** Silicon Game  
**Track:** A — Foundation of Building Blocks  
**Program:** [SSCS Chipathon 2026](https://github.com/sscs-ose/sscs-chipathon-2026/issues/104)  
**PDK:** GF180MCU  

---

## Team Members

| Name | GitHub | Role |
|---|---|---|
| Pandiyarajan S | [@Pandiya2007](https://github.com/Pandiya2007) | Team Lead(Analog and Digital Design |
| Sankaranarayanan V |  [sankaranarayanan95](https://github.com/sankaranarayanan95)  | Analog Design & Ingtegration |
| Deepika R | [Deepika-analog](https://github.com/Deepika-analog)  | Analog Design |
| Padhmanethrri S | [padmanethrri](https://github.com/padhmanethrri) | Analog Design |
| Beer Mohammed Irfan Z |  [mdirfan](https://github.com/mdIrfan264) | Digital Design |
| Devansh Srivastava |@handle| Digital Design|

---

## Overview

A fully All-Digital Phase-Locked Loop (ADPLL) implemented on the GF180MCU open-source PDK. This design replaces the charge pump and analog loop filter entirely with a Vernier Time-to-Digital Converter (TDC) and a synthesizable Digital Loop Filter (DLF) in RTL, eliminating all passive components from the loop path.

---

## Target Specifications

| Parameter | Target |
|---|---|
| Output Frequency | 100 MHz – 800 MHz |
| TDC Resolution | ~20 ps (1 inverter delay) |
| Loop Filter | 2nd-order IIR, 16-bit fixed point |
| Divider Ratio | N = 8 to 1023 (SPI programmable) |
| Supply Voltage | 1.8V |
| Jitter Target | < 5 ps RMS |

---

## Key Novelties

- No passive components in the loop path
- Vernier delay-line TDC (~20 ps resolution)
- Fully synthesizable 2nd-order PI digital loop filter via LibreLane
- Runtime-programmable loop bandwidth via SPI register interface
- On-chip DCO calibration FSM (binary search, <64 cycles convergence)

---

## Repository Structure
## Key Novelties
- No passive components in the loop path
- Vernier delay-line TDC (~20 ps resolution)
- Fully synthesizable 2nd-order PI digital loop filter via LibreLane
- Runtime-programmable loop bandwidth via SPI register interface
- On-chip DCO calibration FSM (binary search, <64 cycles convergence)

---

## Repository Structure

| Folder | Contents |
|---|---|
| `src/` | RTL source files (TDC, DLF, DCO, divider, FSM) |
| `cocotb/` | cocotb testbenches |
| `librelane/` | Synthesis + PnR config |
| `ip/` | IP blocks |
| `scripts/` | Helper scripts |
| `docs/` | Proposal, reports, slides |

---

## Tool Stack

| Tool | Purpose |
|---|---|
| Xschem | Schematic (DCO) |
| Ngspice | Analog simulation |
| cocotb + Icarus | Digital simulation |
| LibreLane | Synthesis + PnR |
| Magic + KLayout | Layout & verification |
| GF180MCU PDK | Process design kit |

---

## Progress Tracker

- [ ] Fork repository and set up project structure
- [ ] TDC RTL design and simulation
- [ ] DCO schematic and characterization
- [ ] Digital loop filter RTL + testbench
- [ ] Multi-modulus divider + SPI interface
- [ ] Calibration FSM implementation
- [ ] Full-chip integration
- [ ] RTL simulation (cocotb)
- [ ] Synthesis via LibreLane
- [ ] Static Timing Analysis (STA)
- [ ] Layout (Magic + KLayout)
- [ ] DRC + LVS clean
- [ ] Post-layout simulation
- [ ] GDS II submission

---

## Links
- [Chipathon Issue #104](https://github.com/sscs-ose/sscs-chipathon-2026/issues/104)
- [Project Proposal](https://github.com/user-attachments/files/28599991/Silicon_Games.project.proposal.pdf)
- [wafer.space Template](https://github.com/wafer-space/gf180mcu-project-template)
