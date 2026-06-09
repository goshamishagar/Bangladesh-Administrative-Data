<div align="center">

<img src="banner.svg" alt="Bangladesh Administrative Data — flag banner" width="100%"/>

# 🇧🇩 Bangladesh Administrative Data Repository

**The most comprehensive open dataset of Bangladesh's administrative geography**

[![License: CC0](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](LICENSE)
[![Upazilas](https://img.shields.io/badge/Upazilas-491-006A4E?style=flat)](csv/upazila/)
[![Thanas](https://img.shields.io/badge/Police%20Thanas-767-F42A41?style=flat)](csv/thana/)
[![Categories](https://img.shields.io/badge/Data%20Categories-22-0075BE?style=flat)]()
[![Format](https://img.shields.io/badge/Format-CSV%20%7C%20XLSX-orange?style=flat)]()
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)]()

</div>

---

## 🌟 What's Inside

A complete, researcher-ready dataset covering **491 Upazilas** and **767 Police Thanas** across all **8 divisions** and **64 districts** of Bangladesh — with **22 data categories** spanning demographics, health, education, infrastructure, agriculture, crime, gender, digital economy, disaster risk, and more.

---

## 📁 Repository Structure

```
bangladesh-administrative-data/
│
├── 📄 README.md
├── 🖼️  banner.svg                          ← Flag banner (used above)
│
├── 📊 excel/                               ← Full Excel workbooks (multi-sheet)
│   ├── Bangladesh_Upazila_Comprehensive.xlsx
│   ├── Bangladesh_Upazila_Expanded.xlsx
│   └── Bangladesh_Police_Thana_COMPLETE_FINAL.xlsx
│
├── 📂 csv/
│   ├── upazila/                            ← 15 CSVs · 491 rows each
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
│   ├── thana/                              ← 7 CSVs · 767 rows each
│   │   ├── thana_01_directory.csv
│   │   ├── thana_02_policing.csv
│   │   ├── thana_03_demographics.csv
│   │   ├── thana_04_infrastructure.csv
│   │   ├── thana_05_crime.csv
│   │   ├── thana_06_special_jurisdiction.csv
│   │   └── thana_07_economic_profile.csv
│   │
│   └── summary/                            ← Merged & summary files
│       ├── upazila_master_merged.csv       ⭐ All 15 categories · 491 rows · 112 cols
│       ├── thana_master_merged.csv         ⭐ All 7 categories  · 767 rows · 56 cols
│       ├── upazila_division_summary.csv
│       ├── thana_division_summary.csv
│       └── data_dictionary.csv             ← Field-by-field documentation
```

---

## 📊 Data Categories

### 🏘️ Upazila Level — 491 Upazilas

| # | File | Key Fields |
|---|------|------------|
| 01 | `upazila_01_overview.csv` | Area, population, density, urban %, economy |
| 02 | `upazila_02_education.csv` | Literacy rate, schools, enrolment rate |
| 03 | `upazila_03_healthcare.csv` | Hospitals, doctors, nurses, immunisation, MMR |
| 04 | `upazila_04_infrastructure.csv` | Roads, electricity, internet, mobile, banking |
| 05 | `upazila_05_agriculture.csv` | Crops, irrigated land, fisheries, agri HH% |
| 06 | `upazila_06_water_sanitation.csv` | Safe water, sanitation, arsenic risk |
| 07 | `upazila_07_disaster_risk.csv` | Flood, cyclone, drought, climate vulnerability |
| 08 | `upazila_08_administrative.csv` | Unions, municipalities, constituencies |
| 09 | `upazila_09_poverty_development.csv` | Poverty rate, HDI, NGOs, food security |
| 12 | `upazila_12_employment_labour.csv` | Labour force, unemployment, sector split |
| 13 | `upazila_13_gender_social.csv` | Sex ratio, child marriage, women empowerment |
| 14 | `upazila_14_transport_connectivity.csv` | Highways, railway, ports, bridges |
| 15 | `upazila_15_housing_living.csv` | Dwelling type, assets, cooking fuel |
| 16 | `upazila_16_religion_ethnicity.csv` | Religious composition, ethnic groups, languages |
| 17 | `upazila_17_digital_economy.csv` | Smartphone, MFS, 4G, e-commerce, freelancers |
| ⭐ | `upazila_master_merged.csv` | **All 15 categories merged · 112 columns** |

### 🚔 Police Thana Level — 767 Thanas

| # | File | Key Fields |
|---|------|------------|
| 01 | `thana_01_directory.csv` | Name, type, area, population, OC rank, FIRs |
| 02 | `thana_02_policing.csv` | Officers, constables, vehicles, detection rate |
| 03 | `thana_03_demographics.csv` | Population, density, gender, literacy |
| 04 | `thana_04_infrastructure.csv` | Roads, electricity, internet, 4G, banks |
| 05 | `thana_05_crime.csv` | Total crime, murder, robbery, narcotics, GBV |
| 06 | `thana_06_special_jurisdiction.csv` | Border, EPZ, port, tourism, flood/cyclone risk |
| 07 | `thana_07_economic_profile.csv` | Poverty, employment, remittance, e-commerce |
| ⭐ | `thana_master_merged.csv` | **All 7 categories merged · 56 columns** |

---

## 🗺️ Administrative Coverage

<div align="center">

| Division | Upazilas | Police Thanas | Districts |
|----------|:--------:|:-------------:|:---------:|
| 🟢 Barisal | 42 | 78 | 6 |
| 🔴 Chittagong | 103 | 128 | 11 |
| 🟩 Dhaka | 67 | 181 | 13 |
| 🔵 Khulna | 59 | 85 | 10 |
| 🟣 Mymensingh | 35 | 62 | 4 |
| 🟠 Rajshahi | 70 | 88 | 8 |
| 🟤 Rangpur | 58 | 78 | 8 |
| 🟡 Sylhet | 38 | 67 | 4 |
| **Total** | **491** | **767** | **64** |

</div>

---

## 🚀 Quick Start

### Python

```python
import pandas as pd

# All upazila data in one file (491 rows × 112 columns)
df = pd.read_csv("csv/summary/upazila_master_merged.csv")
print(df.shape)

# Top 10 most literate upazilas
edu = pd.read_csv("csv/upazila/upazila_02_education.csv")
print(edu[["Division", "Upazila", "Literacy Rate (%)"]]\
      .sort_values("Literacy Rate (%)", ascending=False).head(10))

# Filter metropolitan police thanas
thanas = pd.read_csv("csv/thana/thana_01_directory.csv")
metro  = thanas[thanas["Thana Type"] == "Metropolitan"]
print(f"Metropolitan thanas: {len(metro)}")

# Upazilas with Very High flood risk
risk = pd.read_csv("csv/upazila/upazila_07_disaster_risk.csv")
print(risk[risk["Flood Risk"] == "Very High"][["Division","Upazila"]])
```

### R

```r
library(tidyverse)

df <- read_csv("csv/summary/upazila_master_merged.csv")

# Average literacy by division
df %>%
  group_by(Division) %>%
  summarise(avg_literacy = mean(`Literacy Rate (%)`, na.rm = TRUE)) %>%
  arrange(desc(avg_literacy))

# Crime totals by division
crime <- read_csv("csv/thana/thana_05_crime.csv")
crime %>%
  group_by(Division) %>%
  summarise(total = sum(`Total Crimes (annual)`, na.rm = TRUE)) %>%
  arrange(desc(total))
```

### Excel / Power BI / Tableau
Open any `.csv` file directly — UTF-8 encoding, headers in row 1, no preprocessing needed.

---

## 🔑 Joining Keys

| Level | Key Columns |
|-------|------------|
| Upazila files | `Division` + `District` + `Upazila` |
| Thana files | `Division` + `District` + `Thana / Police Station` |

### Thana Types

| Type | Description |
|------|-------------|
| `Metropolitan` | DMP / CMP / KMP / SMP city thanas |
| `City` | District city or municipality thanas |
| `Sadar` | Upazila headquarters thanas |
| `Rural` | General rural coverage |
| `Industrial` | EPZ, factory-cluster, port-industrial |
| `Border` | India / Myanmar border thanas |
| `Coastal` | Bay of Bengal coastal thanas |
| `River` | Haor / river / ferry-ghat thanas |
| `Hill` | Chittagong Hill Tracts |
| `Tea` | Tea-garden area (Sylhet Division) |
| `Tourism` | Beach / heritage / eco-tourism |

---

## ⚠️ Disclaimer

All **secondary indicators** are **modelled estimates** derived from division-level official statistics using population-weighted calibration.

✅ Suitable for: comparative analysis · planning · research · teaching · visualisation  
❌ Not for: official government reporting · legal or policy decisions requiring verified data

**Official sources:**
[bbs.gov.bd](https://www.bbs.gov.bd) · [police.gov.bd](https://www.police.gov.bd) · [dghs.gov.bd](https://www.dghs.gov.bd) · [lgd.gov.bd](https://www.lgd.gov.bd)

---

## 📜 License

Released under **[Creative Commons Zero v1.0 Universal (CC0)](LICENSE)** — free for any purpose, no permission needed.

---

## 🙌 Contributing

Pull requests are welcome! If you have official data, corrections, or additional variables, please open an **Issue** or submit a **PR**.

---

## 📬 Citation

```bibtex
@misc{bangladesh_admin_data_2024,
  title = {Bangladesh Administrative Data Repository},
  note  = {Upazila and Police Thana level dataset for Bangladesh},
  year  = {2024},
  url   = {https://github.com/goshamishagar/bangladesh-administrative-data}
}
```

---

<div align="center">

Made with ❤️ for Bangladesh 🇧🇩

*Last updated: June 2026 · Reference year: 2022 · 491 Upazilas · 767 Thanas · 22 categories*

</div>
