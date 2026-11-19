# AI 工具包｜基本包：從 0 到上線

這不是教學，是一個**工具包**。

裡面有 3 個工具，照順序裝：裝完，你的電腦上就有一個 AI 會認得你、記得做過什麼、改壞了回得去的工作台；做出來的東西，也能放上網給別人用。

這套做法由一位非工程師的餐飲業老闆實測整理：他用同一套方法經營十家店的日常營運。你拿到的是通用版，跟他的行業無關，任何工作都能用。

## 你只要做三件事（Mac、Windows 都一樣）

1. **在電腦上開一個新資料夾**，名字隨你（例如 `我的AI`）。這個資料夾就是你的「家」，以後所有東西都住在這裡。
2. **打開 Claude 桌面版**（或 Codex 桌面版），開新工作時**選這個資料夾**。
3. **把這個網址貼給 AI**，然後說：

   > 照這個帶我裝工具。我是新手。

AI 會把工具包抓進你的資料夾，然後一步一步陪你裝。過程中畫面會跳出「要不要允許」的詢問，AI 會先跟你講它要做什麼，你按允許就好。

## 給 AI：使用者剛把這個網址貼給你

你現在開著的資料夾，就是使用者的「家」（總基地）。照這三步開工：

1. **把工具包原文抓進這個資料夾的 `工具包/` 裡。** 要原封不動的檔案，**不要用會摘要內容的網頁讀取工具**（裡面的家規範本要照抄，摘要會漏）。一行一個指令執行；Windows 把 `curl` 換成 `curl.exe`（PowerShell 的 `curl` 是別的東西）：

   ```text
   curl -fsSL --create-dirs -o 工具包/START_HERE.md https://raw.githubusercontent.com/weifu0716/ai-toolkit/main/START_HERE.md
   curl -fsSL --create-dirs -o 工具包/tools/0_環境.md https://raw.githubusercontent.com/weifu0716/ai-toolkit/main/tools/0_%E7%92%B0%E5%A2%83.md
   curl -fsSL --create-dirs -o 工具包/tools/1_基地.md https://raw.githubusercontent.com/weifu0716/ai-toolkit/main/tools/1_%E5%9F%BA%E5%9C%B0.md
   curl -fsSL --create-dirs -o 工具包/tools/2_上線.md https://raw.githubusercontent.com/weifu0716/ai-toolkit/main/tools/2_%E4%B8%8A%E7%B7%9A.md
   ```

   網址裡的中文已經編碼過，照貼就好（有些 Windows 終端機遇到網址裡的中文會抓不到）。抓完確認 4 個檔都在、中文正常。
2. **讀 `工具包/START_HERE.md`，照它做。**
3. **家就是現在這個資料夾。** 不要另外在桌面或別處建資料夾。

## 三個工具

| # | 工具 | 裝完你多了什麼 |
|---|---|---|
| 0 | 環境 | 一台能跟 AI 一起做事的電腦（照上面三件事做完，這個就已經好了） |
| 1 | 基地 | 一個會記憶、有地圖的工作台：AI 進門就認得你、知道你在做哪些事各做到哪、做完一件事自己收尾、改壞了回得去，也清楚哪些錯不能犯 |
| 2 | 上線 | 你的第一個「有網址的作品」，別人的手機打得開；要存資料、要登入的也一次接好（Firebase） |

順序照 0 → 1 → 2。第一次來，裝好 1 就可以開始做你的第一個專案；做出東西、想給別人用的時候再裝 2。

## 都裝完，你的 AI 會這樣跟你工作

開一個對話 → 它先讀家規、記憶、地圖、你要做的那個專案 → 做事，被你糾正就問要不要記 → 做完自己寫紀錄、更新進度、存一版 → 東西要給別人用就放上網。碰到錢、刪檔、對外發送，它會先停下來講清楚風險再問你。你不用記得提醒它任何一步。

## 延伸工具（需要再拿）

基本包之外的工具，每一個都是獨立的 repo。需要哪個，就把那個網址貼給你的 AI，說「照這個幫我裝」。

| 工具 | 用途 |
|---|---|
| [obsidian-knowledge-base](https://github.com/weifu0716/obsidian-knowledge-base) | 用 Obsidian 看你的筆記：做完事 AI 把做法、決定、踩過的坑整理進去，瀏覽器看到好文章一鍵存進來 |
| [speak-human-tw-setup](https://github.com/weifu0716/speak-human-tw-setup) | 去 AI 味的校稿員：要給別人看的文字先抓出 AI 腔、中國用語、半形標點 |
| [website-to-desktop-app](https://github.com/weifu0716/website-to-desktop-app) | 把做好的網站變成可以裝在電腦上的 App |
| [namecard-crm](https://github.com/weifu0716/namecard-crm) | 拍名片 → AI 讀圖入庫 → 手機一鍵導航 |
| [employee-island](https://github.com/weifu0716/employee-island) | 把上班表現變成一座島的員工遊戲化做法 |

## 常見問題

**要花錢嗎？** 工具包本身免費。AI 要另外訂閱：Claude 桌面版選資料夾工作（Claude Code）需要付費方案；ChatGPT 的 Codex 各方案能用多少，以官方當下說明為準。上線用的 Firebase 有免費方案，大部分第一個作品用免費方案就夠；需要付費功能時，AI 會先講清楚怎麼計費、最壞會花多少、怎麼設上限，你同意才開。

**我完全不會程式，可以嗎？** 可以，這套就是為此設計的。你負責回答問題和驗收，施工是 AI 的事。

**只有網頁版 Chat、沒有 Claude Code／Codex？** 從工具 0 開始，網頁版 AI 就能陪你把環境裝起來。

**我的 AI 抓不到網址？** 按這頁上方綠色 `Code` → `Download ZIP`，解壓縮後把整包放進你的資料夾、改名叫 `工具包`，再跟 AI 說「讀 工具包/START_HERE.md 帶我裝」。

**以後工具包更新了怎麼辦？** 把這個網址再貼給 AI 一次，說「更新工具包」。它會重新抓、對照你已經裝的，只補新的部分。

**我以前裝過舊版的「知識庫」「說人話」？** 照常可以用，不用重裝。這兩個工具現在搬到上面的延伸工具，以後要更新就去那邊。

## 授權

MIT。可以自由使用、改寫與分享。
