# PROJECT: Investigate a Dataset - No-show Appointments

## Table of Contents

1. Introduction
2. Data Wrangling
3. Exploratory Data Analysis
4. Conclusions

## Introduction

### Dataset Description

This dataset collected information from 100k medical appointments in Brazil, focusing on whether patients showed up for their appointments. Each row includes various patient characteristics:

- **AppointmentDay**: The day the patient set up their next appointment.
- **Age**: Age of the patient.
- **ScheduledDay**: The day the patient set up their appointment.
- **Neighborhood**: Location of the hospital.
- **Scholarship**: Indicates whether the patient is enrolled in the Brazilian welfare program Bolsa Família.
- **Hypertension**: Indicates if the patient has hypertension.
- **Diabetes**: Indicates if the patient has diabetes.
- **Alcoholism**: Indicates if the patient has issues with alcoholism.
- **Handicap**: Indicates if the patient is handicapped.
- **SMS_received**: Number of reminder text messages sent to the patient.
- **No_show**: 'No' if the patient showed up for their appointment, 'Yes' if they did not.

### Questions for Analysis

1. What was the age distribution of patients who did/didn't show up for their appointments?
2. Which patients with medical conditions registered the most no-show appointments? What is the correlation between medical conditions and no-shows?
3. What was the proportion of each patient attribute in the dataset?
4. What was the relationship between age/gender and the diabetic condition of patients?

## Data Wrangling

### General Properties

- Imported data using Pandas.
- Checked for duplicates and null values (found none).
- Renamed columns for consistency (`Hipertension` to `Hypertension`, `No-show` to `No_show`).
- Cleaned data types (`PatientId` and `AppointmentID` to string, `ScheduledDay` and `AppointmentDay` to datetime).

## Exploratory Data Analysis

- Created an `Age_group` column to categorize ages for better analysis.
- Investigated the age distribution of total appointments and missed appointments.
- Explored proportions of attributes like gender, scholarship, hypertension, diabetes, alcoholism, and handicap among patients.

## Conclusions

- **Age Distribution**: Younger patients tended to have more appointments, while older patients were more likely to show up for their appointments.
- **Medical Conditions**: Patients with hypertension and diabetes were more likely to show up for appointments compared to those without these conditions.
- **SMS Reminders**: Patients receiving SMS reminders showed a higher attendance rate.

### Recommendations

- Consider targeted SMS reminders for patients at higher risk of missing appointments based on age and medical conditions.
- Further investigate the impact of socioeconomic factors (like scholarship enrollment) on appointment attendance.

### Future Work

- Apply machine learning models to predict no-show appointments based on patient demographics and medical history.
- Explore the impact of additional factors such as day of the week or month on appointment attendance.

## Code and Libraries Used

```python
import numpy as np
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
%matplotlib inline
