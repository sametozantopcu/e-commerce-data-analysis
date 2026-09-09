# E-Commerce Data Analysis & Business Insights

## 📌 Project Overview
This repository features a comprehensive Exploratory Data Analysis (EDA) and Data Cleaning pipeline for an e-commerce dataset[cite: 1]. The primary goal is to clean raw transactional data, perform statistical outlier detection, and derive actionable business intelligence regarding customer behavior and category performance[cite: 1].

## 🛠️ Technologies Used
* **Language:** Python[cite: 1]
* **Libraries:** Pandas, Matplotlib, Seaborn[cite: 1]

## ⚙️ Methodology & Workflow

**1. Data Cleaning & Preprocessing:**
* The dataset initially contained 1,428 records and 18 features[cite: 1].
* Handled missing data by applying median imputation for continuous variables (`indirim_orani`, `musteri_puani`) and mode imputation for categorical variables (`odeme_turu`, `musteri_tipi`, `sehir`)[cite: 1].
* Detected and removed 28 duplicate order records to maintain observational uniqueness[cite: 1].

**2. Feature Engineering & Text Normalization:**
* Converted the `siparis_tarihi` column to datetime format and engineered granular temporal features, including `siparis_yili`, `siparis_ayi`, `siparis_gunu`, and `haftanin_gunu`[cite: 1].
* Standardized categorical string data using custom normalization functions (lowercasing, stripping, and replacing Turkish characters) to fix syntax inconsistencies[cite: 1]. This reduced the unique city count from 20 down to 14 and cleanly consolidated product categories[cite: 1].

**3. Domain-Specific Validation & Outlier Detection:**
* Eliminated anomalous records that violated basic domain logic, such as zero/negative prices, negative delivery days, or ratings exceeding the 5.0 maximum limit[cite: 1].
* Applied the Interquartile Range (IQR) method to evaluate continuous variables, successfully isolating 91 extreme statistical outliers in the `birim_fiyat` (unit price) column[cite: 1].

**4. Exploratory Data Analysis (EDA):**
* Visualized data using histograms and box plots to observe the right-skewed distribution of `toplam_tutar` (total amount)[cite: 1].
* Generated count plots to map categorical distribution, revealing that *Kredi Kartı* (Credit Card) is the heavily dominant payment method[cite: 1].

## 💡 Analytical Key Findings
* **Top Performing Category:** The *Elektronik* (Electronics) category yields the highest average transaction revenue at 3,178.4 TL, driving the majority of premium spending and extreme outliers[cite: 1].
* **Customer Demographics:** Existing customers (*Mevcut*) make up 51.02% of the total user base, followed by New customers (*Yeni*) at 37.30%, and a niche *VIP* segment at 11.68%[cite: 1].
* **Satisfaction Metrics:** The overall mean customer rating is an excellent 3.99 out of 5[cite: 1]. Both Existing and New segments average a 4.0 rating[cite: 1]. 
* **Actionable Strategy:** Targeted marketing campaigns should be deployed to capitalize on the sales momentum in the Electronics category, while bespoke services and exclusive perks could help elevate the slightly trailing VIP segment[cite: 1].
