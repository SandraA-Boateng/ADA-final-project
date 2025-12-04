# ADA Final Project: BMI and the Dual Burden of Hypertension & Diabetes (BRFSS 2023, Missouri)

## Project Description
This repository contains the complete analysis for my Advanced Data Analysis final project.  
The goal of this work is to examine whether body mass index (BMI) is associated with the dual burden of hypertension and diabetes among Missouri adults aged 35 years and older, using the 2023 Behavioral Risk Factor Surveillance System (BRFSS).

The project also assesses whether this association differs by race. All data cleaning, descriptive analyses, regression models, effect-measure-modification testing, and diagnostics were completed in R (version ≥ 4.3) following reproducible research practices.

**Because BRFSS data are publicly available and large, the raw dataset is not included in the repository.  
The R Markdown file automatically downloads the 2023 BRFSS ZIP file directly from the CDC.**

---

## Files Included

### **Project_Analysis_Code.Rmd**
The full reproducible analysis, including:
- Data download from the CDC
- Data cleaning and analytic dataset construction
- Descriptive statistics and Table 1
- Logistic regression modeling
- BMI × race interaction testing
- Model diagnostics (linearity, multicollinearity, influence)
- Visualizations and output tables

### **README.md**
This file. Provides an overview of the project, dataset details, and instructions for reproducing the analysis.

> *Note:* The BRFSS `.XPT` file is not uploaded due to size limits.  
> The R Markdown script retrieves it automatically during knitting.

---

## Dataset Description

### **Source**
Behavioral Risk Factor Surveillance System (BRFSS), 2023  
Centers for Disease Control and Prevention (CDC)  
Public dataset: https://www.cdc.gov/brfss/annual_data/2023/

### **Study Population**
The analytic sample includes Missouri adults aged **≥ 35 years** with complete data for:
- BMI  
- Hypertension  
- Diabetes  
- Age  
- Sex  
- Race  
- Smoking status  

### **Key Variables**
- **Exposure:** Body Mass Index (BMI), as continuous and categorized  
- **Outcome:** Dual burden (co-occurring hypertension and diabetes)  
- **Covariates:** Age, sex, race (White/Black), smoking status  
- **Effect Modifier:** Race in interaction with BMI  

---

## What the Code Does

### **1. Imports and Prepares Data**
- Downloads the BRFSS 2023 ZIP file from the CDC  
- Extracts the `.XPT` file and loads it into R  
- Filters to Missouri adults aged ≥ 35  
- Recodes variables and creates the dual-burden outcome  
- Produces a complete-case analytic dataset  

### **2. Descriptive Analysis**
- Table 1 summarizing demographic and clinical characteristics  
- Prevalence of dual burden across BMI groups  
- Flowchart of sample selection  

### **3. Regression Models**
- Unadjusted logistic regression  
- Adjusted model (age, sex, race, smoking)  
- Final model using BMI categories after linearity testing  

### **4. Effect Measure Modification**
- BMI × race interaction term  
- Likelihood ratio test for nested models  
- Predicted-probability visualization  

### **5. Model Diagnostics**
- Linearity (Box–Tidwell)  
- Multicollinearity (VIF)  
- Influential points (Cook’s distance)  

---

## How to Run the Code

1. **Clone this repository**
   ```bash
   git clone https://github.com/SandraA-Boateng/ADA-final-project.git
   
2. **Open Project_Analysis_Code.Rmd in RStudio.**

3. **Ensure your working directory is set to the project folder.** 

4 **Run the acript** 

Author

Sandra Agyenim-Boateng
Advanced Data Analysis
December 2025
