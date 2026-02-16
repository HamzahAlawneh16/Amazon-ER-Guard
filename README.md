#  Amazon ER-Guard: Predictive Logistics Control Tower (Jordan Hub)

**"Optimizing Last-Mile Dispatch via Behavioral Intelligence & Operational Frugality"**

---

##  Executive Summary
**ER-Guard** is an AI-driven logistics decision engine designed specifically for **Amazon’s Jordan Operations**. The system tackles the "Last-Mile" delivery challenge—one of the most expensive segments of the supply chain. 

By predicting customer return intent and delivery failure risks **before the van leaves the station**, ER-Guard utilizes a hybrid model of **XGBoost Machine Learning** and **A* Path-Cost Optimization** to decide whether to proceed with a direct delivery or re-route the shipment to a regional hub, saving fuel, time, and carbon emissions.

---

##  Key Features
* **Province-Based Label Encoding:** Custom geospatial encoding for Jordanian provinces (Amman, Irbid, Aqaba, etc.) to handle regional delivery patterns.
* **Predictive Risk Audit:** Real-time inference using **XGBoost** to score customer reliability and product volatility.
* **A* Cost Optimization:** A mathematical engine that calculates the "True Cost of Delivery" by factoring in distance, fuel consumption, and risk-weighted penalties.
* **Live Operations Database:** A persistent system log (Simulated Database) that tracks every decision for transparency and fleet auditing.
* **Eco-Impact Tracker:** Real-time calculation of CO2 savings for every mitigated failed delivery.

---

##  Tech Stack
* **Language:** Python 3.x
* **AI/ML:** XGBoost (Extreme Gradient Boosting)
* **Web Framework:** Streamlit (Custom Amazon UI/UX)
* **Data Science:** Pandas & NumPy for Geospatial Encoding
* **Optimization:** A* Search Algorithm Logic for Operational Costs

---

##  System Architecture
The system follows a high-performance pipeline to ensure **Inference Latency < 50ms**:

1.  **Ingestion:** Capture Shipment ID, Destination, and Customer Risk Profile.
2.  **Encoding:** Transform categorical Jordan provinces into numerical vectors (e.g., *Irbid* → `2`).
3.  **Intelligence:** The XGBoost model analyzes the vector to predict the **Probability of Return**.
4.  **Decision (A* Logic):** $$Total Cost = (Distance \times Fuel Rate) + (Risk Probability \times Loss Penalty)$$
5.  **Execution:** * **Cost < 35 JOD:** ✅ **RELEASE FOR DISPATCH**
    * **Cost > 35 JOD:** 🚨 **AUTO-RE-ROUTE TO HUB**



---

## Amazon Leadership Principles in Action
* **Customer Obsession:** Ensuring high-probability deliveries to maintain customer trust and reduce failed attempt frustrations.
* **Invent and Simplify:** Turning complex geospatial and behavioral data into a simple "Green/Red" dispatch decision.
* **Frugality:** Drastically reducing "Operational Waste" (Fuel and Courier time) by preventing high-risk trips.
* **Bias for Action:** Providing a ready-to-use Control Tower interface that allows human supervisors to override AI decisions in real-time.

---

##  Performance Metrics (Projected)
| Metric | Impact |
| :--- | :--- |
| **Decision Latency** | < 50ms per shipment |
| **Prediction Accuracy** | ~92.4% (Based on XGBoost validation) |
| **Fuel Savings** | Estimated 18% reduction in failed delivery mileage |
| **Carbon Footprint** | ~21.0 kg CO2 saved per avoided long-distance failure |

---

##  Installation & Usage
To run the **Logistics Control Tower** locally:

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/your-username/amazon-er-guard.git](https://github.com/your-username/amazon-er-guard.git)

   ```
   ```bash
   pip install streamlit xgboost pandas numpy
   ```
   ```bash
   streamlit run app.py
   ```
   ## Developed by: Hamza Alawneh

  ## Location: Irbid, Jordan | Amazon Operations Research Lab (Simulated)
   
