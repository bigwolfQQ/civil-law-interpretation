# 📖 民法條文解釋教學講義產生器｜Civil Law Interpretation

![Profile views](https://komarev.com/ghpvc/?username=mjib007&label=Profile%20views&color=4c8eda&style=flat)
[![Stars](https://img.shields.io/github/stars/mjib007/civil-law-interpretation?style=flat&color=yellow)](https://github.com/mjib007/civil-law-interpretation/stargazers)
[![Forks](https://img.shields.io/github/forks/mjib007/civil-law-interpretation?style=flat&color=blue)](https://github.com/mjib007/civil-law-interpretation/network/members)
![AI](https://img.shields.io/badge/AI-Claude%20(Anthropic)-blueviolet)
![Platform](https://img.shields.io/badge/Platform-claude.ai-orange)
![Language](https://img.shields.io/badge/Language-繁體中文-red)
[![License](https://img.shields.io/badge/License-CC%20BY--NC%204.0-lightgrey)](LICENSE)
![Status](https://img.shields.io/badge/status-active-success)

> 貼上民法條文，AI 主動討論、確認範圍，產出結構化 HTML 教學講義——用理解取代死背。

---

## 這是什麼？

**Civil Law Interpretation** 是一套專為法律系學生、教師設計的 AI 輔助條文解釋工具。

跟「申論題練習」「判決分析」這兩套工具不同，這套工具是**從條文本身出發**：貼上一條或多條民法條文，AI 會先主動建議關聯條文、詢問是否有補充資料（學說、實務見解），討論到一定程度後，才產出一份包含條文結構、要件分析、教學案例、速查卡的完整講義。

核心精神是「用理解取代死背」——法律申論題的閱卷者，看的是你有沒有寫出正確的法條條號與關鍵字，不是要你把整條文字一字不漏地默寫出來。這套工具幫你把條文拆解成結構化的「要件」與「關鍵字」，取代逐字硬背。

---

## 適合誰使用？

| 對象 | 用途 |
|------|------|
| 📚 法律系學生 | 條文研讀、建立要件架構、速查卡複習 |
| 👨‍🏫 法律系教師 | 課堂講義製作、依授課對象調整深度 |
| ⚖️ 國考／司律考生 | 拆解常考條文的要件與關鍵字，減少死背負擔 |
| 🔬 法學教育研究者 | 探索 AI 輔助條文教學的可能性 |

---

## 主要功能

| 步驟 | 內容 |
|------|------|
| 1️⃣ 收集條文 | 原文照錄，並主動分析、建議關聯條文（必要／建議／可跳過） |
| 2️⃣ 確認講義範圍 | 條文結構解析（必選）、要件分析、教學案例、申論練習題、速查卡，逐項確認 |
| 3️⃣ 確認授課對象 | 依大一／大二三／研究所調整內容深度 |
| 4️⃣ 產生 HTML 講義 | 固定七章節：封面、條文原文、條文結構、要件解析、教學案例、申論練習題、速查卡 |
| 5️⃣ 實務見解搜尋 | 涉及判決、大法官解釋時，主動搜尋並列表供使用者確認，附原始來源與查詢路徑 |
| 6️⃣ 審閱修正 | 局部修改用 str_replace，大幅重構才整份重新輸出 |

---

## 快速開始

### 第一步：準備工具
你需要一個 **Claude 帳號**（免費版即可使用）：
👉 [https://claude.ai](https://claude.ai)

### 第二步：安裝 Skill
下載本倉庫的 [`SKILL.md`](./SKILL.md)，依你使用之 Claude 介面的 Skill 安裝方式匯入
（例如放入 `/mnt/skills/user/civil-law-interpretation/SKILL.md`）。

### 第三步：開始使用
1. 在 Claude 開啟一個新對話
2. 貼上你要解釋的民法條文全文，或說「幫我解釋民法第○條」
3. Skill 會先主動建議關聯條文、詢問補充資料，討論到位後才產出講義

就這樣，不需要安裝任何額外程式。

---

## 使用範例

**輸入：**
```
請解釋民法第92、93條之規定
（貼上條文全文）
```

**AI 回應（節錄）：**
```
在正式產出講義前，先幫您分析一下關聯條文，請您確認或補充：

【必要】民法第114條：撤銷之效力（撤銷後溯及既往無效）
【建議加入】民法第88、89條：錯誤之意思表示（可比較區分）
【可先跳過】民法第245-1條：締約過失（進階延伸，非核心）

想請問：
1. 這些關聯條文，您要補充哪些全文給我？
2. 講義單元要包含哪些？
3. 授課對象設定為哪個階段？
```

討論確認後，才會產出完整講義，包含條文結構、要件分析、速查卡等單元。

---

## 使用限制與提醒

- AI 分析結果僅供研讀與教學參考，**不構成正式法律意見**
- 法條、判決字號請以官方資料庫（全國法規資料庫、司法院法學資料檢索系統）為準
- 「判例」制度已於民國108年法院組織法修正後不再選編，舊判例現僅作為裁判先例參考，本工具引用時會特別標註
- 涉及非官方網站節錄之實務見解，會標明原始來源網址，使用前請自行至官方資料庫核實

---

## 檔案結構

```
civil-law-interpretation/
│
├── README.md      # 你現在看的這份說明文件
├── SKILL.md        # 完整 Skill 內容，依 Claude Skill 格式安裝即可使用
└── LICENSE          # CC BY-NC 4.0 授權條款
```

---

## 授權

本專案以 [CC BY-NC 4.0](./LICENSE) 授權公開，僅限非商業用途，
歡迎自由使用、修改與分享，請保留原作者資訊。

---

## 聯絡與貢獻

歡迎：
- 提交 **Issue** 回報問題或建議
- 提交 **Pull Request** 貢獻使用範例或改善 Skill 內容

---

*Powered by Claude（Anthropic）*
