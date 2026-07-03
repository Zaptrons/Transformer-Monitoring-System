# Transformer Monitoring System

## Generation 2 Architecture

---

# Vision

The goal of Generation 2 is to transform the project from a software simulation into the software architecture of a real embedded transformer monitoring device.

The software should be designed so that simulation components can later be replaced by real hardware without changing the overall architecture.

---

# Design Philosophy

Generation 2 follows a simple rule:

> Each class has one responsibility.

No class should perform work outside of its own responsibility.

---

# System Architecture

```text
                     Core
                       │
        ┌──────────────┼──────────────┐
        │              │              │
   TimeEngine     Measurement     ReportManager
        │              │
        │      ┌───────┴────────┐
        │      │                │
        │ CurrentSensor   VoltageSensor
        │      │                │
        └──────┴────────┬───────┘
                        │
                     Feeders
                        │
                   Transformer
                        │
                     Analyzer
```

---

# Class Responsibilities

## Core

System coordinator.

Responsibilities:

* Controls execution flow
* Requests measurements
* Calls analyzer
* Stores reports
* Coordinates system components

Core never performs engineering calculations.

---

## TimeEngine

Provides system time.

Responsible for:

* Clock
* Calendar
* Time progression

No engineering calculations.

---

## Measurement

Collects raw measurements.

Responsible for:

* Reading current sensors
* Reading voltage sensors
* Returning measurement data

No analysis is performed here.

---

## Analyzer

Engineering calculation engine.

Responsible for:

* Transformer loading
* Load percentage
* Phase balance
* Voltage evaluation
* Future diagnostic algorithms

Analyzer contains all engineering logic.

---

## Transformer

Represents the physical transformer.

Responsible only for:

* Rated power
* Rated voltage
* Rated current
* Physical properties

Transformer does not perform calculations.

---

## Feeder

Represents one outgoing feeder.

Stores:

* Feeder ID
* Three-phase voltage
* Three-phase current
* Feeder status

---

## Sensors

Represent measurement devices.

CurrentSensor

* Reads feeder current

VoltageSensor

* Reads feeder voltage

Sensors never analyze data.

---

## ReportManager

Responsible for:

* Recording system data
* Exporting reports
* Historical logging

---

# Design Rules

1. One class = One responsibility.

2. Core coordinates only.

3. Sensors measure only.

4. Analyzer calculates only.

5. Transformer represents hardware only.

6. Reports never perform calculations.

---

# Future Expansion

Generation 2 has been designed to allow future integration of:

* STM32
* ESP32
* Real Current Sensors
* Real Voltage Sensors
* RTC
* SD Card
* Ethernet / WiFi
* Cloud Monitoring

without redesigning the software architecture.

---

# Project Status

Current Development Stage

Generation 2

Architecture Design
