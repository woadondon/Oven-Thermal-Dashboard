# 🏭 Industrial Oven Thermal-Fluid & MEK Extraction Dashboard
*(工業烘箱流固耦合模擬與 MEK 氣體排除視覺化儀表板)*

![Python](https://img.shields.io/badge/Python-3.9+-blue.svg)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?logo=streamlit&logoColor=white)
![CFD](https://img.shields.io/badge/Ansys-Fluent-F3CD00?logo=ansys&logoColor=black)

## 📌 專案背景 (Motivation)
在工業烘箱的乾燥過程中，高溫風嘴 (Inlet) 對移動中的固體進行加熱。然而，傳統烘箱內部容易產生渦流，導致 MEK (甲基乙基酮) 溶劑蒸氣滯留，嚴重影響產品良率與安全性。
本專案結合 **Ansys Fluent CFD 模擬** 與 **Python Streamlit 網頁框架**，開發出一套高保真度 (High-fidelity) 的互動式分析工具，能快速讀取 CFD 穩態分析 (Solid Motion) 的原始數據，並視覺化展示流場優化成果。

## 💡 核心工程突破 (Engineering Highlights)
* **Solid Motion 熱傳分析：** 精準模擬固體受風嘴持續加熱，提取從入口至出口的穩態溫度變化曲線，保留最真實的熱流擾動細節。
* **屋脊結構設計 (Roof-ridge Structure)：** 針對 MEK 滯留痛點，原創設計屋脊型流道，成功消除內部渦流，大幅提升溶劑抽離效率。

## 🚀 儀表板功能 (Dashboard Features)
1. **📂 原始數據無損匯入：** 一鍵解析 Fluent 輸出的高密度溫度分佈 `.csv` 檔，確保零數據遺失。
2. **📈 極致細節探索 (Interactive Plotting)：** 支援滑鼠懸停顯示精確節點數值 (Hover Tooltips)，並可自由框選、無段放大局部溫度曲線，深入分析微觀熱流現象。
3. **📊 流場優化前後對比 (A/B Test)：** 並排顯示 3D 流場/溫度分佈圖，直觀展示「傳統設計」與「屋脊結構設計」對 MEK 滯留消除的巨大差異。
4. **疊圖交叉比對：** 支援多組 Case 數據同時匯入與疊加，精準量化設計變更對固體升溫歷程的影響。

## 📸 介面展示 (Demo)
*(請在此處放上你開發完的 Streamlit 網頁截圖或操作 GIF)*

## 🛠️ 如何執行 (Quick Start)
```bash
# 1. 安裝所需套件
pip install streamlit pandas plotly

# 2. 啟動儀表板
streamlit run app.py
