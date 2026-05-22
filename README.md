# 世界能源消耗資料分析期末專題

## 專題主題

世界能源消耗資料分析：全球能源轉型趨勢與台灣能源結構挑戰  
World Energy Consumption Analysis: Global Energy Transition and Taiwan's Energy Structure Challenges

本專題使用 `World Energy Consumption.csv` 分析全球能源消耗、能源結構轉型、再生能源占比、化石燃料依賴、發電碳強度，以及台灣相對於全球與主要國家的能源轉型挑戰。

## 組別與成員

- 課程：資料探勘概論期末專題
- 組別：第 10 組
- 4113053103 林貞伶
- 4111053021 董琦溱
- 指導教授：蔡孟勳 教授

## 資料來源

- 資料集：`World Energy Consumption.csv`
- 來源：Our World in Data - World Energy Consumption Dataset
- 資料範圍：1900-2022
- 資料筆數：22,012 筆
- 欄位數：129 欄
- 國家與地區數：306

## 專案檔案說明

| 檔案或資料夾 | 說明 |
|---|---|
| `World Energy Consumption.csv` | 原始資料集 |
| `energy_analysis_sections_1_to_4_executed.ipynb` | 已執行版 notebook，保留輸出結果、表格與圖表 |
| `key_results.md` | 從 CSV 實際計算出的關鍵數字與資料檢查結果 |
| `figures/` | 所有分析圖表 PNG |


## 圖表清單

圖表皆位於 `figures/` 資料夾。

| 圖檔 | 內容 |
|---|---|
| `fig01_global_primary_energy_trend.png` | World primary energy consumption, 1900-2022 |
| `fig02_global_energy_structure.png` | World energy structure stacked area chart |
| `fig03_world_renewables_share_trend.png` | World renewables share trend, 2000-2022 |
| `fig04_taiwan_vs_world_renewables.png` | Taiwan vs World renewables share |
| `fig05_renewables_share_2022_country_comparison.png` | 2022 renewables share country comparison |
| `fig06_taiwan_vs_world_fossil_share.png` | Taiwan vs World fossil fuel share |
| `fig07_carbon_intensity_2022_country_comparison.png` | 2022 carbon intensity country comparison |
| `fig08_correlation_heatmap.png` | 2022 correlation heatmap |
| `fig09_kmeans_clusters.png` | K-means clusters with Taiwan highlighted |
| `fig10_taiwan_renewables_forecast_2030.png` | Taiwan renewables share linear trend extrapolation to 2030 |

## 分析方法

本專題主要使用以下方法：

- Exploratory Data Analysis, EDA
- 2000-2022 年主要國家比較
- 2022 年橫斷面相關分析
- K-means 分群
- PCA 二維視覺化
- Linear Regression 趨勢外推

K-means 分群前已移除缺失值，並使用 `StandardScaler` 進行標準化。趨勢外推僅作為趨勢參考，不代表精準預測。

## 主要分析對象

- World
- Taiwan
- Germany
- China
- Japan
- United States
- India

## 重要結果摘要

詳細數字請見 `key_results.md`。

- World 2022 再生能源占比：14.214%
- Taiwan 2022 再生能源占比：4.411%
- World 2022 化石燃料占比：81.792%
- Taiwan 2022 化石燃料占比：91.116%
- World 2022 發電碳強度：436.336 gCO2/kWh
- Taiwan 2022 發電碳強度：561.000 gCO2/kWh
- Taiwan K-means cluster：3
- Taiwan 2030 再生能源占比趨勢外推值：3.583%

## 報告主軸

本專題的核心結論是：

全球能源轉型已經開始，但化石燃料仍占主導；台灣再生能源占比低、化石燃料依賴高、發電碳強度偏高，因此需要從政策、技術、產業與社會多面向推動能源轉型。

## 注意事項

- 所有數據皆由 `World Energy Consumption.csv` 實際計算。
- 分析過程不隨意補值；若分析欄位缺失，該分析排除缺失資料。
