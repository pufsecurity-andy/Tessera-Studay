# Tessera Study

研究 [TesseraHSM](https://github.com/TesseraHSM) 開源整合式 HSM 專案的工作 repo。

## 內容

| 路徑 | 說明 |
| --- | --- |
| [`codemap/index.html`](codemap/index.html) | **Code Map**：七層架構展開圖、請求路徑、六個 repo 的模組樹、TBOR 指令集、信任鏈、資安審查、商業分析 |
| [`codemap/system-map.html`](codemap/system-map.html) | **System Map**：雲端、伺服器（VM/hypervisor/sidecar）、PCIe 卡、晶片四層的關係圖，可切換 7 條資料流（運算、DARC 金鑰進入、證明、開機更新、備份、sidecar、營運者管理） |
| `repos/` | 六個 TesseraHSM repo 的 git submodule，固定在分析當下的 commit |

## 怎麼看 Code Map

GitHub 不會直接渲染 HTML。請把 repo clone 下來（或在 GitHub 上下載 `codemap/` 底下的 HTML 檔），再用瀏覽器打開。每個頁面都是單一檔案，不需要網路就能看。

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

## 注意

Code Map 裡的資安發現是靜態閱讀的結果，沒有執行或在硬體上驗證過。對外公開之前，請先私下聯絡 TesseraHSM 維護者（responsible disclosure）。
