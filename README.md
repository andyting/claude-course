# Claude Certified Architect – Foundations 備考教材

**Claude Certified Architect – Foundations** 認證考試的中文備考課程，涵蓋全部 5 個 Domain、30 個 Task Statement 的互動式 HTML 教材。

---

## 關於這份教材

本課程以 Anthropic 官方考試指南（Exam Guide PDF）為唯一內容來源，針對每個 Task Statement 製作一份 HTML 教學頁面，幫助學員將考綱知識點轉化為「遇到真實問題時能直接套用」的實戰能力。

考試格式為選擇題（1 個正確答案 + 3 個 distractors），所有題目都基於 6 個生產情境（Scenario）出題。本教材的設計完全對齊這個出題邏輯。

---

## 課程內容

### 5 個 Domain 與 30 個 Task

| Domain | 名稱 | Tasks | 比重 |
|--------|------|-------|------|
| 1 | Agentic Architecture & Orchestration | 1.1–1.7 | 27% |
| 2 | Tool Design & MCP Integration | 2.1–2.5 | 18% |
| 3 | Claude Code Configuration & Workflows | 3.1–3.6 | 20% |
| 4 | Prompt Engineering & Structured Output | 4.1–4.6 | 20% |
| 5 | Context Management & Reliability | 5.1–5.6 | 15% |

### 6 個考試 Scenario

正式考試會從以下 6 個情境隨機抽 4 個，每道題都掛在某個情境下出題：

| # | 情境名稱 | 核心技術 |
|---|---------|---------|
| 1 | Customer Support Resolution Agent | Claude Agent SDK、MCP tools |
| 2 | Code Generation with Claude Code | Claude Code、CLAUDE.md、slash commands |
| 3 | Multi-Agent Research System | Coordinator/Subagent、多代理協作 |
| 4 | Developer Productivity with Claude | Built-in tools、MCP server |
| 5 | Claude Code for CI/CD | `-p` flag、`--output-format json`、CI 整合 |
| 6 | Structured Data Extraction | `tool_use` + JSON schema、validation |

---

## 每份教材的結構

每個 Task HTML 頁面包含以下區塊：

### 官方考綱原文
直接引用 Exam Guide 中該 Task 的 **Knowledge of** 與 **Skills in** 條列，作為學習覆蓋率的對照參考。

### 本題情境（Scenario）
說明這個 Task 對應到哪個考試情境，讓抽象知識點有具體的生產環境脈絡。

### 一句話主軸
用一句話抓住整個 Task 的核心，作為學習的錨點。

### 知識點 / 技能點（含觸發情境）
每個知識點與技能點標題下方都有一個**紫色觸發情境框**，說明：

> 「你在什麼實際情況下會需要用到這個知識？」

幫助學員建立「問題 → 知識」的連結，而非被動記憶條文。

### 雙語術語標注
關鍵英文技術術語在中文說明中同步標注英文原文，例如：
- `orchestration（編排）`
- `anti-pattern（反模式）`
- `few-shot（少樣本）`
- `conversation history（對話歷史）`

### 代碼範例（✅ 正解 / ❌ 反模式）
每個知識/技能點附有可複製的 Python 代碼，對比正確做法與常見錯誤。

### 記憶骨架
頁尾整合摘要，濃縮整個 Task 最需要記住的核心邏輯。

### 考試情境題（3 題）
每個 Task 末尾附 3 道模擬考題：
- **題目與選項**：英文，格式與正式考試相同（生產情境 + 四個選項）
- **解析**：中文，說明正確答案的理由，以及每個錯誤選項的問題所在

全課程共 **90 道**模擬題，涵蓋全部 5 個 Domain。

---

## 檔案結構

```
Claude 課程/
├── index.html                    # 課程首頁（所有 Task 索引）
├── HTML教材/
│   ├── 考試介紹_Overview.html    # 考試格式說明
│   ├── Task_1.1_教學.html        # Domain 1: Agentic Architecture
│   ├── Task_1.2_教學.html
│   ├── ...（共 30 個 Task）
│   └── Task_5.6_教學.html
└── instructor-...Exam+Guide.pdf  # Anthropic 官方考試指南（原始來源）
```

---

## 使用方式

直接在瀏覽器開啟 `index.html` 即可進入課程首頁，點選各 Domain 下的 Task 進入對應教材。所有頁面為純靜態 HTML，無需伺服器。

### 建議學習流程

1. 先讀**一句話主軸**，建立整個 Task 的核心概念
2. 逐節閱讀知識點/技能點，遇到觸發情境時思考：「如果是我，我會怎麼處理？」
3. 閱讀代碼範例，理解 ✅ 與 ❌ 的差異
4. 完成頁尾的 3 道考試情境題，先作答再展開解析
5. 複習記憶骨架，確認核心邏輯已內化

---

## 技術規格

- 純靜態 HTML + CSS + 少量 vanilla JavaScript（複製代碼按鈕）
- 繁體中文介面，關鍵術語保留英文原文並加中文標注
- 考試題使用 `<details>/<summary>` 折疊，避免不小心看到答案
- 支援行動裝置瀏覽（響應式排版）

---

## 關於考試

- **形式**：全選擇題，每題 1 個正確答案
- **及格分數**：720 / 1000（scaled score）
- **考試時間**：依 Anthropic 官方安排
- **目標對象**：具備 6 個月以上 Claude API / Agent SDK / Claude Code 實際開發經驗的 solution architect

詳細考試資訊請參考 `instructor-...Exam+Guide.pdf`。
