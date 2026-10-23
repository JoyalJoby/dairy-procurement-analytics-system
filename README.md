# 🥛 Dairy Procurement & Quality-Yield Analytics Suite
**Commercial Operations, Supply Chain Re-Engineering & Pricing Analytics Case Study**

[![Power BI](https://img.shields.io/badge/Power%20BI-Desktop-yellow.svg)](https://powerbi.microsoft.com/)
[![DAX](https://img.shields.io/badge/DAX-Advanced%20Measures-orange.svg)]()
[![Process](https://img.shields.io/badge/BPMN%202.0-Supply%20Chain%20Optimization-blue.svg)]()
[![Volume](https://img.shields.io/badge/Procured%20Volume-39.5K%20L-green.svg)]()

---

## 📌 Executive Summary
An operational People & Supply Chain Analytics project evaluating 814 days of commercial dairy cooperative batch collection data ($39,496.0\text{ Litres}$, ₹$1,717,296.48\text{ total revenue}$).

### Key Business Challenges Addressed:
1. **Supply Scaling:** Tracked herd capacity expansion from a baseline of $14\text{ L/day}$ to peak daily output exceeding $83\text{ L/day}$ (a **5.5× scale-up**).
2. **Quality Arbitrage Discovery:** Uncovered a structural butterfat asymmetry between morning and evening milking cycles, where evening batches produce **$+0.54\%$ higher FAT**, unlocking a **+₹1.85 to +₹2.02/L pricing premium**.
3. **Logistics Re-engineering:** Identified dispatch inefficiencies that allowed the operation to consolidate transport routes, cutting operational overhead by **~18%**.

---

## 🖥️ Executive Power BI Dashboards

### 1. Executive Operations Overview
High-level volume trajectory, revenue KPIs, and morning vs. evening batch split ($63.9\%\text{ AM} / 36.1\%\text{ PM}$).
<img width="1798" height="1008" alt="01_executive_overview png" src="https://github.com/user-attachments/assets/3bcb09cc-30b6-4a65-b21e-203119c6a2c6" />



### 2. Quality-Yield Arbitrage & What-If Pricing Model
Empirical comparison of AM vs. PM butterfat percentages across every month, supported by a dynamic What-If simulation slider modeling price adjustment elasticity.
<img width="1791" height="1023" alt="02_quality_pricing png" src="https://github.com/user-attachments/assets/374dec27-36e8-46e2-a958-70edb6c651d5" />



---

## 🔄 Supply Chain Process Re-engineering (BPMN 2.0)
To eliminate duplicate vehicle runs and capture the evening butterfat premium before ambient temperature spoilage, delivery operations were re-engineered from fragmented dual dispatches into a consolidated cold-chain delivery model:

```mermaid
graph TD
    subgraph AS_IS["AS-IS Workflow: Fragmented Procurement (High Overhead)"]
        A1[Daily Milking AM & PM] --> A2[Manual Lactometer & Gerber Test]
        A2 --> A3[Handwritten Society Slip]
        A3 --> A4[Dispatched in 2 Separate Vehicle Runs]
        A4 --> A5[Society Manual Entry & Queuing]
        A5 --> A6[Discrepancies Discovered 15 Days Later at Payout]
        A6 --> A7[Outcome: 18% Excess Logistics Cost + Margin Leakage]
    end

    subgraph TO_BE["TO-BE Workflow: Quality Arbitrage & Route Optimization"]
        B1[Daily Milking AM & PM] --> B2[Digital Analyzer Batch Scan CLR / FAT / SNF]
        B2 --> B3[Batch Data Synced to Analytics Engine]
        B3 --> B4{Shift Routing Logic}
        B4 -->|AM Batch 64% Volume| B5[On-Farm Chiller Hold]
        B4 -->|PM Batch 36% Volume - High FAT| B6[Consolidated Single-Trip Evening Dispatch]
        B5 --> B6
        B6 --> B7[Automated Cooperative Society Handover via QR Code]
        B7 --> B8[Real-Time Daily Yield Dashboard & Instant Settlement]
        B8 --> B9[Outcome: 18% Overhead Cut + Payout Rate Maximized]
    end

    style AS_IS fill:#ffe6e6,stroke:#ff4d4d,stroke-width:2px;
    style TO_BE fill:#e6f2ff,stroke:#2b7fff,stroke-width:2px;
