# NIRF Ranking Analytics & Prediction: A Machine Learning Approach 🇮🇳

## Project Overview

This project presents a comprehensive machine learning framework designed to reverse-engineer, analyze, and predict the scores and overall ranks of Indian educational institutions under the **National Institutional Ranking Framework (NIRF)**. By focusing on critical, data-intensive parameters, this research provides granular insights into the factors driving institutional success and serves as a policy-level decision-making tool for strategic resource allocation.

The methodology involves deep deconstruction and predictive modeling of high-impact metrics within the NIRF framework, specifically:

* **FRU** (Financial Resources Utilization)
* **FPPP** (Footprint of Projects, Professional Practice, and Executive Development Programmes)
* **IPR** (Intellectual Property Rights and Patents)

---

## Key Features & Methodology

### 1. Advanced Predictive Modeling

* **Sub-Metric Regression**: Individual regression models (Linear & Polynomial) trained to predict FRU, FPPP, and IPR scores. These serve as checkpoints, validating score components against actual NIRF data.
* **Composite Rank Prediction**: A final model estimates the Overall NIRF Score and Rank using the five official pillars: Teaching, Learning & Resources (TLR), Research & Professional Practice (RPC), Graduation Outcomes (GO), Outreach & Inclusivity (OI), and Perception (PR).
* **Performance**: The composite model achieved an **R² score of 0.94** for Overall Rank Prediction.

### 2. Strategic Sensitivity & Policy Simulation

* **Financial Shock Testing**: FRU model simulates hypothetical reallocations of Budget Capital (BC) and Budget Operational (BO) with ±₹1 Cr and ±₹5 Cr increments.
* **Actionable Insights**: Visualize rank shifts under different budget scenarios, aiding university admins in optimizing investments.

### 3. Deep Parameter Deconstruction (FRU & FPPP)

* **FRU Analysis**: Institutions spend ~4x more on BO (salaries, maintenance) compared to BC (infrastructure).
* **FPPP Analysis**: Institutions with 100–300 faculty and balanced Research Funding (RF) & Consultancy Funding (CF) score higher.
* **Case Study (IIITD: IR-E-U-0105)**: Average FRU (15.69) but high FPPP (3.16), placing in the top 25% for productivity.

### 4. Data Quality and Transparency

* Identified **inconsistencies and reporting gaps** in public datasets, highlighting the need for stronger data integrity in national rankings.

---

## Model Performance Summary

| NIRF Component          | Model Type            | R² Score |
| ----------------------- | --------------------- | -------- |
| Overall Rank Prediction | Composite Regression  | **0.94** |
| FRU                     | Individual Regression | 0.92     |
| IPR                     | Individual Regression | 0.90     |
| FPPP                    | Individual Regression | 0.87     |

**Evaluation Metrics**: MSE & RMSE were used for accuracy validation.

---

## Repository Structure

```
📂 NIRF-Ranking-Analytics-and-Prediction
├── Rank_predictor.ipynb       # Composite Overall Rank Prediction model
├── NIRF_FRU.ipynb             # FRU analysis + sensitivity analysis plots
├── NIRF_FPPP.ipynb            # FPPP analysis + correlation matrix plots
├── NIRF_IP_report.pdf         # Final project report & recommendations
├── FRU_final.csv              # Cleaned FRU dataset (BC, BO, FRU scores)
├── FPPP_Data.csv              # Cleaned dataset for FPPP analysis
├── Data.xlsx - Sheet1.csv     # Consolidated NIRF scores (2021–2024)
```

---

## Associated Institution & Project Details

* **Associated with**: Indraprastha Institute of Information Technology, Delhi (IIITD)
* **Project Date**: Jan 2025 – Present

---

## How to Run the Project

### 1. Clone the Repository

```bash
git clone https://github.com/YourUsername/NIRF-Ranking-Analytics-and-Prediction.git
cd NIRF-Ranking-Analytics-and-Prediction
```

### 2. Install Dependencies

```bash
pip install pandas numpy scikit-learn matplotlib seaborn
```

### 3. Run Analysis

Open the Jupyter Notebooks (`.ipynb`) in sequence:

1. **NIRF_FRU.ipynb** → Financial Resources Utilization analysis
2. **NIRF_FPPP.ipynb** → Faculty productivity analysis
3. **Rank_predictor.ipynb** → Composite overall rank prediction

The `Rank_predictor.ipynb` includes a function:

```python
predict_score_rank(parameters)
```

that allows testing new parameter sets for instant NIRF score & rank predictions.

---

## License

License (feel free to use, modify, and share).

---

## Acknowledgements

Special thanks to **IIIT Delhi** and **Arani Bhattacharya** for institutional support and to the open-source Python ecosystem powering this research.
