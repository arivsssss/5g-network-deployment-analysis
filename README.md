# 📡 5G Network Deployment Data Analysis

## 🌍 Overview
This project analyzes the geographical distribution of 5G network deployments in India, specifically focusing on telecom operators **Airtel** and **Reliance Jio**. The dataset includes deployment locations, status, and geospatial coordinates to perform various analyses, including network coverage, operator recommendation, and deployment patterns using **machine learning models**. 📊

## 📂 Dataset
- **📌 Source:** [Ookla Speed Test 5G Map](https://www.speedtest.net/ookla-5g-map)
- **📑 Format:** Originally in **GeoJSON**, converted to **CSV** for better processing
- **📝 Columns:**
  - `🆔 unique_id`: Unique identifier for each deployment
  - `📶 operator`: Telecom operator providing 5G service (**Airtel / Reliance Jio**)
  - `🏙️ city_name`: Name of the city where deployment is located
  - `📡 status`: Commercial availability or pre-release phase
  - `🌐 latitude`: Latitude coordinate of deployment
  - `🗺️ longitude`: Longitude coordinate of deployment

## 🎯 Objectives
- 📍 Analyze the **distribution** of 5G deployments across India.
- 🗺️ Use **geospatial techniques** to extract deployment insights.
- 🏆 Predict the **best telecom operator** based on a user’s location using ML models.
- 🔗 Identify **key connectivity nodes** using graph centrality measures.

## 🛠️ Data Preprocessing
✅ Filtered out **non-Indian deployments**.
✅ Removed **non-relevant operators** (Vodafone Idea does not have 5G yet).
✅ Standardized **operator names** for consistency.
✅ Used **state-level GeoJSON files** to remove outliers.

## 🔗 Graph Construction
- **🖇️ Edges:** Created based on a **10 km communication radius** between deployments of the same operator.
- **📊 Graph Centrality Measures:**
  - 🔥 **Degree Centrality:** Identifies **highly connected nodes**.
 
  - ![image](https://github.com/user-attachments/assets/9acd8581-b893-4cde-8112-065be25ba83f)

  - 🏃 **Closeness Centrality:** Measures **accessibility** of nodes.
 
  - ![image](https://github.com/user-attachments/assets/a9ef0f19-adc2-4338-ae83-30943e9cc3b1)


  - 🌉 **Betweenness Centrality:** Determines nodes acting as **bridges**.
 ![image](https://github.com/user-attachments/assets/16d7d967-e7d4-4017-b950-a588c0609feb)


  - 🌎 **Eigenvector Centrality:** Highlights **influential nodes** in the network.
 
  - ![image](https://github.com/user-attachments/assets/d8a62c08-3634-4e9c-9bef-5426b944cddb)


## 🤖 Machine Learning Models
### 1️⃣ K-Nearest Neighbors (KNN) 🔍
- Predicts the **best 5G operator** based on user location.
- Uses a **5 km radius** to determine the **nearest deployments**.

![image](https://github.com/user-attachments/assets/cf878e21-2cbe-4d8c-85d9-735d54796df0)


### 2️⃣ Unsupervised Learning 📈
- **K-Means Clustering**: Groups deployments based on **location**.

- ![image](https://github.com/user-attachments/assets/22461634-d34a-49b1-9695-c072348ef699)

- **Gaussian Mixture Model (GMM)**: Allows **overlapping clusters**, useful for dense regions.

- ![image](https://github.com/user-attachments/assets/c39e4a4c-99c1-4dc6-acec-2245de023539)


### 3️⃣ Graph Convolutional Network (GCN) 🌐
- Predicts the **operator** based on geospatial features.
- Utilizes **spatial relationships** between deployments.
- **KNN outperforms GCN** due to complex dataset criteria.

-![image](https://github.com/user-attachments/assets/c3a5b329-da51-4134-8e00-553f5adc8cad)

-
- ![image](https://github.com/user-attachments/assets/df316dba-3f5f-454e-98d1-7388d0cb1f3e)


## 🔎 Key Findings
✔️ **5G deployments are concentrated in urban & IT hub areas** (e.g., Chennai & Kolkata outskirts).
✔️ **Airtel has stronger connectivity in Kerala**, whereas **Reliance Jio dominates Kolkata**.
✔️ **Centrality analysis** reveals **critical deployment hubs** influencing network structure.

## 🛠️ Tools & Technologies
- **💻 Programming Language:** Python 🐍
- **🛠️ Development Platforms:** Jupyter Notebook, Google Colab
- **📚 Libraries Used:**
  - 🏗️ `pandas` (Data Processing)
  - 📊 `matplotlib`, `plotly`, `folium` (Visualization)
  - 🔗 `networkx` (Graph Analysis)
  - 🤖 `tensorflow`, `sklearn` (Machine Learning)
  - 📝 `json` (Data Parsing)

## 🏁 Conclusion
🚀 With the help of **ML models & graph centrality analysis**, we successfully predicted the **best network provider** for each user.
📡 **Clustering techniques** helped analyze **deployment patterns**.
📊 **Graph centrality measures** provided insights into **network structure & connectivity**.

## 🔮 Future Enhancements
💡 **Expand dataset** to include **real-time network performance metrics**.
📡 **Incorporate additional telecom operators** as they roll out 5G.
📈 **Improve GCN model accuracy** using advanced graph architectures.



