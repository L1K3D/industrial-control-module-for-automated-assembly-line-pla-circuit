# ⚙️ Industrial Control Module for Automated Assembly Line

This project was developed by a team specialized in industrial control systems to meet the requirements of a major automotive client. It implements a logic control module for an automated assembly line using a **Programmable Logic Array (PLA)**, ensuring precise coordination of machine states based on sensor inputs. The system is designed to operate reliably, safely, and efficiently throughout the production cycle.

## 📌 Project Overview

The control module interprets five digital sensor inputs and generates seven actuator control signals. These outputs are derived from a set of Boolean expressions and a comprehensive truth table, implemented via a PLA embedded in a ROM circuit. The logic was modeled and validated using **Logisim**, a digital circuit simulation environment.

### 🔍 Sensor Inputs

| Sensor | Description |
|--------|-------------|
| S4     | Raw material detection at the start of the line |
| S3     | Presence of part at stage 1 |
| S2     | Correct positioning of the part at stage 2 |
| S1     | End-of-stroke signal from the robotic arm |
| S0     | Critical temperature detection at the welding station |

### 🚦 Actuator Outputs

| Output | Function |
|--------|----------|
| A0     | Activates conveyor belt when raw material is detected |
| A1     | Triggers robotic arm for structural assembly |
| A2     | Activates alarm if part is misaligned after robotic movement |
| A3     | Initiates welding process when positioning and arm stroke are confirmed |
| A4     | Activates cooling system if post-welding temperature exceeds safe limits |
| A5     | Triggers thermal alarm if temperature reaches critical threshold |
| A6     | Signals successful task completion and readiness for next cycle |

## 🧠 Logic Implementation

- **Truth Table**: Exhaustively defines all valid input combinations and corresponding outputs
- **Boolean Expressions**: Derived and optimized for each output signal
- **PLA Matrix**: Constructed and simulated in Logisim to validate logic and timing

## 🛠 Technologies Used

- [Logisim](http://www.cburch.com/logisim/) — Digital circuit simulation
- PLA — Programmable Logic Array
- ROM — Embedded memory for output logic

## 📁 Repository Structure

├── docs/               # Technical documentation and circuit diagrams ├── logisim/            # Logisim project files (.circ) ├── src/                # Boolean expressions and truth tables ├── README.md           # Project overview and documentation


## ✅ Results

- Accurate synchronization of production stages
- Deterministic response to sensor conditions
- Reliable actuator control with minimal latency
- Scalable and maintainable logic architecture

## 📄 Conclusion

This project demonstrates the effective use of a PLA to implement a robust control system for industrial automation. The logic design ensures safe and efficient operation of the assembly line, minimizing errors and optimizing workflow. The modular structure and simulation-driven development process provide a solid foundation for future enhancements and integration into broader control architectures.

## 📬 Contact

Developed by **Heitor**  
📍 Diadema, São Paulo — Brazil  
📧 [heitor.santos.ferreira231203@gmail.com]

---

> This repository is part of an applied study in digital control systems for industrial automation. Contributions and adaptations for other use cases are welcome.
