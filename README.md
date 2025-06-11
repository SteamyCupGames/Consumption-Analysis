# 🧠 Domestic Electricity Consumption Forecasting (Tarea 2 - Néstor Piedra)

This repository contains a **data storytelling and linear regression analysis** of domestic electricity consumption, based on time series data. The original project was written in **Spanish** as part of an academic assignment for a Big Data course, but this `README.md` is in **English** to serve as part of my data science portfolio. 

As a mechatronic engineer, as soon as I started working on this project, the recent blackout in the Iberian Peninsula came to my mind. Although I am a faithful supporter of clean energy, it is important to have a proper consumption planning because energies such as wind energy are unpredictable and fickle, so special care must be taken to avoid situations of this type.

---

## 📘 Project Overview

This project demonstrates how to:

- Clean and prepare time-stamped electricity usage data
- Select a focused time window for modeling (only the year 2010)
- Build a **linear regression model** to predict energy consumption
- Evaluate model performance using correlation
- Apply the model to new data (2020) for forecasting
- Analyze peak consumption periods
- Simulate future behavior during peak hours using regression

All analysis and visualizations were written in **R Markdown**, and the final output is available as an interactive **HTML report** (in Spanish).

---

## 📊 Dataset

Two datasets were used:

- `consumo_electrico_domestico.csv`: Historical domestic electricity consumption data (includes timestamped energy variables).
- `consumo_electrico_domestico2020.csv`: Similar data structure, used to apply the trained model and test generalization on newer data.

Each record includes:

- Date and time
- Active and reactive energy
- Intensity, voltage, and sub-meter readings

---

## 📈 Modeling Approach

- Selected data from 2010 to ensure manageability and recentness
- Cleaned missing values (`NA`) and removed irrelevant columns
- Trained a **linear regression model** using all remaining variables
- Split data into training and test sets (67/33%)
- Evaluated the model with correlation (≈ 99.9%)
- Applied the model to 2020 data
- Identified **Sunday at 8:00 PM** as peak consumption
- Simulated future values using a secondary regression model during peak hours

---

## 📂 Files

- `Tarea2_Nestor_Piedra.Rmd`: Original Spanish R Markdown file with analysis
- `Tarea2_Nestor_Piedra.html`: Rendered HTML report
- `consumo_electrico_domestico.csv`: Historical data (2010 and earlier)
- `consumo_electrico_domestico2020.csv`: New data for forecasting
- `README.md`: English description of the project for portfolio purposes

---

## 🛠️ Reproducibility

To run this analysis:

1. Clone this repo
2. Open the `.Rmd` file in **RStudio**
3. Install the required libraries:
   ```r
   install.packages(c("readr", "dplyr", "ggplot2", "caret", "corrplot"))
