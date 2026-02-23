# ITG-EIP
ITG-EIP專為團隊成員方便管理團隊事務得軟體


# ITG-EIP 企業資訊入口系統

ITG-EIP 是一套基於 PyWebView 的桌面端企業資訊管理系統，搭配獨立部署於 VPS 的 Flask 後端 API，提供員工登入、專案檔案管理、團隊即時通訊、會計帳務及系統設定等功能。

---

## 系統架構

```
用戶端 (Windows)                          伺服器端 (VPS)
┌──────────────────────┐                 ┌──────────────────────────┐
│  main.py (PyWebView) │  ── HTTP ──>   │  server.py (Flask)        │
│  index.html          │                 │  Port: 6096              │
│  styles.css          │                 │                          │
│  app.js              │  <── JSON ──   │  data/                    │
│  favicon.ico         │                 │                          │
│  eip_settings.json   │                 │                          │
└──────────────────────┘                 │  ├── discord.env         │
                                         │  ├── accounting/         │
                                         │  ├── projects/           │
                                         │  │   ├── project1/       │
                                         │  │   └── project2/       │
                                         │  └── chats/              │
                                         └──────────────────────────┘
```

---
