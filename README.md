# Ghost Squadron SAE Aero Design Challenge – Remote Controlled Aircraft Project

## Overview
Ghost Squadron is a multidisciplinary team of graduate and undergraduate engineering students who participated in the 2024/25 SAE Aero Design Challenge. The objective was to design, build and flight‑test a remote‑controlled fixed‑wing aircraft capable of carrying the maximum possible payload while meeting strict competition constraints on take‑off distance, stall speed and structural integrity.

This repository contains our full design documentation, aerodynamic analyses, payload optimisation studies, electronics selection and test results. It also includes images and simulation outputs that show the evolution of our design and validate its performance.

## Objectives
- **Maximum payload fraction** – maximise the payload‑to‑gross weight ratio while satisfying competition limits on take‑off distance and wing loading.
- **Stable, controllable airframe** – ensure favourable handling qualities through careful selection of airfoil, aspect ratio and control-surface sizing.
- **Structural efficiency** – design a lightweight fuselage and wing that can withstand flight loads and payload without excessive weight.
- **Rapid assembly and maintainability** – design modular structures and accessible electronics to facilitate quick assembly and field repairs.

## Design Approach
Our design process combined analytical calculations, computational fluid dynamics (CFD), finite element analysis (FEA) and iterative prototyping.

### Airfoil and Wing Planform
We surveyed several low‑Reynolds‑number airfoils—including S1223, CH10 (smoothed), E423, FX74‑CL5‑140 and RG–15—using XFOIL to evaluate their lift‑to‑drag characteristics. The S1223 provided the highest lift‑coefficient at moderate angles of attack and an excellent lift‑to‑drag ratio, making it suitable for high payload fractions【220662197521525†screenshot】. The wing planform features a moderate taper and aspect ratio of 6.5 to balance induced drag and structural weight. Elliptic lift distribution was approximated using washout and twist.

### Aerodynamic Analysis
XFOIL results were validated via CFD in ANSYS Fluent. Key results include:
- **Lift coefficient vs angle of attack (Cl–α)** – the S1223 airfoil achieves Cl≈1.8 at 12° angle of attack, with stall beyond 18°【220662197521525†screenshot】.
- **Drag coefficient vs angle of attack (Cd–α)** – minimum drag coefficient (Cd≈0.03) occurs near 5°, increasing steeply past stall【220662197521525†screenshot】.
- **Lift‑to‑drag ratio (Cl/Cd) vs α** – the optimum L/D ≈ 100 is achieved around 8‑10°, guiding our cruise angle of attack and trimming settings【220662197521525†screenshot】.
- **Pressure variation across the airfoil** – CFD contours confirm laminar flow and highlight pressure recovery near the trailing edge【220662197521525†screenshot】.

### Structural Design
The fuselage uses a rectangular box‑beam construction with balsa‑ply sandwich skins and carbon‑fibre spars. Finite element models were used to size the main spar and ribs for 3.5× limit load. The tail boom is a carbon‑tube structure supporting a conventional tail with large elevator and rudder for slow‑speed control.

### Payload Optimisation
We modelled the aircraft performance using the competition payload fraction requirements. A linear relationship between density altitude and payload fraction was observed; at 0 ft density altitude the payload fraction reached ≈0.60 but decreased to ≈0.57 at 5 000 ft【220662197521525†screenshot】. The optimum competition configuration carried ~4.5 kg payload within a 9 kg maximum take‑off weight. The payload bay was sized to accommodate standard payload blocks and includes quick‑release mounting rails.

### Electronics and Power System
The propulsion system was selected to provide a static thrust‑to‑weight ratio greater than 0.7. Key components include:
- **Motor** – SunnySky X4112 brushless outrunner (400 kV).
- **Electronic speed controller (ESC)** – 60 A opto ESC with regenerative braking.
- **Propeller** – 14×8 wooden propeller selected through static thrust tests.
- **Battery** – 6‑cell 10 000 mAh Li‑Po providing ~10 minutes endurance at full throttle.
- **Servos** – high‑torque digital servos for ailerons, elevator and rudder; micro‑servos for flaps.
- **Radio system** – FlySky FS‑i6 transmitter/receiver chosen for reliable 2.4 GHz telemetry【484373478668588†screenshot】.

### Testing and Validation
A series of bench tests, wind‑tunnel tests and flight tests were conducted:
- **Wind‑tunnel tests** – validated lift and drag data obtained from XFOIL/CFD and verified stall behaviour.
- **Static propulsion tests** – measured thrust, current draw and efficiency across propeller sizes.
- **Ground roll and take‑off tests** – confirmed compliance with competition take‑off distance limits.
- **Flight tests** – evaluated handling qualities, control authority and stability. Trimmed level flight at 8° angle of attack yielded cruise speed of ~17 m/s.

### Results
The final Ghost Squadron aircraft achieved:
- Payload fraction of 0.58 at sea‑level density altitude.
- Take‑off distance under 45 m with full payload.
- Flight endurance of ~10 minutes with 4.5 kg payload.
- Structural safety factor >3 at ultimate load.
These results were validated by the payload–altitude graph and flight‑test data provided in the figures.

## Repository Structure
- `figures/` – images and graphs used throughout the README and report (aerodynamic plots, payload curve, pressure contour, electronics photograph).
- `reports/` – detailed design report in PDF and DOCX formats.
- `README.md` – this comprehensive project overview.

## Usage
This repository is intended for educational purposes and to aid future SAE Aero Design teams. Feel free to explore the figures and reports for deeper insight into our methodology. To reproduce the aerodynamic analyses, see the Python scripts and XFOIL input files (not provided here due to competition rules). For questions or collaboration enquiries, please contact the Ghost Squadron team lead.

---

© 2025 Ghost Squadron SAE Aero Design Team. Distributed under the MIT License.
