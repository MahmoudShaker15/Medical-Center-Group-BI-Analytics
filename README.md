# Medical Center BI Solution 🏥

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

<img width="955" height="617" alt="Star Schema" src="https://github.com/user-attachments/assets/1a385a5d-1780-4140-9c4a-5e8edbaf6b09" />

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

## Key Findings & Dashboards

- **Top hospital by revenue:** Eastfield Care Hospital
- **Top specialty by revenue:** Cardiology
- **Top doctor by revenue:** Dr. Philip Graves
- **Revenue split:** Outpatient 35.93% | Emergency 32.8% | Inpatient 31.27%
- **Highest patient satisfaction by specialty:** Orthopedics
- **Peak visit month:** August (79 visits)

### Financial Performance

<img width="1996" height="1119" alt="Financial Performance" src="https://github.com/user-attachments/assets/a9a30ae2-0a8c-408a-9d2a-4b1ad8251109" />

### Doctors & Patients Analysis (Doctoors View)

<img width="1985" height="1113" alt="Doctors   Patients Analysis (Doctors View)" src="https://github.com/user-attachments/assets/12b87aab-1f76-4a09-8f29-c13d49e669ba" />

### Doctors & Patients Analysis (Patients View)

<img width="1986" height="1113" alt="Doctors   Patients Analysis (Patients View)" src="https://github.com/user-attachments/assets/5a5a0c75-fa6d-49aa-983a-917cef82cf35" />
