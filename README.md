# 🛒 Big Mart Sales Prediction  

![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-Project-green?logo=scikitlearn)
![XGBoost](https://img.shields.io/badge/XGBoost-Model-orange?logo=xgboost)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

---

## 📖 Project Overview  
This project predicts the **sales of products at different Big Mart outlets** using **Machine Learning (XGBoost Regressor)**.  
The goal is to build a predictive model that can help retailers forecast sales, optimize stock, and improve decision-making.  

---

## 📂 Dataset  
The dataset contains information about:  

## 📑 Dataset Description  

| Column Name            | Description                                                                 | Example Value       |
|-------------------------|-----------------------------------------------------------------------------|---------------------|
| **Item_Identifier**     | Unique ID for each product                                                  | FDA15               |
| **Item_Weight**         | Weight of the product (in kilograms)                                        | 9.3                 |
| **Item_Fat_Content**    | Whether the product is low-fat or regular                                   | Low Fat / Regular   |
| **Item_Visibility**     | % of total display area allocated to the product in the store               | 0.016047            |
| **Item_Type**           | Category to which the product belongs                                       | Dairy / Snacks      |
| **Item_MRP**            | Maximum Retail Price (list price) of the product                            | 249.8               |
| **Outlet_Identifier**   | Unique ID for each outlet                                                   | OUT049              |
| **Outlet_Establishment_Year** | Year when the store was established                                  | 1999                |
| **Outlet_Size**         | Size of the outlet (Small / Medium / High)                                  | Medium              |
| **Outlet_Location_Type**| Type of city where the outlet is located (Tier 1 / Tier 2 / Tier 3)         | Tier 1              |
| **Outlet_Type**         | Type of outlet (e.g., Grocery Store, Supermarket Type1/2/3)                 | Supermarket Type1   |
| **Item_Outlet_Sales**   | **Target Variable** – Sales of the product in a particular outlet (in ₹)    | 3735.1              |


- **Product Attributes**:  
  - Item Identifier  
  - Item Fat Content  
  - Item Type  
  - Item MRP  

- **Outlet Attributes**:  
  - Outlet Identifier  
  - Outlet Size  
  - Outlet Location Type  
  - Outlet Type  

- **Target Variable**:  
  - `Item_Outlet_Sales` (sales value to be predicted)

---

## ⚙️ Data Preprocessing  
✔️ Handled missing values:  
- Replaced missing values in **Outlet_Size** using the mode of corresponding **Outlet_Type**.  

✔️ Cleaned categorical columns:  
- Unified inconsistent categories in **Item_Fat_Content** (`low fat`, `LF` → `Low Fat`, `reg` → `Regular`).  

✔️ Encoding:  
- Converted categorical features into numerical format using **Label Encoding** (`Item_Type`, `Outlet_Type`, etc.).  

---

## 🤖 Model Training  
- Algorithm Used: **XGBoost Regressor**  
- Train-Test Split: **80-20**  

### 🔧 Model Parameters (default XGBoost)  
- Booster: `gbtree`  
- Learning rate: 0.1  
- Max depth: 6  
- Number of estimators: 100  

---

## 📌 Interpretation:  
- The model explains **85.8% of variance** on training data.  
- On test data, it explains **55.1% of variance**, showing moderate generalization.  

---

## 🚀 Future Improvements  
🔹 Hyperparameter tuning with GridSearchCV / RandomizedSearchCV  
🔹 Feature scaling and transformation  
🔹 Ensemble methods: LightGBM, CatBoost, Random Forest  
🔹 Adding feature importance analysis  

---


