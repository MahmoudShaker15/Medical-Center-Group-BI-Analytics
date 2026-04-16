# Medical Center BI Solution

A high-fidelity Business Intelligence solution developed to transform raw operational data from a multi-specialty medical group into actionable insights. This project focuses on financial health monitoring, departmental efficiency, and patient satisfaction benchmarking.

## Project Structure

```
Medical-Center-Group-BI-Analytics/
├── Data/
│   ├── Doctors.csv
│   ├── Hospitals.csv
│   ├── Visits.csv
│   └── Security File.xlsx
│
├── Dashboard & Modeling/
│   ├── Star Schema.png
│   ├── Financial Performance.jpg
│   ├── Doctors & Patients Analysis (Doctors View).jpg
│   └── Doctors & Patients Analysis (Patients View).jpg
│
├── Medical_Center_Analytics.pbix
├── Project_Documentation.pdf
├── Theme.json
└── README.md
```

## Overview

| Metric | Value |
|---|---|
| Doctors | 15 |
| Hospitals | 3 |
| Total Revenue | $6.13M |
| Avg Satisfaction Score | 2.95 / 5 |
| Avg Length of Stay | 7.35 days |

## Data Model

Star schema with `Visits` as the central fact table connected to four dimension tables.

| Table | Type |
|---|---|
| Visits | Fact |
| Doctors | Dimension |
| Patients | Dimension |
| Hospitals | Dimension |
| Date | Dimension (DAX) |

![alt text](<Star Schema.png>)

## Row-Level Security

Each hospital manager is restricted to their assigned hospital's data using:

```dax
[User Email] = USERPRINCIPALNAME()
```

## Technical Implementation

- Custom UI/UX: Developed a specialized "Midnight Medical" JSON theme for a modern, high-contrast dark mode experience.

- Advanced DAX: Engineered complex measures for Time Intelligence, dynamic titling, and conditional KPI formatting.

- Interactive Navigation: Seamless user experience powered by Bookmark-driven state switching to toggle between Patient and Doctor views.

- Dynamic Modeling: Implemented Field Parameters to allow stakeholders to swap chart dimensions and metrics dynamically.

## Key Findings

- **Top hospital by revenue:** Eastfield Care Hospital
- **Top specialty by revenue:** Cardiology
- **Top doctor by revenue:** Dr. Philip Graves
- **Revenue split:** Outpatient 35.93% | Emergency 32.8% | Inpatient 31.27%
- **Highest patient satisfaction by specialty:** Orthopedics
- **Peak visit month:** August (79 visits)

