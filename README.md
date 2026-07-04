> 📦 Archived Repository
>
> This repository represents **Generation 1** of the research.
>
> Active development has moved to **Generation 2 (Local Grid Optimizer - LGO)**.

# Transformer Simulation System

A modular Python framework for distribution transformer simulation.

---

# Overview

This project was developed as the first research prototype for modeling the behaviour of distribution transformers using a clean and modular software architecture.

The system combines:

- Ambient temperature
- Load profile
- Transformer operating state
- Time progression
- Daily reporting

Beyond the electrical simulation itself, the primary objective of this repository was to establish a scalable software architecture suitable for future Embedded and Digital Twin projects.

---

# Current Features

- Hourly simulation engine
- Modular time management

  - Clock
  - Calendar
  - TimeEngine

- Temperature sensor simulation
- Load sensor simulation
- Transformer operating state calculation
- Daily report generation
- Dependency Injection architecture
- Clean separation of responsibilities

---

# Project Architecture

```text
Simulation
│
├── TimeEngine
│     ├── Clock
│     └── Calendar
│
├── TemperatureSensor
├── LoadSensor
├── Transformer
└── DailyReport
```

---

# Example Output

```python
{
    "Record Number": 125,
    "Hour": 14,
    "Day": 6,
    "Month": 3,
    "Year": 0,
    "Season": "Spring",

    "Ambient Temperature": 31.4,
    "Current Load": 482.3,
    "Load Percentage": 76.2,
    "Oil Temperature": 68.7
}
```

---

# Project Status

## Generation 1 — Completed

This repository has completed its research objectives.

Generation 1 successfully validated:

- Clean Architecture
- Dependency Injection
- Modular simulation design
- Digital Twin software concepts

During field research and discussions with power distribution engineers, a new engineering challenge was identified that offers greater practical value.

For this reason, Generation 1 has been archived.

The knowledge gained from this repository now serves as the technical foundation for **Generation 2**.

---

# Lessons Learned

The most important lesson from this project was:

> Building a professional solution is valuable only after identifying the correct engineering problem.

Generation 1 provided the software architecture and engineering experience required to begin a more realistic research direction.

---

# Future Direction

Research continues under a new project:

## Local Grid Optimizer (LGO)

Generation 2 focuses on:

- Local Grid Optimization
- Intelligent Phase Balancing
- Behaviour Learning
- Predictive Decision Engine
- Edge Intelligence
- Adaptive Algorithms

Unlike Generation 1, the new project originates from real operational challenges observed in low-voltage distribution networks.

---

# Technologies

- Python
- Object-Oriented Programming (OOP)
- Dependency Injection
- Clean Architecture
- Digital Twin Concepts

---

# Repository Status

✅ Archived

This repository will remain available as a historical reference and technical milestone.

No further feature development is planned.

---

# Author

**Hadi Norouzi**

Electrical Engineer | Embedded Systems | Software Architecture

GitHub

https://github.com/Zaptrons/Transformer-Simulation-System