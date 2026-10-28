# Tessera Study

研究 [TesseraHSM](https://github.com/TesseraHSM) 開源整合式 HSM 專案的工作 repo。

## 內容

| 路徑 | 說明 |
| --- | --- |
| [`index.html`](index.html) | 網站首頁，列出 `pages/` 底下所有頁面 |
| [`pages/code-map.html`](pages/code-map.html) | **Code Map**：七層架構展開圖、請求路徑、六個 repo 的模組樹、TBOR 指令集、信任鏈、安全設計（規格原文） |
| [`pages/system-map.html`](pages/system-map.html) | **System Map**：雲端、伺服器（VM/hypervisor/sidecar）、PCIe 卡、晶片四層的關係圖，可切換 7 條資料流（運算、DARC 金鑰進入、證明、開機更新、備份、sidecar、營運者管理） |
| [`pages/asic.html`](pages/asic.html) | **Tessera ASIC 架構與需求**：CRD 375 項需求的方塊圖、效能目標、實作現況與完整需求原文 |
| `repos/` | 六個 TesseraHSM repo 的 git submodule，固定在分析當下的 commit |

## 線上瀏覽

- 首頁：<https://pufsecurity-andy.github.io/Tessera-Studay/>
- Code Map：<https://pufsecurity-andy.github.io/Tessera-Studay/pages/code-map.html>
- System Map：<https://pufsecurity-andy.github.io/Tessera-Studay/pages/system-map.html>
- ASIC 架構與需求：<https://pufsecurity-andy.github.io/Tessera-Studay/pages/asic.html>

每個頁面都是單一 HTML 檔，也可以下載後直接用瀏覽器打開，不需要網路。

## 新增頁面

1. 把 HTML 檔放進 `pages/`（頁面內回首頁的連結用 `../index.html`）
2. 在根目錄 `index.html` 的 `PAGES` 陣列加一筆（`href`、`title`、`desc`、`tags`、`date`）

## 取得原始碼

```sh
git clone --recursive https://github.com/pufsecurity-andy/Tessera-Studay.git
# 已經 clone 的話
git submodule update --init --depth 1
```

| Submodule | Commit | 日期 |
| --- | --- | --- |
| tessera-specs | `bcdb753` | 2026-10-09 |
| tessera-rtl | `fc5e739` | 2026-10-09 |
| tessera-sw | `3281212` | 2026-10-27 |
| tessera-linux-driver | `a43d313` | 2026-10-09 |
| tessera-sidecar-scripts | `d3292a9` | 2026-10-10 |
| unikraft | `0a6044d` | 2026-10-09 |

更新到上游最新版：`git submodule update --remote --depth 1`

