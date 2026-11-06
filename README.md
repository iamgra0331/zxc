# 拔河賽自動賽程表 - 多人即時同步系統

本專案提供拔河賽自動賽程表及跨裝置多人即時同步功能，支援手機、平板與大螢幕即時顯示戰況與比分更新。

## 功能特點

- **多組別賽程管理**：支援高一、高二等多個年級與隊伍名單設定。
- **多人即時同步**：後端使用 Python 內建 HTTP 伺服器處理即時賽況同步與資料持久化 (`tournament_data.json`)。
- **外網連線支援**：支援搭配 Cloudflare Tunnel (`cloudflared`) 進行行動網路與外網穿透，跨網路環境亦可即時查看。
- **一鍵啟動**：提供 Windows 批次檔 (`啟動多人同步伺服器.bat`)，點擊即可自動啟動伺服器並開啟瀏覽器。

## 檔案說明

- `index.html`：賽程表前端互動介面。
- `server.py`：Python 同步伺服器核心。
- `tournament_data.json`：賽程與對戰紀錄資料檔。
- `啟動多人同步伺服器.bat`：Windows 快速啟動腳本。
- `config.yml`：Cloudflare Tunnel 設定檔。

## 使用方式

1. 確保已安裝 Python 3.x。
2. 雙擊執行 `啟動多人同步伺服器.bat`，或在終端機執行：
   ```bash
   python server.py
   ```
3. 瀏覽器將自動開啟 `http://localhost:8080`。
