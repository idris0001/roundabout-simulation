# 🛣️ Roundabout Traffic Simulation Using SUMO

This project models a multi-entry roundabout using the **SUMO (Simulation of Urban Mobility)** framework. It simulates realistic traffic flows based on vehicle count data collected over a one-hour interval from four major entry points:

- **Barka**
- **Muscat**
- **Maabilah**
- **Bait Albarakah Palace**

Each origin is modeled across three distinct lanes:
- **Inner lane**: for left turns and U-turns
- **Middle lane**: for straight-through traffic
- **Outer lane**: for right turns and short exits

---

## 📦 Contents

- `roundabout.rou.xml`: Route definitions for all 12 modules
- `requirement.pdf`: Source document with vehicle counts and directions
- `tripinfo.xml` & `summary.xml`: SUMO-generated performance metrics
- `screenshots/`: Visual outputs from the simulation

---

## 🚗 Vehicle Types Simulated

- Passenger Cars (PC)
- Trucks
- Buses
- Recreational Vehicles (RV)

Each flow includes realistic parameters for acceleration, deceleration, length, and speed.

---

## 📊 Simulation Results

- **Trip Info**: Logs each vehicle’s journey, duration, and delay
- **Summary**: Aggregated metrics like average speed and waiting time

---

## 🖼️ Screenshots

Visual outputs showing vehicle flows across different lanes and origins.

---

## ✅ Status

All 12 modules are implemented and validated:
| Origin       | Inner Lane | Middle Lane | Outer Lane |
|--------------|------------|-------------|-------------|
| **Barka**     | ✅          | ✅           | ✅           |
| **Muscat**    | ✅          | ✅           | ✅           |
| **Maabilah**  | ✅          | ✅           | ✅           |
| **Palace**    | ✅          | ✅           | ✅           |

---

## 📚 How to Run

Use SUMO with the provided `.rou.xml` and `.net.xml` files:
```bash
sumo -n network.net.xml -r roundabout.rou.xml --tripinfo-output tripinfo.xml --summary-output summary.xml
