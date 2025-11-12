# 🌦️ Microwatt IoT Weather Station (Digital IC Design Project)

> **Course Project:** Digital IC Design using Cadence Virtuoso  
> **Student:** Rick Raj Das  
> **Institution:** VIT Vellore — M.Tech (VLSI Design)  
> **Tools Used:** Cadence Virtuoso, Verilog HDL, Synopsys Design Compiler, Cadence Innovus, MATLAB  

---

## 🧠 Project Overview

This project presents the **design and simulation of a Microwatt-Powered IoT Weather Station** — an ultra-low-power **digital system-on-chip (SoC)** capable of collecting environmental data (temperature, humidity, and light intensity) using minimal energy resources.  

The entire system is implemented using **digital IC design principles** in **Cadence Virtuoso**, focusing on:
- Power optimization
- Area minimization
- Timing and performance trade-offs
- Standard-cell-based digital design methodology  

---

## ⚙️ System Architecture

The design consists of the following core modules:

| Module | Description |
|--------|--------------|
| **Sensor Interface Unit (SIU)** | Captures digital data from temperature, humidity, and light sensors |
| **Data Processing Unit (DPU)** | Performs averaging, scaling, and threshold comparison |
| **Control Logic** | Manages timing, enables power gating, and synchronizes modules |
| **Clock Divider** | Generates low-frequency clock from high-speed oscillator |
| **Power Management Unit (PMU)** | Handles power-down and wake-up operations |
| **UART Transmitter** | Transmits processed data to the IoT module |
| **IoT Node Interface** | Connects with an external transceiver (e.g., ESP8266) for cloud data upload |

---

## 🧩 Design Flow

The project follows a **complete ASIC design flow**:

1. **RTL Design:**  
   Verilog-based modeling of all modules (Sensor Interface, Controller, UART, etc.)

2. **Functional Simulation:**  
   Testbench development using Cadence SimVision to verify logic functionality.

3. **Synthesis:**  
   RTL-to-gate-level synthesis using **Synopsys Design Compiler**.

4. **Floorplanning & Placement:**  
   Layout design in **Cadence Innovus**.

5. **Power Optimization:**  
   Clock gating and low-Vt cell selection.

6. **Post-Layout Simulation:**  
   Timing and power verification using extracted parasitic netlists.

---

## 🔬 Key Features

- ✅ Ultra-low-power digital design (<1 μW active power)
- ✅ Compact layout optimized for 130nm process node
- ✅ Fully automated Verilog-based RTL flow
- ✅ Power gating and clock gating implemented
- ✅ Functional verification with file-based testbenches
- ✅ Compatible with IoT transceivers via UART

---

## 🧾 Specifications

| Parameter | Value |
|------------|--------|
| **Process Node** | 130 nm CMOS |
| **Operating Voltage** | 1.2 V |
| **Clock Frequency** | 50 MHz (base), divided down to 1 kHz |
| **Power Consumption** | < 1 µW (active), < 100 nW (sleep) |
| **Area** | ~0.04 mm² |
| **Technology** | Cadence Virtuoso & Synopsys DC Flow |

---

## 🧠 Simulation Results

- **Waveforms:** Verified functional correctness in all modules  
- **Post-layout Timing:** Zero timing violations at 1.2 V  
- **Power Report:** Leakage minimized through multi-threshold cell usage  

*(Add screenshots of simulation waveforms, layout, and timing reports here once available.)*

---

## 🗂️ Repository Structure

```bash
📦 Microwatt-IoT-Weather-Station
├── 📁 RTL_Code
│   ├── clk_divider.v
│   ├── controller.v
│   ├── uart_tx.v
│   ├── sensor_interface.v
│   └── top_module.v
├── 📁 Testbench
│   ├── tb_top.v
│   └── stimulus.txt
├── 📁 Reports
│   ├── synthesis_report.txt
│   ├── power_report.txt
│   └── timing_report.txt
├── 📁 Layout
│   ├── floorplan.png
│   ├── layout.png
│   └── DRC_LVS_reports/
├── 📁 Documentation
│   ├── project_report.pdf
│   └── presentation_slides.pptx
└── README.md
