# 🇧🇩 Bangladesh Administrative Data — Open Dataset

A comprehensive open dataset covering **Bangladesh's administrative geography** at both the **Upazila level (~491 units)** and **Police Thana level (~767 units)**, spanning demographics, health, education, infrastructure, agriculture, crime, digital economy, gender, disaster risk, and more.

> **Data is modelled/estimated** from division-level official statistics (BBS, DGHS, Bangladesh Police). Suitable for research, planning, and comparative analysis. Not a substitute for official census data.

---

## 📁 Folder Structure

```
bangladesh-administrative-data/
│
├── README.md
│
├── excel/                          ← Original Excel workbooks
│   ├── Bangladesh_Upazila_Comprehensive.xlsx
│   ├── Bangladesh_Upazila_Expanded.xlsx
│   └── Bangladesh_Police_Thana_COMPLETE_FINAL.xlsx
│
├── csv/
│   ├── upazila/                    ← One CSV per category (491 upazilas each)
│   │   ├── upazila_01_overview.csv
│   │   ├── upazila_02_education.csv
│   │   ├── upazila_03_healthcare.csv
│   │   ├── upazila_04_infrastructure.csv
│   │   ├── upazila_05_agriculture.csv
│   │   ├── upazila_06_water_sanitation.csv
│   │   ├── upazila_07_disaster_risk.csv
│   │   ├── upazila_08_administrative.csv
│   │   ├── upazila_09_poverty_development.csv
│   │   ├── upazila_12_employment_labour.csv
│   │   ├── upazila_13_gender_social.csv
│   │   ├── upazila_14_transport_connectivity.csv
│   │   ├── upazila_15_housing_living.csv
│   │   ├── upazila_16_religion_ethnicity.csv
│   │   └── upazila_17_digital_economy.csv
│   │
│   ├── thana/                      ← One CSV per category (767 thanas each)
│   │   ├── thana_01_directory.csv
│   │   ├── thana_02_policing.csv
│   │   ├── thana_03_demographics.csv
│   │   ├── thana_04_infrastructure.csv
│   │   ├── thana_05_crime.csv
│   │   ├── thana_06_special_jurisdiction.csv
│   │   └── thana_07_economic_profile.csv
│   │
│   └── summary/                    ← Merged & summary files
│       ├── upazila_master_merged.csv   ← All 15 upazila categories in one file
│       ├── thana_master_merged.csv     ← All 7 thana categories in one file
│       ├── upazila_division_summary.csv
│       └── thana_division_summary.csv
```

---

## 📊 Dataset Overview

### Upazila Level — 491 Upazilas × 15 Categories

| File | Columns | Description |
|------|---------|-------------|
| `upazila_01_overview.csv` | 8 | Area, population, density, urban %, main economy |
| `upazila_02_education.csv` | 9 | Literacy rate, school counts, enrolment rate |
| `upazila_03_healthcare.csv` | 10 | Hospitals, doctors, nurses, immunisation, MMR |
| `upazila_04_infrastructure.csv` | 10 | Roads, electricity, internet, mobile, banking |
| `upazila_05_agriculture.csv` | 12 | Crop types, irrigated land, fisheries |
| `upazila_06_water_sanitation.csv` | 9 | Safe water, sanitation, arsenic risk |
| `upazila_07_disaster_risk.csv` | 10 | Flood, cyclone, drought, climate vulnerability |
| `upazila_08_administrative.csv` | 9 | Unions, municipalities, constituencies |
| `upazila_09_poverty_development.csv` | 9 | Poverty rate, HDI, NGOs, food security |
| `upazila_12_employment_labour.csv` | 12 | Labour force, unemployment, sector split |
| `upazila_13_gender_social.csv` | 11 | Sex ratio, child marriage, women empowerment |
| `upazila_14_transport_connectivity.csv` | 12 | Highway, railway, river ports, bridges |
| `upazila_15_housing_living.csv` | 12 | Dwelling type, assets, cooking fuel |
| `upazila_16_religion_ethnicity.csv` | 9 | Religious composition, ethnic groups, languages |
| `upazila_17_digital_economy.csv` | 12 | Smartphone, MFS, 4G coverage, freelancers |
| **`upazila_master_merged.csv`** | **112** | **All categories merged into one file** |

### Police Thana Level — 767 Thanas × 7 Categories

| File | Columns | Description |
|------|---------|-------------|
| `thana_01_directory.csv` | 12 | Name, type, area, population, OC rank, FIRs |
| `thana_02_policing.csv` | 15 | Officers, constables, vehicles, detection rate |
| `thana_03_demographics.csv` | 12 | Population, density, gender, literacy |
| `thana_04_infrastructure.csv` | 14 | Roads, electricity, internet, 4G, banks |
| `thana_05_crime.csv` | 11 | Total crime, murder, robbery, narcotics, GBV |
| `thana_06_special_jurisdiction.csv` | 13 | Border, EPZ, port, tourism, flood/cyclone risk |
| `thana_07_economic_profile.csv` | 12 | Poverty, employment, remittance, e-commerce |
| **`thana_master_merged.csv`** | **56** | **All categories merged into one file** |

---

## 🗺️ Administrative Coverage

| Unit | Count |
|------|-------|
| Divisions | 8 |
| Districts | 64 |
| Upazilas (in dataset) | 491 |
| Police Thanas (in dataset) | 767 |

**Divisions:** Barisal · Chittagong · Dhaka · Khulna · Mymensingh · Rajshahi · Rangpur · Sylhet

---

## 🚀 Quick Start

### Python (pandas)
```python
import pandas as pd

# Load all upazila data in one shot
df = pd.read_csv("csv/summary/upazila_master_merged.csv")
print(df.shape)   # (491, 112)
print(df.head())

# Load just the thana directory
thanas = pd.read_csv("csv/thana/thana_01_directory.csv")
print(thanas[thanas["Division"] == "Dhaka"].head(10))

# Filter by flood risk
high_risk = df[df["Flood Risk"] == "Very High"]
print(f"Very high flood risk upazilas: {len(high_risk)}")
```

### R
```r
library(tidyverse)

# Load upazila overview
df <- read_csv("csv/upazila/upazila_01_overview.csv")

# Top 10 most densely populated upazilas
df %>% arrange(desc(`Pop. Density (/km²)`)) %>% head(10)
```

### Excel / Power BI / Tableau
Just open any `.csv` file directly — all files use UTF-8 encoding with headers in row 1.

---

## 📋 Key Fields Reference

### Upazila files — joining key
```
Division | District | Upazila
```

### Thana files — joining key
```
Division | District | Thana / Police Station | Thana Type
```

### Thana Types
| Type | Description |
|------|-------------|
| Metropolitan | DMP, CMP, KMP, SMP city thanas |
| City | District city/municipality thanas |
| Sadar | Upazila HQ thanas |
| Rural | General rural coverage |
| Industrial | EPZ, factory, port-industrial |
| Border | India/Myanmar border thanas |
| Coastal | Bay of Bengal coastal thanas |
| River | Haor/river/ferry-ghat thanas |
| Hill | Chittagong Hill Tracts |
| Tea | Tea-garden area (Sylhet) |
| Tourism | Beach/heritage/eco-tourism |

---

## ⚠️ Disclaimer

All **secondary indicators** (education, health, infrastructure, crime, economic) are **modelled estimates** derived from division-level official statistics using population-weighted calibration. They are suitable for:
- ✅ Comparative and relative analysis between areas
- ✅ Planning, research, and visualisation
- ✅ Teaching and academic use

They are **not** suitable for:
- ❌ Official government reporting
- ❌ Legal or policy decisions requiring verified data

**Official sources:**
- Bangladesh Bureau of Statistics: [bbs.gov.bd](https://www.bbs.gov.bd)
- Bangladesh Police: [police.gov.bd](https://www.police.gov.bd)
- DGHS: [dghs.gov.bd](https://www.dghs.gov.bd)
- Local Govt. Division: [lgd.gov.bd](https://www.lgd.gov.bd)

---

## 📜 License

This dataset is released under the **[Creative Commons Zero v1.0 Universal (CC0)](LICENSE)** license.

You are free to copy, modify, distribute, and use the data for any purpose, even commercially, without asking permission.

---

## 🙌 Contributing

Contributions are very welcome! If you have:
- **Official data** that can replace estimates
- **Corrections** to district/upazila/thana names or boundaries
- **Additional variables** that would be useful

Please open an **Issue** or submit a **Pull Request**.

---

## 📬 Citation

If you use this dataset in research or publications, please cite it as:

```
Bangladesh Administrative Data Repository (2024).
Upazila and Police Thana level dataset for Bangladesh.
GitHub: https://github.com/YOUR_USERNAME/bangladesh-administrative-data
```

---

*Last updated: June 2026 | Data reference year: 2022*
