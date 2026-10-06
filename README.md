# 🏔️ Comprehensive Financial Scenarios & Risk Bounds Pre-Forecaster
> **用蒙地卡羅隨機漫步模型，解構企業「成本與營收波動」的不確定性怪山。**
> *A Corporate Monte Carlo Simulation System for Stochastic Cash Flow Stress Testing.*

---

## 💼 商業痛點與戰略價值 (Business Context & Strategic Value)

在多變的市場環境中，單一維度的財務預估（點預測）往往隱藏了致命的盲點。本專案為決策者提供了一個**「由歷史流水帳驅動的平行宇宙測試沙盒」**。

本系統的核心商業邏輯在於：
1. **方向與斜率 (Drift)**：由歷史平均或操之在己的策略設定，決定公司前進的方向。
2. **風險與肉墊 (Volatility)**：由歷史波動率決定骰子的重量，利用連續 12 個月的**跨期複利疊加（隨機漫步 Random Walk）**，將不確定性擴散為直觀的**「帶狀預測雲」**。
3. **安全邊際 (Stress Testing)**：利用 P10 悲觀防線，幫助經理人精準進行財務壓力測試，提前鎖定現金流轉折點與緊急週轉金的防禦水位。

---

## 🛠️ 核心功能亮點 (Key Features)

* **數據靈魂自動擷取**：自動從過去一年的歷史流水帳中計算營收與成本的月增率標準差。
* **高階情境並聯對比**：支援以逗號分隔連續輸入多組策略（如：持平 `0`、進攻 `0.02`、衰退 `-0.01`），一鍵生成跨宇宙對比。
* **頂級財務視覺化 (CFO Style)**：隱去刺眼的數據標記，純粹以**「同色細虛線邊界」**與**「高通透半透明陰影」**在同一張圖上堆疊不同策略的利潤區間，層次分明、絕不混亂。
* **網頁級動態交互 (Interactive UX)**：基於 `Plotly` 引擎，支援游標聯動提示（Unified Hover Tooltips）、區域框選放大、以及點擊右側圖例動態隱藏/顯示特定情境。

---

## 💻 快速開始 (Quick Start)

### 1. Prerequisites (依賴環境)
確保您的環境已安裝以下核心數據科學套件：
```bash
pip install pandas numpy plotly
```

### 2. Execution (運行預測)
在您的 Jupyter Notebook 或 Python 環境中執行主程式 `financial_forecast.py`，系統將啟動互動式終端介面：

```text
💬 Please enter multiple drift rates (e.g., 0, 0.02, -0.01): 0, 0.03, -0.02
```

執行後，系統將自動彈出網頁級動態圖表 `Comprehensive Financial Scenarios & Risk Bounds Comparison`。

---

## 📊 決策判讀指南 (Executive Interpretation)

* **全線 P50 (Expected Median Line)**：代表扣除震盪後機率最高的常態路徑，作為年度預算與編列的黃金基準。
* **全線 P10 (Pessimistic Risk Boundary)**：代表最極端的 10% 寒冬情境。決策者應檢視此防線是否跌破損益兩平點，並以此計算應準備的防禦性現金頭寸。
* **全線 P90 (Opmistic Boundary)** ：代表最極端的 10% 蓬勃市場，決策者應將此線視為最大可能結果，而不能直接當作財務預測。
* **喇叭狀擴散 (The Uncertainty Cone)**：隨著時間往 M+12 推移，區間帶越寬，代表時間放大了隨機誤差，提醒經理人近場預測可信度高，遠場預測需保持動態微調。

---

## 📝 版本與授權 (License)
* **Author**: 頂擊經理人協作小組
* **Version**: v1.0.0 (Pre-Release Masterpiece)
* **License**: MIT License
