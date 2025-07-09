# Dynamic Pricing for Urban Parking Lots

**Capstone Project - Summer Analytics 2025**  
**Hosted by:** Consulting & Analytics Club × Pathway  
**Author:** Sanghita Roy  

##📌 Overview

Urban parking is a limited and fluctuating resource. Traditional static pricing leads to inefficiencies: overcrowding during peak demand and underutilization during off-peak hours. This project simulates a **real-time dynamic pricing system** for **14 urban parking spaces**, updating prices based on:

- Historical occupancy patterns
- Traffic congestion levels
- Queue lengths
- Special events and holidays
- Vehicle types
- Proximity to competitor lots

We build and visualize dynamic models that continuously update parking prices using **only Python, Numpy, Pandas, and Pathway**, complying with real-time streaming and pricing constraints.

---

## 🛠️ Tech Stack

| Layer            | Technology Used                         |
|------------------|------------------------------------------|
| Language         | Python                               |
| Data Processing  | Pandas, Numpy                            |
| Real-Time Engine | [Pathway](https://pathway.com)           |
| Visualization    | [Bokeh](https://docs.bokeh.org/), Panel  |
| Modeling         | Pure Python (no external ML frameworks)  |
| IDE              | Google Colab                             |
| Data             | `dataset.csv` (14 locations × 73 days × 18 time points/day) |

---

## 🧠 Architecture Diagram

```mermaid
flowchart TD
    A[Raw Dataset (CSV)] --> B[Data Preprocessing]
    B --> C[Feature Engineering]
    C --> D[Real-Time Streaming with Pathway]
    D --> E[Windowed Aggregation (per day)]
    E --> F[UDF compute_price()]
    F --> G[Real-Time Dynamic Pricing Output]
    G --> H[Bokeh Live Visualization]
    G --> I[Optional Rerouting Suggestions]

