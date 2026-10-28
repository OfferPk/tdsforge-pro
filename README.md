# TDSForge Pro (v1.0.0)

> **CCSDS 922.2-B-2 Cross Support Transfer Service (CSTS) Tracking Data Service (TD-CSTS) Studio**  
> Complete CSTS Specification Framework FSM (UNBOUND, READY, ACTIVE), Multi-Observable Radiometric Synthesizer (Two-Way Doppler, Range, Azimuth/Elevation Angles, Carrier Phase), Real-Time Streaming & Replay Buffer, and 10-Point Normative Aerospace Standards Auditor.

---

## 🛰️ Product Overview

TDSForge Pro is a specialized aerospace flight dynamics and tracking station software suite designed for deep-space mission navigators, ground tracking networks (NASA Deep Space Network \- DSN, ESA ESTRACK, KSAT, JAXA), and space situational awareness operators. It provides a software reference implementation and compliance auditing toolkit for the **CCSDS 922.2-B-2** (*Cross Support Transfer Service—Tracking Data Service*) and **CCSDS 921.1-B-2** (*Cross Support Transfer Service—Specification Framework*) standards.

### Key Capabilities

- **CSTS Framework 3-State FSM**: Implements the standardized CSTS procedure automaton (`UNBOUND`, `READY`, `ACTIVE`) with rigorous transition guards.  
- **Multi-Observable Radiometric Synthesis**: Generates high-fidelity Doppler carrier shifts, round-trip light time ranging, antenna pointing angles, and carrier phase telemetry.  
- **Microsecond Time-Tagging**: Formats standardized UTC/TAI timestamps for seamless integration into orbit determination filters (ODTK, GMAT, FreeFlyer).  
- **Physical Boundary Verification**: Enforces physical antenna angle limits (Azimuth 0..360°, Elevation \-5..90°) and signal quality thresholds (\$P\_c/N\_0\$ 20..80 dB-Hz).  
- **Real-Time Streaming & Offline Playback**: Simulates continuous tracking passes with buffered queuing and replay bounds.  
- **10-Point Normative Standards Auditor**: Enforces rules TDS-001 through TDS-010 to guarantee mission-readiness.  
- **Zero-Dependency Architecture**: Cross-platform pure ES6+ library, zero-dependency Python 3 CLI, and interactive HTML5 Mission Operations Console.

---

## 🚀 Quick Start

### 1\. Interactive Mission Operations Console

Open `source-code/index.html` in any web browser to step through the CSTS state machine, produce radiometric tracking observables, deliver them to navigators, and run compliance audits.

### 2\. Python Command Line Interface (CLI)

Run a full simulated CSTS TD-CSTS session lifecycle:

python3 source-code/tds\_cli.py session

Generate a standalone Doppler observable:

python3 source-code/tds\_cli.py generate \--type DOPPLER \--rate 12.45

Stream multi-observable radiometric telemetry:

python3 source-code/tds\_cli.py stream \--count 4

Execute the 10-Point Normative Standards Audit:

python3 source-code/tds\_cli.py audit

### 3\. Automated Test Suite

Run the 10 automated unit verification tests:

python3 source-code/test\_runner.py

---

## 📊 Compliance Matrix Summary

| Rule ID | Normative Checkpoint | Standard Reference | Status |
| :---: | :---- | :---- | :---: |
| **TDS-001** | CSTS Specification Framework Lifecycle | CCSDS 921.1 §3.2 & 922.2 §3.1 | **PASS** |
| **TDS-002** | Multi-Observable Tracking Data Format | CCSDS 922.2 §3.3 | **PASS** |
| **TDS-003** | High-Precision Timestamp Time-Tagging | CCSDS 922.2 §3.6.2 | **PASS** |
| **TDS-004** | Two-Way Doppler & Range-Rate Accounting | CCSDS 922.2 §3.6.3 | **PASS** |
| **TDS-005** | Ranging Measurement Ambiguity & Range Units | CCSDS 922.2 §3.6.4 | **PASS** |
| **TDS-006** | Topocentric Antenna Pointing Angles Geometry | CCSDS 922.2 §3.6.5 | **PASS** |
| **TDS-007** | Carrier Phase & Pc/N0 Quality Bounds | CCSDS 922.2 §3.6.6 | **PASS** |
| **TDS-008** | Real-Time & Offline Buffer Sizing | CCSDS 922.2 §3.6.7 | **PASS** |
| **TDS-009** | TDU Monotonic Sequence Tracking | CCSDS 922.2 §3.6.8 | **PASS** |
| **TDS-010** | CSTS Specification Framework Version Alignment | CCSDS 921.1 §1.3 | **PASS** |

---

## 💼 Commercial & Monetization Details

- **Target Customer**: Flight Dynamics Centers (NASA JPL, ESA ESOC, CNES), commercial ground station networks, orbit determination software vendors, and deep space navigation teams.  
- **Distribution Model**: Professional Developer Seat & Enterprise Ground Station Site License.  
- **Pricing**: \$349/year per developer seat or \$2,499 one-time enterprise site license.  
- **Zero Cloud Infrastructure**: Client-side and local CLI execution with zero external data transmission.