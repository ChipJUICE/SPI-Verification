# SPI Protocol Verification using SystemVerilog Assertions & Functional Coverage

This repository contains a **SystemVerilog-based verification
environment** for the **Serial Peripheral Interface (SPI)** protocol.\
The project focuses on **assertion-based verification (ABV)** and
**functional coverage**, ensuring protocol compliance, timing
correctness, and complete stimulus space exploration.

------------------------------------------------------------------------

## 🔍 Overview

The goal of this project is to verify an SPI design using:

-   **SystemVerilog Assertions (SVA)**\
    To continuously check protocol behavior, detect violations, and
    validate timing sequences.

-   **Functional Coverage**\
    To measure verification completeness and ensure all SPI modes, data
    patterns, and protocol scenarios are exercised.

The verification environment is **self-checking**, lightweight, and
suitable for learning ABV concepts as well as protocol verification.

------------------------------------------------------------------------

## 📁 Repository Structure

    ├── design.sv          # SPI DUT (Design Under Test)
    ├── verification.sv    # Complete testbench with SVA + coverage
    ├── README.md

------------------------------------------------------------------------

## 🧩 Verified SPI Features

### ✔ Protocol Checks (via Assertions)

-   Correct relationship between **SCLK**, **MOSI**, **MISO**, and
    **SS_n**
-   CPOL/CPHA timing alignment
-   SS_n active-low behavior
-   Data stability on sampling edges
-   No data toggling when SS_n is high
-   Proper clock transitions per SPI mode

### ✔ Functional Coverage

-   All **four SPI modes** (Mode 0--3)
-   Transmit and receive data pattern coverage
-   Edge-case patterns (0x00, 0xFF, alternating bits, random)
-   Cross-coverage of CPOL × CPHA
-   Frame length coverage (if applicable)

------------------------------------------------------------------------

## 🎓 Learning Outcomes

-   Assertion-Based Verification (ABV)
-   SystemVerilog temporal properties
-   Functional coverage development
-   Protocol verification methodology
-   Building reusable verification code
