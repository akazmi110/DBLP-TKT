# DBLP-TKT: Temporal Keyword Trend Dataset from the DBLP Citation Network

This repository provides the **DBLP-Temporal Keyword Trend (DBLP-TKT) Dataset**, constructed from the DBLP Citation Network (v14), to facilitate research on **temporal keyword analysis**, **hot topic detection**, and **trend forecasting** in computer science literature.

## 📘 Overview

The DBLP-TKT dataset is built using metadata from the [DBLP-Citation-network V14](https://www.aminer.cn/citation), compiled by the AMiner team. It contains the **annual frequency of preprocessed author-defined keywords** from the years **1936 to 2022** (excluding years with incomplete or missing data).

This dataset is useful for:
- Time series analysis of research trends
- Forecasting keyword popularity
- Trend classification of emerging technologies
- Bibliometric and scientometric studies

---

## 📂 Dataset Structure

The main dataset file:

- **`DBLP-TKT.csv`**  
  A tabular time series where:
  - **Rows** = preprocessed keywords
  - **Columns** = years (1936 and 1951–2022)
  - **Values** = frequency of keyword appearances in that year

Sample entry:
| Keyword              | 1936 | 1951 | ... | 2020 | 2021 | 2022 |
|----------------------|------|------|-----|------|------|------|
| deep learn           | 0    | 0    | ... | 6436 | 10083| 10134|
| data mine            | 0    | 0    | ... | 941  | 1297 | 1097 |

---

## 🧹 Keyword Preprocessing

Each keyword in the dataset was processed through the following steps:
1. Lowercasing
2. Removal of numbers, special characters
3. Tokenization and stopword removal
4. Porter stemming
5. Rejoining cleaned words to form preprocessed keywords

---

## 🛠️ Construction Pipeline

The dataset was generated using a custom script that:
- Parses JSON-formatted DBLP articles
- Extracts keywords and publication years
- Filters incomplete entries and missing years
- Computes per-year keyword frequency
- Saves the data in CSV format

A high-level pseudocode of the process is available in the related publication and repository.

---

## 📉 Excluded Years

Certain years were excluded due to data unavailability or incompleteness:
- 1937–1947
- 1949–1950
- 2023 (partial)
- 2024 (incomplete keyword data)

---

## 📜 Citation

If you use this dataset in your research, please cite the following:

@misc{akazmi2025dblptkt,
  author       = {Anab Batool Kazmi},
  title        = {DBLP-TKT: Temporal Keyword Trend Analysis Dataset and Code},
  year         = {2025},
  howpublished = {\url{https://github.com/akazmi110/DBLP-TKT}}
 
}




