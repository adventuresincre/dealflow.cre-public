# DealFlow.CRE Public Repository

## 📌 Overview
This repository contains standardized **commercial real estate (CRE) investment data**, best practices, and open resources for deal tracking, underwriting, and analysis.

## 📂 Key Files
### **1️⃣ attributes.xlsx** (🔄 Version-tracked)
This file contains all **attribute-related data** for DealFlow.CRE, ensuring consistency and standardization across the platform.

#### 📋 **Worksheets:**
- **`deal_attributes`** – Defines core attributes for **Deals** (in development).  
- **`attribute_selections`** – Predefined **data validation lists** (e.g., `Deal_Status`).  
- **`glide_input_types_2.16.2025`** – Glide’s **input types** as of **2.16.2025**.

### **2️⃣ address_msa_protocol.md**
Defines how addresses are **standardized using Google Maps API** and how **Metropolitan Statistical Areas (MSAs)** are assigned based on **Census Delineation Files**.

### **3️⃣ selection_list_protocol.md**
Explains how **data validation lists** are structured and maintained within **`attribute_selections`** in `attributes.xlsx`.

### **4️⃣ Census Delineation Files)**
A **separate dataset** mapping **counties to MSAs** based on **U.S. Census Bureau** data found here: https://www.census.gov/geographies/reference-files/time-series/demo/metro-micro/delineation-files.html

---

## ✅ How to Use
- **Developers & Analysts**: Use **`attributes.xlsx`** as the standard for deal tracking.
- **Contributors**: Open an **Issue** or submit a **Pull Request** if updates are needed.

For questions, open an issue in this repository! 🚀
