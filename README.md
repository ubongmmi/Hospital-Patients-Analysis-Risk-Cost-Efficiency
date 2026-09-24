# 🏥 Hospital Patients Analysis: Risk, Cost & Efficiency

**Prepared by:** Ubong Solomon

---

## 1. Introduction

Hospitals must balance clinical outcomes, patient satisfaction, and financial performance, all while managing risks such as readmission and extended length of stay. This project analyzes a hospital patient dataset through an interactive Power BI dashboard, converting raw admission, condition, procedure, and outcome data into insights that support management decisions on cost control, patient risk management, and care quality.

The goal of this report is to summarize the dashboard's findings in a structured format for management review, and to translate the numbers into clear, actionable recommendations.

---

## 2. Data Description

The dataset underlying this dashboard covers hospital patient admission, condition, procedure, and outcome records. Each record includes:

| Field | Description |
|---|---|
| Patient ID | Unique identifier per patient |
| Gender | Female, Male |
| Condition/Diagnosis | Medical condition or diagnosis (15 unique diagnoses) |
| Outcome | Patient outcome: Recovered or Stable |
| Readmission | Whether the patient was readmitted (Yes/No) |
| Length of Stay (LOS) | Number of days admitted |
| Revenue/Cost | Revenue and cost generated per patient/procedure |
| Procedure | Type of procedure performed |
| Satisfaction Score | Patient satisfaction rating |

**Scope:** 984 patients, $8.23M in total revenue, filterable by Gender, Outcome, and Readmission status, across two dashboard pages (Hospital Patients Analysis, Patient Risk and Efficiency).

---

## 3. Methodology

The analysis followed these steps:

1. **Data consolidation** – Patient admission, condition, procedure, and outcome records were combined into a single structured table.
2. **Data cleaning** – Records were checked for missing values, consistent condition/procedure naming, and correct outcome and readmission classification.
3. **Aggregation** – Revenue, cost, length of stay, satisfaction, and readmission were aggregated by condition, gender, outcome, and procedure.
4. **Visualization** – Aggregated measures were built into a 2-page interactive Power BI dashboard using KPI cards, bar charts, a donut chart, and a satisfaction gauge, with slicers for Gender, Outcome, and Readmission.
5. **Interpretation** – Patterns in the visualized data were reviewed to identify cost drivers, risk concentrations, and satisfaction gaps warranting management attention.

**Tool used:** Power BI Desktop

---

## 4. Analysis and Findings

### 4.1 Overall Performance

| Metric | Value |
|---|---|
| Total Revenue | **$8.23M** |
| Total Patients | **984** |
| Average Length of Stay (Days) | **37.66** |
| Readmission Rate | **26.83%** |
| Average Revenue per Patient | **$8,367.48** |
| Unique Diagnoses | **15** |
| Number of Outcome Categories | **2 (Recovered, Stable)** |

An average length of stay of 37.66 days is notably long, and a readmission rate of 26.83% — roughly 1 in 4 patients — signals meaningful room for improvement in discharge planning and follow-up care.

### 4.2 Total Revenue by Condition (Top 5)
- Cancer: **$1.65M**
- Prostate Cancer: **$1.30M**
- Heart Attack: **$1.21M**
- Heart Disease: **$0.98M**
- Childbirth: **$0.78M**

### 4.3 Total Revenue by Condition (Bottom 5)
- Diabetes: **$130K**
- Hypertension: **$66K**
- Respiratory Infection: **$52K**
- Fractured Arm: **$33K**
- Allergic Reaction: **$7K**

The top 5 conditions alone generate **$5.92M**, roughly **74% of total revenue**, while the bottom 5 conditions combined contribute less than $300K — revenue is heavily concentrated in a small number of major conditions, led by oncology and cardiac care.

### 4.4 Outcome by Total Cost
- Recovered: **~$1.75M (63.58%)**
- Stable: **~$1.0M (36.42%)**

Nearly two-thirds of this tracked cost measure is associated with patients who ultimately recovered, with the remainder tied to patients discharged in stable (not fully recovered) condition.

### 4.5 Condition by Readmission
- No readmission: **292 patients**
- Readmitted: **33 patients**

This 292:33 split (~89.8% vs. ~10.2%) is drawn from the procedure-level cost tracking population (325 patients, see Section 4.8), distinct from the full 984-patient base, and is consistent with the 26.83% headline readmission rate calculated across the broader patient population.

### 4.6 Average Satisfaction vs. Target
- Actual: **3.60**
- Target: **4.00**
- Scale: **0.00–5.00**

Average patient satisfaction (3.60) falls short of the 4.00 target by 0.40 points, indicating an unmet service quality goal.

### 4.7 Average Length of Stay by Gender
- Male: **~39–40 days**
- Female: **~35–36 days**

Male patients show a somewhat longer average length of stay than female patients, a gap worth investigating by condition mix.

### 4.8 Procedure Cost Summary

| Procedure | Patient Count | Total Cost | Average Cost |
|---|---|---|---|
| Radiation Therapy | 65 | $1,300,000 | $20,000.00 |
| CT Scan and Medication | 66 | $660,000 | $10,000.00 |
| Lithotripsy | 64 | $390,000 | $6,000.00 |
| Physical Therapy and Pain Management | 64 | $256,000 | $4,000.00 |
| Antibiotics and Rest | 65 | $52,000 | $800.00 |
| **Total** | **325** | **$2,658,000** | **$8,178.46** |

Radiation Therapy alone accounts for **~49% of this tracked procedure cost** ($1.3M of $2.658M), despite having a similar patient count to the other procedures — it is by far the most expensive procedure per patient ($20,000 average).

### 4.9 Satisfaction by Outcome
- Stable: **~570** (satisfaction-weighted total)
- Recovered: **~360** (satisfaction-weighted total)

Patients with a Stable outcome show a notably higher satisfaction-weighted total than those who Recovered — worth further investigation, as it may reflect differences in expectations, condition severity, or care experience between the two outcome groups.

---

## 5. Key Insight

- **Length of stay and readmission both signal risk.** An average LOS of 37.66 days and a 26.83% readmission rate (~1 in 4 patients) point to opportunities in discharge planning and post-discharge follow-up.
- **Revenue is heavily concentrated in a few major conditions.** Cancer, Prostate Cancer, Heart Attack, Heart Disease, and Childbirth together generate roughly 74% of total revenue.
- **Radiation Therapy is the dominant cost driver among tracked procedures**, at $20,000 average cost per patient — nearly double the next most expensive procedure (CT Scan and Medication at $10,000).
- **Patient satisfaction is below target.** At 3.60 against a 4.00 goal, satisfaction is falling short by a meaningful margin.
- **Male patients have a longer average length of stay than female patients**, a gap that warrants a closer look at underlying condition mix.
- **Satisfaction appears higher among Stable-outcome patients than Recovered patients**, a counterintuitive pattern worth validating and understanding further.

---

## 6. Recommendation

1. **Investigate the drivers of the 37.66-day average length of stay and the 26.83% readmission rate**, starting with the top-revenue conditions (Cancer, Prostate Cancer, Heart Attack, Heart Disease), to identify discharge and follow-up care improvements.
2. **Review Radiation Therapy cost structure**, given its outsized $20,000 average cost per patient, to confirm pricing, resource allocation, and whether cost-efficiency opportunities exist.
3. **Launch a satisfaction improvement initiative** targeting the 0.40-point gap between actual (3.60) and target (4.00) satisfaction scores, starting with root-cause analysis of the Recovered-outcome group's lower satisfaction-weighted total.
4. **Examine the gender gap in length of stay** (Male ~39–40 days vs. Female ~35–36 days) to determine whether it reflects differences in condition severity, treatment pathway, or care delivery.
5. **Protect and invest in high-revenue service lines** (oncology and cardiac care), which together drive the large majority of total revenue, while monitoring cost efficiency in lower-revenue conditions.
6. **Reconcile the different patient-count bases used across the dashboard** (984 total patients vs. 325 in the procedure-cost table) to ensure metrics are being compared on a consistent population going forward.

---

## 7. Conclusion

Across 984 patients and $8.23M in total revenue, this hospital's performance shows both strong points and clear areas for improvement. Revenue is heavily concentrated in a handful of major conditions — led by Cancer, Prostate Cancer, and Heart Attack — while Radiation Therapy stands out as the most expensive procedure by a wide margin. At the same time, an average length of stay of 37.66 days, a readmission rate of 26.83%, and a patient satisfaction score of 3.60 (against a 4.00 target) all point to meaningful opportunities to improve patient outcomes and experience. Acting on the recommendations in this report — tightening discharge and follow-up processes, reviewing high-cost procedures, and closing the satisfaction gap — can help management improve both the quality of care delivered and the efficiency of hospital operations going forward.

---

**Prepared by:** Ubong Solomon
