# Leadership Impact Analysis

## Introduction
This Leadership Impact Analysis examines how informatics leadership can leverage
operational workflow data to improve patient engagement, reduce no-show rates,
and enhance workflow efficiency within a healthcare setting. The analysis aligns
with observations from my leadership practicum, including Epic optimization
governance, interdisciplinary coordination, and patient safety discussions.

The goal of this analysis is to demonstrate how data-informed leadership can
support decision-making related to communication strategies, workflow design,
and performance improvement initiatives.

---

## Dataset Overview
The dataset used for this analysis is a simulated operational workflow dataset
(`operational_workflow_data.csv`) representing patient visits over a three-month
period. The data includes appointment attendance, visit type, communication
channels, and service duration metrics.

Key fields include:
- Department
- Visit type (in-person or telehealth)
- Appointment attendance status
- No-show reason
- Communication channel
- Service duration (minutes)

The dataset contains no protected health information (PHI) and was created
solely for academic practicum purposes.

---

## Analytical Approach
Basic descriptive analytics were planned using Python (pandas and matplotlib)
to identify:
- Overall no-show rates
- Differences in attendance by department
- Common no-show reasons
- Average service duration for completed visits

These analyses are intended to highlight workflow and communication patterns
that may inform leadership decisions related to Epic optimization and patient
outreach strategies.

---

## Python Analysis Code

```python
import pandas as pd
import matplotlib.pyplot as plt

# Load the dataset
df = pd.read_csv("../data/operational_workflow_data.csv")

# Preview the data
df.head()

# Review dataset structure
df.info()

# Convert attended field to boolean
df["attended_bool"] = df["attended"].astype(str).str.lower().map({"yes": True, "no": False})

# Calculate
