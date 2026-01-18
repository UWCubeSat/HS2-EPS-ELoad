# HS2 EPS Electronic Load (E-Load)

This repository contains software for controlling a **KEL103 Electronic Load** as part of the **HuskySat-2 Electrical Power System (EPS) Electrical Ground Support Equipment (EGSE)**.

The goal of this project is to enable **programmable battery discharge testing** and **data collection** to support EPS battery testing.

---

## Project Goals

- Programmatically control a **KEL103 electronic load**
- Execute time-based discharge schedules (e.g. CC or CP profiles)
- Collect and log battery data (voltage, current, power)
- Implement safety cutoffs for low-voltage conditions
- Generate CSV outputs
- Run on a **Raspberry Pi**

---

## Hardware Overview

- **Electronic Load:** KEL103  
- **Interface:** USB or RS-232  
- **Controller:** Raspberry Pi

---

## Software Overview

- **Language:** Python
- **Primary Library:** [`py-kelctl`](https://pypi.org/project/py-kelctl/)
- **Data Format:** CSV

The `py-kelctl` package provides a high-level Python interface to the KEL103, allowing control of:
- Constant Current (CC)
- Constant Power (CP)
- Load enable/disable
- Voltage, current, and power measurements

Using this library avoids implementing low-level serial commands from scratch.
