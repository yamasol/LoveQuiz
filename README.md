# LoveQuiz

一個純靜態的互動小網站集合，收錄各種戀愛測驗、觀察報告、潮語辭典與生活指南。
每一頁都是獨立的單一 HTML 檔案（樣式與腳本全部內嵌），不需要打包、不需要安裝任何套件，用瀏覽器打開就能跑。

🔗 **線上瀏覽：** [yamasol.github.io/LoveQuiz](https://yamasol.github.io/LoveQuiz/)

---

## 頁面一覽

### 測驗與觀察

| 頁面 | 檔案 | 說明 |
| --- | --- | --- |
| 楷哲的粉紅泡泡觀察所 | `kaizhe_pink_bubble_love_lab.html` | Q 號戀愛研究計畫，整理日常互動與暈船指數的互動式體驗 |
| 小K 暈船觀察報告 | `Observation.html` | 以第三方視角記錄暈船的各個階段與行為線索 |
| 人生副本診斷室 | `love.html` | 用遊戲副本與騎士精神的比喻，拆解感情與人生課題 |
| 楷哲情感鑑定所 | `loveTest.html` | 「你到底只是朋友還是暈船？」的關係定位測驗 |
| MBTI 深度性格探索 | `mbti.html` | 深入挖掘性格特質與行為傾向的性格測驗 |
| 塔羅心靈測驗 | `tarot_test.html` | 找出決策盲點，抽出屬於自己的命定書 |
| 水煎包生存學 | `bao.html` | 家庭溝通與人格毒舌測驗，用水煎包比喻拆解溝通模式 |
| 通話陪伴衝突紀錄 | `couple_argument.html` | 情侶通話衝突的紀錄與復盤頁面 |
| 人類圖手記 | `humandesign.html` | 從零開始說明人類圖的類型、能量中心與看圖方式 |

### 潮語／成語辭典

| 頁面 | 檔案 | 說明 |
| --- | --- | --- |
| 精緻女孩 | `Exgirl2.html` | 潮語辭典詞條，拆解「真精緻」與「偽精緻」的差別 |
| 輝老鼠 | `Mickey.html` | 潮語辭典詞條，收錄詞義、造句與近反義詞 |
| 舔狗 | `tiangou.html` | 潮語辭典詞條 |
| 外強中乾 | `papertiger.html` | 經典四字成語詞條，說解本義、引申義與辨析提醒 |

### 閱讀筆記

| 頁面 | 檔案 | 說明 |
| --- | --- | --- |
| 慣習．七大資本 | `habitus-seven-capitals.html` | 談階級差異與七種資本的閱讀筆記 |
| 箭還插在身上 | `poison-arrow_2.html` | 《中部》第 63 經・鬘童子小經（毒箭之喻）的白話導讀 |

### 生活指南

| 頁面 | 檔案 | 說明 |
| --- | --- | --- |
| 板橋牛肉麵指南 | `noodle.html` | 板橋在地牛肉麵店家推薦與比較 |
| 一次認識好市多 | `costco.html` | Costco 商業模式與賣場動線的互動圖鑑 |
| 吃什麼選擇器 | `Gemini_eat.html` | 拯救選擇困難症的隨機推薦工具 |
| 選擇困難症救援中心 | `chatGPT_eat.html` | 另一個版本的「今天要吃什麼」推薦器 |

> `index.html` 是全站導覽頁，目前只列出部分頁面；新增頁面後記得回頭補上卡片。

---

## 專案結構

```
LoveQuiz/
├── index.html          # 全站導覽頁（卡片式選單）
├── *.html              # 各個獨立頁面，樣式與 JS 全部內嵌
├── costco.png          # 頁面用圖片素材
├── protein.png
├── 阿主.jpg
├── 阿派.JPG / 阿派.png
└── 809703510.174403.mp4
```

## 技術說明

- 純 HTML + CSS + 原生 JavaScript，**沒有框架、沒有建置流程、沒有相依套件**
- 中文以 `lang="zh-Hant"` 標記，字型優先使用 Noto Sans TC / 微軟正黑體
- 以 CSS 變數（`--bg`、`--ink`、`--accent` 等）管理配色，方便單頁調整主題
- RWD：導覽頁在 760px / 480px 兩個斷點分別切換為兩欄與單欄
- 透過 GitHub Pages 部署，推上 `main` 分支即自動更新

## 本機執行

直接用瀏覽器打開 `index.html` 就可以，或啟一個簡易伺服器：

```bash
git clone https://github.com/yamasol/LoveQuiz.git
cd LoveQuiz
python3 -m http.server 8000
# 開啟 http://localhost:8000
```

## 新增一頁

1. 在根目錄建立新的 `.html`（建議沿用既有頁面的 `:root` 變數與版面結構）
2. 在 `index.html` 對應分類的 `.grid` 裡加上一張卡片：

```html
<a class="card" href="your_page.html">
  <h3>頁面標題</h3>
  <p>一句話說明這頁在做什麼。</p>
  <span class="go">進入 →</span>
</a>
```

3. commit 並 push 到 `main`，GitHub Pages 會自動部署

## 備註

站內內容多為娛樂與自我探索性質，測驗結果純屬趣味，請勿當作專業心理、醫療或命理建議。
