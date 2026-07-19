# Research Graph — 公司研究 Graph 工具原型(v20)

線上版:**https://omnis-labs.github.io/hunch-it-demo/graph/**

純靜態、單一 HTML、無後端、無外部請求。丟一個問題,graph 繞著它長出來;
研究 → 觀點 → 交易計畫 → 對答案覆盤,全程可 audit。

核心機制:
- **問題驅動骨架**:parseQuery(公司 × 主題)決定 session 與 ⌖ 核心節點(TSMC 完整劇情 / NVDA / ASML)
- **一切皆節點**:原地展開卡、per-node 持久對話串、reasoning DAG(挑戰證據 → promote 沿依賴邊流動重算下游)
- **觀點機制**:假說 H1–H4 接受/存疑/拒絕 + 風險偏好 → 推導方向/信念/進場框架 — 同一題,不同人,不同計畫
- **交易計畫閉環**:falsifier → 出場規則、pre-trade 曝險檢查、法說會結算對答案 + 校準記分、pre-mortem 一鍵掛哨兵
- **多 session**:同公司不同問題 = 獨立 session(各自存檔、佈局、觀點),INBOX 卡片牆管理
- **Agentic**:🤖 活動 feed、閒置主動建議、供應鏈 graph(邊標業務關係)斷鏈傳播

操作:點節點=展開卡 · 雙擊/⤢=內部圖 · 右鍵=加分析節點 · 拖曳節點=重排(佈局會記住)· ⌂=回首頁

示意數字非即時行情,不構成投資建議。源碼開發於 `ChiShengChen/event-trader` 的 `demo_frontend/`。
