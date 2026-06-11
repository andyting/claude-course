# Claude 課程教材 — 索引頁與部署說明

`index.html` 是整套教材的入口。它用**相對路徑**連到 `HTML教材/` 裡的 31 個檔案，
所以**本地打開**和**放上網路**完全一樣，不需要改任何程式碼。

---

## 一、在本地電腦看（最簡單，零設定）

直接用瀏覽器打開 `index.html` 就好：

- **macOS**：在 Finder 對 `index.html` 按右鍵 →「打開檔案的應用程式」→ 選 Chrome / Safari。
  或直接 double-click。
- 也可以把 `index.html` 拖進已經開著的瀏覽器視窗。

打開後點任一張 Task 卡片，就會跳到該章節的教學頁；左上角按瀏覽器「上一頁」即可回到索引。

> 重點：`index.html` 必須和 `HTML教材/` 資料夾**放在一起**（同一層）。
> 只要不把這兩者分開，連結就不會壞。

---

## 二、放上公開網路

以下兩種都免費，連結都用相對路徑所以「本地能跑＝上網能跑」。

### 方案 A：Netlify Drop（最快，免帳號也能試，3 分鐘）

1. 打開 https://app.netlify.com/drop
2. 把整個 **`Claude 課程`** 資料夾**直接拖進**網頁中央的虛線框。
3. 等它上傳完，Netlify 會給你一個公開網址（像 `https://random-name.netlify.app`）。
4. 把網址分享給別人就能看。

> 想要固定、好記的網址或之後能更新內容，註冊一個免費 Netlify 帳號即可。
> 之後要更新，只要重新拖一次資料夾覆蓋。

### 方案 B：GitHub Pages（適合長期維護、版本控管）

需要一個 GitHub 帳號（免費）。

1. 到 https://github.com 登入 →「New repository」建一個新 repo，
   例如命名 `claude-course`，設為 **Public**，建立。
2. 進到 repo 頁面 →「Add file」→「Upload files」→
   把 `index.html`、`HTML教材/` 整個資料夾、`logo.png` 等一起拖上去 → Commit。
3. repo 上方 **Settings** → 左側 **Pages**。
4. 「Build and deployment」的 Source 選 **Deploy from a branch**，
   Branch 選 **main** / 資料夾選 **/(root)** → Save。
5. 等 1～2 分鐘，Pages 頁面上方會出現你的網址：
   `https://你的帳號.github.io/claude-course/`
6. 打開那個網址就是你的線上課程首頁。

> 之後要更新內容：在 repo 裡重新上傳改過的檔案並 Commit，
> Pages 會自動重新發佈（約 1 分鐘生效）。

---

## 三、上傳時要包含哪些東西

無論哪個方案，請確保這些一起上傳、且維持原本的資料夾結構：

```
Claude 課程/
├── index.html          ← 入口（首頁）
├── HTML教材/            ← 31 個教學頁，index 靠相對路徑連到這裡
│   ├── 考試介紹_Overview.html
│   ├── Task_1.1_教學.html
│   └── ...（其餘 Task）
└── logo.png            ← 若教材頁面有引用到圖檔，一併上傳
```

`_archive/` 是舊備份，**不需要**上傳。

---

## 四、常見問題

**Q：點卡片出現「找不到檔案 / 404」？**
A：代表 `index.html` 和 `HTML教材/` 被分開了，或上傳時漏了 `HTML教材/` 資料夾。
把兩者放回同一層即可。

**Q：中文檔名在網路上會有問題嗎？**
A：Netlify 與 GitHub Pages 都支援中文檔名與網址，可正常運作。若想更保險，
也可日後把檔名改成英數（但改名後 `index.html` 裡的連結要一起更新）。

**Q：可以加密碼、只給特定人看嗎？**
A：GitHub Pages 公開 repo 是全公開的。要私密存取，Netlify 付費方案或
其他平台（如 Cloudflare Pages + Access）才支援密碼保護。
