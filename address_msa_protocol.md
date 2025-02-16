# Address & Metropolitan Statistical Area (MSA) Protocol

## 📌 Overview
This document outlines how **DealFlow.CRE** standardizes addresses and assigns Metropolitan Statistical Areas (MSAs) to properties using reliable geographic data.

## 📍 Address Standardization
We use **Google's Geocoding API** to ensure that all addresses are **consistent, properly formatted, and enriched with geographic metadata**.

### **Steps for Address Handling**
1. **User Input:** The user provides an address.
2. **Google Geocoding API Lookup:** The address is validated and standardized.
3. **Key Address Components Stored:**
   - **Formatted Address** – Standardized version of the input address.
   - **Latitude & Longitude** – GPS coordinates for precise mapping.
   - **County** – Extracted from the `administrative_area_level_2` field.
   - **State** – Extracted from `administrative_area_level_1`.
   - **ZIP Code** – Extracted from `postal_code`.

---

## 📊 Mapping Counties to Metropolitan Statistical Areas (MSAs)
**Why MSAs?**  
Metropolitan Statistical Areas (MSAs) provide a standardized way to group **economically related counties**. This is critical for real estate analysis, market research, and investment decision-making.

### **How MSAs Are Assigned**
1. **Extract County from Google Geocoding API.**
2. **Match County to MSA** using U.S. Census Bureau **Delineation Files**.
3. **Store MSA Information** alongside the deal's address.

---

## 📂 Data Sources
- **Google Geocoding API** – Used for address standardization.
- **U.S. Census Bureau Delineation Files** – Used for county-to-MSA mapping.
  - 📌 Latest delineation file can be found [here](https://www.census.gov/geographies/reference-files/time-series/demo/metro-micro/delineation-files.html).

---

## ✅ Implementation Notes
- **If a county belongs to multiple MSAs** → The primary assigned MSA from Census data is used.
- **If an address is outside an MSA** → It is flagged as **“Non-Metro”** for classification.
- **Future Integration**: We may add Census API support for real-time MSA matching.

---

## 📢 Contribution & Feedback
If you have suggestions for improving this protocol, please open an issue in this repository.  
