# GE Healthcare Reliability Analysis Project

This repository contains the reliability analysis project conducted on real-world healthcare equipment data from GE Healthcare (GE HC). Our goal was to model and analyze the reliability of healthcare systems and components to support decision-making in GE HC's after-sales service process.

Our team achieved **the best accuracy on the test set, with around 5% errors**, demonstrating the effectiveness of our reliability modeling approach.

---

## Project Overview

Healthcare equipment requires **high reliability and availability**. Failures can have severe consequences, and long downtimes are unacceptable for hospitals. GE HC maintains a large-scale service supply chain, supporting over **one million installed systems worldwide**, with **400,000+ spare part references** (including **~10,000 repairable parts**).

The project focused on:
- **Estimating System Reliability:** Identifying the best-fitting statistical model for equipment lifespan.
- **Analyzing Component Failures:** Studying the reliability of individual components.
- **Handling Censored Data:** Accounting for systems that have not yet failed.
- **Using Data-Driven Methods:** Applying probability distributions to model failure rates.

---

## Dataset

The dataset provided by GE HC includes:
- **Failure History:** Repair records for multiple healthcare systems.
- **Censoring Information:** Some systems were still operational at the time of data collection.
- **Component-Level Data:** Information about individual components within each system.

---

## Methodology

### **1. Data Cleaning and Preprocessing**
- Extracted relevant information from raw datasets.
- Identified censored (still functional) and uncensored (failed) data.

### **2. System-Level Reliability Analysis**
- Applied statistical models to estimate system failure probability.
- Used the `Fit_Everything` function from the **Reliability** package.
- Identified **Loglogistic distribution** as the best fit
- Avoided overfitting by excluding complex Weibull Mixture models.

### **3. Component-Level Reliability Analysis**
- Developed a function to estimate the reliability of each component.
- Modeled failures individually to identify weak points in the system.

---

## Results

- **Best Fit for System Reliability:** Loglogistic distribution.  
- **Component Failure Modeling:** Individual analysis for key components.  
- **Final Accuracy:** **~5% error on the test set**, the best performance among groups.  

Our models provide actionable insights into failure patterns, helping improve GE HC's after-sales service efficiency.
