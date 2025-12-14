# 💰 Expense Tracker (簡易費用追蹤工具)

這是一個基於 Python 的簡單的費用追蹤工具。它結合了 tkinter 圖形介面與 matplotlib 數據視覺化，讓使用者能輕鬆新增、編輯、刪除收支紀錄，並即時透過圓餅圖查看消費分佈。

## ✨ 主要功能

### 📝 資料管理
* 新增消費紀錄（日期、金額、類別、備註）。
* 編輯現有紀錄。
* 刪除紀錄。
* 資料自動保存於 expenses.csv。

### 📊 視覺化分析
* 即時圓餅圖顯示消費類別比例
* 自動將小比例的消費類別合併顯示為「其他」，保持圖表簡潔。
* 支援中文顯示。
* 即時顯示總消費金額。

### 🔍 進階篩選
* 可依照「月份」（如 2025-12）或「消費類別」進行篩選。
* 篩選後，下方的列表與右側的圓餅圖會同步顯示篩選後的結果。

---

## 📂 檔案結構

本專案採用模組化設計，由三個主要 Python 檔案組成：

* `main.py`：**主程式入口**。負責建立 GUI 介面，處理使用者操作（按鈕、輸入框），並呼叫其他模組。
* `input.py`：**資料處理模組 (Model)**。負責後端邏輯，包含 CSV 檔案的讀寫、日期格式驗證、以及資料的增刪改實作。
* `output.py`：**視覺化模組 (View)**。負責讀取數據並使用 Matplotlib 繪製圓餅圖，同時處理中文字型設定。

---

## ⚙️ 安裝與設定

### 1. 環境需求
請確保你的電腦已安裝 [Python](https://www.python.org/downloads/)。

### 2. 安裝依賴套件
本專案使用 `tkinter` (Python 內建標準庫) 與 `matplotlib` (外部庫)。你需要手動安裝 matplotlib：

```bash
pip install matplotlib
```

---

## 🚀 如何運行

雖然專案分為多個模組，但你只需要執行主程式即可。

1. 開啟終端機 (Terminal) 或命令提示字元 (CMD)。

2. 切換到專案資料夾目錄。

3. 執行以下指令：

```bash
python main.py
```
⚠️ 注意：請勿直接執行 input.py 或 output.py，它們是作為模組被 main.py 呼叫使用的。

---

## 📖 操作說明

### 1. 新增記錄 (Add)
* 填寫 日期（YYYY-MM-DD）、類別、金額、備註（可選）
* 點擊「Add New」

### 2. 編輯記錄 (Edit)
* 在下方表格中選取一筆記錄
* 點擊「Load Selected」將資料載入輸入欄位
* 修改後點擊「Update Selected」

### 3. 刪除記錄 (Delete)
* 在表格中選取一筆記錄
* 點擊右上角「Delete Selected」按鈕（會跳出確認視窗）

### 4. 過濾顯示 (Filter)
* 輸入月份（YYYY-MM）或類別（完全符合）
* 點擊「Apply Filter」
* 圓餅圖與表格會即時更新為過濾結果
* 點擊「Clear Filter」恢復顯示全部

### 5. 雙擊快速編輯
* 在表格中雙擊任一列，等同於「Load Selected」

---

## 📸 操作介面及統計圓餅圖
![App Screenshot](path/to/image.png)
"C:\Users\renee\Pictures\Screenshots\螢幕擷取畫面 2025-12-14 104925.png"



