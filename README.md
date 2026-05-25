# 📊 Production Planning & Industrial Efficiency Dashboard

## 📌 Project Overview
An interactive data visualization and enterprise analytics dashboard engineered in **Power BI** to monitor factory floor efficiency, machine utilization metrics, and manufacturing output. By integrating cross-departmental operations data, this dashboard serves as a central operational command center for production planners, supply chain teams, and plant managers to resolve throughput bottlenecks and audit machinery performance.

## 📈 Dashboard Architecture & Insights

![Industrial Efficiency Dashboard](Dashboard%201.png)

### 1. Unified Operational KPIs
* Tracks real-time performance indicators such as Total Production Volumes, Defect Rates, Yield Percentages, and Machine Capacity Utilization.
* Highlights critical baseline drifts across operational targets to flag manufacturing friction early.

### 2. Machine Performance & Downtime Analysis
* Segregates machinery run-time efficiencies by production lines, allowing targeted interventions on lagging equipment.
* Correlates specific maintenance schedules with historical shift logs to map out optimal operating configurations.

### 3. Supply Chain & Inventory Mapping
* Visualizes material consumption velocities against raw production outputs to manage pipeline inventory.
* Implements dynamic filters to let operations teams drill down by **Shift, Plant Location, Product SKU, and Failure Logs**.

## 🚀 Technical Highlights & DAX Engineering
* **Advanced Data Modeling:** Designed a robust **Star Schema** connecting heavy transactional manufacturing facts with dimension tables (Calendar, Machine Registry, and Product SKUs).
* **Power Query ETL:** Formatted, cleaned, and contextualized irregular sensor files and operational spreadsheets into cohesive structured formats.
* **Custom DAX Measures:** Implemented optimized DAX expressions for calculating complex moving averages, running production counts, and dynamic Year-over-Year (YoY) throughput changes.

## 🧰 Tech Stack
* **Core Platform:** Microsoft Power BI (Desktop & Service)
* **ETL Engine:** Power Query (M Language)
* **Modeling / Expressions:** DAX (Data Analysis Expressions)

## 💡 Strategic Business Impacts
* **Data-Driven Operations:** Eradicates guesswork in shift scheduling by mapping real-time capacities against strategic commercial demands.
* **Cross-Functional Alignment:** Unifies maintenance engineering insights directly with supply chain logistics to ensure smoother lead times.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


# 🛠️ Machine Predictive Maintenance: End-to-End ML Classification

## 📌 Project Overview
This repository contains an end-to-end Machine Learning project developed for **Predictive Maintenance (PdM)** in industrial manufacturing loops. In modern manufacturing environments, unexpected machine failures cause severe downtime losses. This project builds a classification model to proactively predict machine failures and determine the specific root cause of the failure based on real-time sensor metrics (temperatures, rotational speed, torque, and tool wear).

## 🚀 Key Features & Workflow

### 1. Data Ingestion & Exploratory Data Analysis (EDA)
* Analyzed **10,000 industrial records** capturing multiple features: Air Temperature [K], Process Temperature [K], Rotational Speed [rpm], Torque [Nm], Tool Wear [min], and Type (Low, Medium, High quality products).
* Identified a severe **Class Imbalance** where only ~3.39% of data represented a machine failure (`Target = 1`).
* Uncovered key failure correlations (e.g., strong relationships between high Torque combined with high Tool Wear and early tool breakages).

### 2. Rigorous Data Preprocessing
* **Feature Engineering:** Extracted temperature differentials and normalized operational metrics.
* **Handling Class Imbalance:** Applied **SMOTE (Synthetic Minority Over-sampling Technique)** to balance the training features, ensuring the model avoids biased predictions toward normal machine operations.
* **Scaling:** Implemented standard feature scaling (`StandardScaler`) to normalize operational variables with distinct metric bounds (e.g., RPM vs. Kelvins).

### 3. Model Architecture & Training
* Built and validated multiple classification setups using algorithms like **Logistic Regression**, **Random Forest**, and **XGBoost Classifier**.
* Conducted hyperparameter tuning to optimize both multi-class and binary failure boundaries.

### 4. Advanced Evaluation Metrics
* Rather than relying solely on accuracy, the model was evaluated using **Precision, Recall, and F1-Score**.
* Achieved high recall rates on failure tracking, significantly reducing **False Negatives** (undetected machine failures that cause heavy breakdown costs).

## 🧰 Tech Stack & Libraries
* **Environment:** Jupyter Notebook / Google Colab
* **Core Libraries:** `pandas`, `numpy`, `scikit-learn`, `imbalanced-learn` (SMOTE), `seaborn`, `matplotlib`

## 📊 Business Value Delivered
* **Minimizes Downtime:** Shifts factory operations from reactive maintenance to proactive planning.
* **Maximizes Tool Lifespan:** Signals production planners exactly when tool wear reaches critical margins before actual breakdown occurs.
