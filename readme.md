# House Price Prediction: A Production-Ready ML Pipeline

> Elevating a standard machine learning project into a top 1% data science portfolio piece through rigorous software engineering, in-depth data exploration, and end-to-end MLOps integration.

This repository demonstrates the complete lifecycle of a machine learning project, predicting house prices based on various home features. Rather than just focusing on model accuracy, this project prioritizes clean code architecture, scalable pipelines, and professional-grade deployment strategies. 

---

## 📌 Project Overview

While many data science projects stop at a Jupyter Notebook, this repository is built as a fully functional, production-ready system. It emphasizes understanding the underlying data, validating assumptions, and applying industry-standard MLOps and design patterns to create a robust and maintainable architecture.

---

## 🚀 What I Learned and Implemented

### 1. Advanced Exploratory Data Analysis (EDA)
* **Data-Driven Decision Making:** Treated EDA as the foundation for feature engineering rather than a simple checklist.
* **Assumption Testing:** Validated algorithmic assumptions directly against the data distribution.
* **Focused Modeling:** Perfected the core data pipeline using a single, robust algorithm to prioritize system architecture over hyperparameter tuning of multiple models.

### 2. MLOps Integration
* **Workflow Orchestration:** Utilized ZenML to manage pipeline execution order and stack integrations.
* **Experiment Tracking:** Implemented MLflow for systematic tracking of model experiments and performance metrics.
* **CI/CD Principles:** Built pipelines that ensure automated testing, reproducibility, and seamless API deployment.

### 3. Software Engineering Best Practices
* **Scalability:** Wrote clean, extensible, and type-checked code.
* **Maintainability:** Segregated logic using proven object-oriented design patterns to allow future features to be added without breaking existing pipelines.

---

## 🏗️ Architecture & Design Patterns

To ensure the codebase remains scalable and flexible, I implemented three core design patterns:

| Design Pattern | Application in Project | Benefit |
| :--- | :--- | :--- |
| **Factory Pattern** | Ingesting data from various formats (ZIP, CSV, JSON). | Dynamically produces the correct ingestor based on file type, handling extraction and error validation automatically. |
| **Strategy Pattern** | Switching between different EDA and modeling techniques. | Enables interchangeable data inspection strategies (univariate, bivariate, multivariate) without modifying the core context. |
| **Template Pattern** | Analyzing and handling missing values. | Provides a fixed algorithmic skeleton for missing value identification, while allowing flexible implementations for different data types. |

---

## 📊 Data Exploration & Engineering Insights

A significant portion of this project was dedicated to understanding the Ames Housing dataset and treating anomalies before modeling.

### Dataset Overview
| Metric | Value |
| :--- | :--- |
| **Total Entries** | 2,930 |
| **Features** | 81 (Numeric + Categorical) |
| **Target Variable** | SalePrice |
| **Average Sale Price** | $179,796 |

### Key Findings & Feature Engineering
* **Distribution Skewness:** The target variable (`SalePrice`) exhibited a heavy right skew. I applied log transformations to satisfy linear regression normality assumptions.
* **Outlier Detection:** Identified severe outliers in features like `Lot Area` and `Ground Living Area` using scatter plots and box plots, which required careful handling to prevent model distortion.
* **Missing Data:** Visualized missingness via heatmaps. Handled both random missing values (scattered) and structured missingness (clustered) using custom imputation strategies.
* **Multivariate Correlations:** Generated correlation heatmaps revealing that `Overall Quality` (0.80) and `Ground Living Area` (0.71) are the strongest predictors of `SalePrice`.

---

## 🗺️ Project Roadmap

| Stage | Implementation Details |
| :--- | :--- |
| **1. Data Ingestion** | Deployed Factory pattern for flexible dataset validation and import. |
| **2. EDA** | Leveraged Strategy pattern for univariate, bivariate, and multivariate analysis. |
| **3. Missing Values** | Implemented Template pattern for consistent missing value visualization and imputation. |
| **4. Feature Engineering** | Handled outliers, normalized skewed distributions, and encoded categorical variables. |
| **5. Model Development** | Built and trained the core ML prediction pipeline. |
| **6. MLOps Orchestration** | Integrated MLflow for experiment tracking and ZenML for pipeline orchestration. |
| **7. Deployment** | Finalized reproducible pipelines ready for API deployment and monitoring. |

---

## 🛠️ Tech Stack

* **Language:** Python
* **Data Manipulation:** Pandas, NumPy
* **Data Visualization:** Matplotlib, Seaborn
* **Machine Learning:** Scikit-Learn
* **MLOps & Orchestration:** ZenML, MLflow
* **Code Architecture:** Object-Oriented Programming (OOP) Design Patterns