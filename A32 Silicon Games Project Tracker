# A32 Silicon Games — ADPLL Project Tracker

## 1. Specification & Idea Decision

| Task | Target / Completion Date | Ownership | Status | Comments |
|---|---|---|---|---|
| Finalize ADPLL Architecture (200MHz out, 10MHz ref, /20 divider) | - | Team | ✅ Completed | Low Power All Digital PLL with Vernier TDC |
| GF180MCU PDK & Tool Flow Finalized (Xschem + Ngspice, Docker) | - | Team | ✅ Completed | iic-osic-tools container |
| Block-Level Spec Finalized (TDC, DCO, DLF, Divider, BIAS/LDO) | - | Team | ✅ Completed | Pin counts, resolution, freq targets defined |

## 2. Block-Level Schematic Design & Simulation

| Task | Target / Completion Date | Ownership | Status | Comments |
|---|---|---|---|---|
| Vernier TDC — Unit Cell (inv_fast, INV_SLW, D_FlipFlop) | - | Pandiyarajan | ✅ Completed | 20ps resolution verified |
| Vernier TDC — 5-Stage Chain | - | Pandiyarajan | ✅ Completed | Full swing 0-3.3V confirmed |
| Vernier TDC — 100-Stage Chain | - | Pandiyarajan | ✅ Completed | Thermometer code range verified |
| DCO — Ring Oscillator + Cap Bank | - | Teammate | ✅ Completed | Needs tuning from ~528-950MHz down to 180-220MHz |
| Digital Loop Filter (RTL, PI Controller) | - | Teammate | ✅ Completed | Verified in RTL sim — lock_now/locked waveforms confirmed |
| Frequency Divider (20-stage DFF chain) | - | Teammate | ✅ Completed | Divides 200MHz → 10MHz |
| BIAS & LDO (Bandgap + PMOS Pass Transistor) | - | Teammate | ✅ Completed | 1.8V regulated from 3.3V, ~5µA bias |

## 3. Top-Level Integration & Simulation

| Task | Target / Completion Date | Ownership | Status | Comments |
|---|---|---|---|---|
| Top-Level Schematic Assembly (all 5 blocks placed) | - | Pandiyarajan | ✅ Completed | adpll_top.sch |
| DLF Behavioral Placeholder for SPICE Co-sim | - | Pandiyarajan | ✅ Completed | EDLF-based analog stand-in for RTL-verified DLF |
| Bit-Width Bridging (TDC↔DLF↔DCO pin mapping) | TBD | Pandiyarajan & Teammate | 🟡 In Progress | Resolving 1-bit vs 8-bit interface mismatch |
| Open-Loop Top-Level Simulation (no feedback closure) | TBD | Pandiyarajan | ⏳ Pending | Verify signal propagation stage by stage |
| Closed-Loop Top-Level Simulation (full feedback) | TBD | Pandiyarajan | ⏳ Pending | Verify frequency convergence toward 200MHz/10MHz |

## 4. Physical Design (Layout)

| Task | Target / Completion Date | Ownership | Status | Comments |
|---|---|---|---|---|
| Layout Milestone Deadline | ~2 weeks from now | Team | ⏳ Pending | Top-level sim must pass first |
| Vernier TDC Layout | TBD | Pandiyarajan | ⏳ Pending | - |
| DCO Layout | TBD | Teammate | ⏳ Pending | - |
| DLF Layout (Digital/Synthesized) | TBD | Teammate | ⏳ Pending | - |
| Divider Layout | TBD | Teammate | ⏳ Pending | - |
| BIAS & LDO Layout | TBD | Teammate | ⏳ Pending | - |
| Chip-Level DRC & LVS Check | TBD | Team | ⏳ Pending | - |

## 5. Documentation & Presentations

| Task | Target / Completion Date | Ownership | Status | Comments |
|---|---|---|---|---|
| ADPLL System Overview Poster (Vernier TDC section) | - | Pandiyarajan | ✅ Completed | Introduction, Why Vernier TDC, Architecture, Sim Results |
| BIAS/LDO Poster Section | - | Pandiyarajan | ✅ Completed | 3-point summary added |
| Top-Level Integration Writeup | TBD | Pandiyarajan | ⏳ Pending | To follow after top-level sim results |
| Layout Review Documentation | TBD | Team | ⏳ Pending | - |
