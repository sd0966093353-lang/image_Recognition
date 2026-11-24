# Ollama-Groq 視覺分析助手 (Vision Analysis Assistant)

這是一個基於 **Streamlit** 開發的多模型影像辨識與視覺分析網頁應用程式。使用者可以上傳圖片並自訂提示詞（Prompt），自由切換 **本機 Ollama**、**Ollama Cloud** 與 **Groq API** 三種推論引擎進行影像內容解析。

## ✨ 功能特色

- **多平台模型切換**：支援三種不同的視覺語言模型（VLM）後端：
  - **Ollama (Local)**：使用本機部署的 `llava:13b` 模型，無需連網即可進行隱私推論。
  - **Ollama-Cloud**：連線至 Ollama 官方雲端服務，呼叫 `gemma4:31b-cloud` 進行高精度分析。
  - **Groq API**：透過 Groq 高速推論引擎呼叫 `qwen/qwen3.8-27b` 模型。
- **智慧影像前處理**：
  - 自動修正手機或相機拍攝照片的 EXIF 旋轉方向問題。
  - 自動將 RGBA / 灰階等格式轉換為標準 RGB，確保 Base64 JPEG 編碼穩定不報錯。
- **彈性提示詞與並排檢視**：內建觀光客視角繁體中文預設提示詞，支援自訂指令，並以左右雙欄並排顯示原圖與分析結果。

---

## 🛠️ 環境需求與安裝

### 1. 複製專案並安裝依賴套件
```bash
git clone [https://github.com/你的帳號/你的專案名稱.git](https://github.com/你的帳號/你的專案名稱.git)
cd 你的專案名稱
pip install -r requirements.txt