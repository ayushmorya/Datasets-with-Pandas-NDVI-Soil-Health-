# Datasets-with-Pandas-NDVI-Soil-Health-
This repository documents what I learned today about importing, inspecting, and cleaning real-world datasets using Python (Pandas) in Jupyter Notebook. The work is based on an NDVI (Normalized Difference Vegetation Index) soil health dataset and follows an industry-style data preprocessing workflow.

## 📌 What This Project Covers

### 1. Importing Data

- Loaded a CSV dataset using `pandas.read_csv()`
    
- Verified successful import by inspecting the first few rows
    

### 2. Dataset Inspection

- Used `df.head()` to preview records
    
- Used `df.info()` to understand:
    
    - Column names
        
    - Data types
        
    - Missing values
        
- Used `df.describe()` to analyze:
    
    - Distribution
        
    - Min, max, mean
        
    - Potential anomalies
        

### 3. Identifying Data Issues

- Detected unrealistic NDVI values (e.g., `999`)
    
- Recognized that NDVI values must always be between **-1 and 1**
    
- Identified categorical target labels not suitable for ML models
    

### 4. Handling Outliers

- Applied clipping to constrain NDVI values:
    
    - Lower bound: `-1`
        
    - Upper bound: `1`
        
- This ensures domain-valid geospatial vegetation data
    

### 5. Feature Transformation

- Converted categorical health labels into numerical values:
    
    - `healthy → 1`
        
    - `unhealthy → 0`
        
- Prepared the dataset for machine learning models
    

---

## 🧠 Key Learnings

- Real-world datasets are **never clean**
    
- Domain knowledge (like NDVI ranges) is critical in data cleaning

Author: Ayush M

Learning-focused, resume-ready, and industry-aligned ✨
    
- Data inspection is mandatory before modeling
    
- ML models require **numerical features**, not text
    
- Pandas provides powerful, simple tools for preprocessing


Author: Ayush M

Learning-focused, resume-ready, and industry-aligned ✨
