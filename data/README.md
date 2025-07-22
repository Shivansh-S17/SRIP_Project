# 📁 Data Folder

This folder contains data preprocessing and preparation notebooks used in the SRIP project on rainfall bias correction and analysis over the Narmada River basin.

---

## 📊 Datasets Used

### 1. **ERFS Dataset (0.25° x 0.25°)**
- **Type:** Forecasted rainfall data from the Ensemble Rainfall Forecasting System (ERFS)
- **Source:** [IMD ERFS Portal / RIMES / Indian Meteorological Department]
- **Resolution:** 0.25° × 0.25°
- **Usage:** Used as the *input forecast data* requiring bias correction

### 2. **IMD Dataset**
- **Type:** Gridded observed rainfall data
- **Source:** India Meteorological Department (IMD)
- **Usage:** Used as the *ground truth* for observed rainfall to compare and correct ERFS predictions

> ⚠️ **Note:** Due to size and licensing restrictions, raw datasets are not included in this repository. Please download the datasets manually from the respective sources and place them in this folder.

---

## 🧪 Notebooks in this Folder

| Notebook File                  | Purpose                                      |
|-------------------------------|----------------------------------------------|
| `Combining_Data_Files.ipynb`  | Combines downloaded ERFS rainfall data files |
| `Combining_Lead_Files.ipynb`  | Merges forecast lead times into single files |
| `Dataset_Preparation.ipynb`   | Aligns ERFS and IMD data, generates features and targets for modeling |

---

## 📍 Region of Study
- **Region:** Narmada River Basin
- **Latitude / Longitude range:** [Specify exact range if available]
- Data was filtered to focus only on grid points within this region.

---

## 📂 How to Use

1. Download ERFS and IMD datasets and save them in this `data/` folder.
2. Run the notebooks in order:
   - `Combining_Data_Files.ipynb`
   - `Combining_Lead_Files.ipynb`
   - `Dataset_Preparation.ipynb`

3. Proceed to the `models/` folder for training and evaluation.

---

For questions or dataset access help, please refer to the main [README](../README.md).
