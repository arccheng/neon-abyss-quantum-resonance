# 霓虹深淵：量子共鳴 · NEON ABYSS: QUANTUM RESONANCE

一款單檔 HTML 的霓虹風格俯視角生存射擊（roguelite）遊戲，支援桌機滑鼠鍵盤、手機／平板觸控，以及好友 1v1 連線對戰。

**▶ 線上直接玩：<https://arccheng.github.io/neon-abyss-quantum-resonance/>**

![status](https://img.shields.io/badge/build-single--file%20HTML-39d0ff) ![license](https://img.shields.io/badge/license-MIT-blue)

---

## 遊戲內容

| 項目 | 說明 |
|---|---|
| 模式 | 單人無盡生存、雙人對戰 1v1（P2P 房間碼連線） |
| 難度 | 新兵校準（0.8×）/ 標準共振（1.0×）/ 深淵過載（1.4×）/ 量子奇點（2.0×） |
| 戰鬥 | 波次生存、首領戰（Boss HP 條）、量子護盾、衝刺相位閃避、連擊 Combo |
| 構築 | 每波結束三選一進化模組、戰術補給箱、戰術重骰、59 項模組圖鑑（Codex） |
| 場地 | 19 張競技場（雷射／機關、重力／蟲洞、隱匿／機動、反射／迷宮等主題） |
| 計分 | 最終戰術評分、最佳分數、即時／峰值 DPS、擊殺數統計 |
| 音效 | WebAudio 即時合成音效，可一鍵靜音 |

## 操作方式

**桌機**

- `WASD` / 方向鍵：移動
- 滑鼠：瞄準（零自瞄）與射擊
- `Space` / 滑鼠右鍵：相位衝刺（無敵幀）
- `Shift` / `E`：時空緩速
- `F`：自動連發開關
- `R`：戰術重骰
- `P`：圖鑑／暫停

**手機／平板**

- 左半螢幕虛擬搖桿：移動
- 右半螢幕虛擬搖桿：瞄準並自動開火
- 介面按鈕可直接觸控操作

## 本機執行

遊戲是單一 HTML 檔，不需要建置流程：

```bash
# 方式一：直接開檔
open index.html

# 方式二：起本機伺服器（建議，行為與線上一致）
python3 -m http.server 8080
# 瀏覽 http://localhost:8080
```

> 注意：請用 HTTP 或直接開檔遊玩；在 iPad 上用「檔案」App 的 Quick Look 預覽不會執行 JavaScript，需改用網址開啟。

## 技術說明

- 純前端單檔（HTML + CSS + JavaScript），無框架、無需編譯。
- 渲染：Canvas 2D。
- 連線：PeerJS（WebRTC P2P），以房間碼配對；無自架伺服器。
- 外部依賴僅 CDN 的 PeerJS 與 Google Fonts，因此**首次載入需要網路**；單人遊玩在載入後可離線進行。

## 版本

- `index.html` 對應 Claude 產出的最終版本（neon_abyss_quantum_resonance 第 14 版，2026-11-21）。

## 授權

MIT License，詳見 [LICENSE](LICENSE)。
