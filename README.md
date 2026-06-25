# 🚀 Edge AI 工業級多目標考勤與高精度情緒分析系統

[![WebGPU Supported](https://img.shields.io/badge/WebGPU-Accelerated-emerald?style=flat-square)](https://developer.mozilla.org/en-US/docs/Web/API/WebGPU_API)
[![ONNX Runtime](https://img.shields.io/badge/ONNX_Runtime-v1.16+-blue?style=flat-square)](https://onnxruntime.ai/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=flat-square)](https://opensource.org/licenses/MIT)

一個純前端、零後端（Zero-Backend）的邊緣運算（Edge AI）智能解決方案。結合 **Face-API.js** 的人臉特徵庫與 **FERPlus (INT8 量化優化版)** 卷積神經網路模型，實現網頁端高精度多目標追蹤、考勤時長統計，並透過 **Chart.js** 實時視覺化每位成員的多維度情緒分佈圓餅圖。

---

## ✨ 核心亮點

*   **⚡ 網頁端硬體加速 (WebGPU/WebGL/WASM)**：自動調用本地 GPU/NPU 算力，告別高昂的雲端伺服器 API 費用。
*   **📦 本地 INT8 量化大模型**：成功適配 `emotion-ferplus-12-int8.onnx`。模型體積大幅壓縮 75%（約 8MB~11MB），完美契合 GitHub 檔案限制，且具備極佳的邊緣推理速度。
*   **📊 實時精細化情緒百分比**：擺脫單一標籤，即時動態計算全情緒矩陣（中性、愉悅、疲憊、嚴肅、緊張、驚訝、反感、輕蔑）的機率分佈。
*   **📈 互動式動態圓餅圖 (Live Pie Chart)**：點擊用戶標籤即可彈出 Chart.js 莫蘭迪色系圖表，數據以 150ms 頻率背景無感刷圖，絕不卡頓視訊幀率。
*   **🤝 特徵動態融合與手動合併**：自動追蹤過渡特徵防止因轉頭誤判；提供視覺化名冊管理，支援手動合併重複標籤，時長與表情歷史數據完美合流。

---

## 📂 檔案目錄結構

請確保你的 GitHub 倉庫根目錄包含以下核心檔案：

```text
├── index.html                       # 系統主程式 (包含 HTML, CSS, JS 邏輯)
├── emotion-ferplus-12-int8.onnx     # 本地 INT8 量化表情大模型 (不可改名)
└── README.md                        # 本說明文件
