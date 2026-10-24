# 深海優游交接資料｜給桌面版 ChatGPT

## 專案目前狀態

- 遊戲名稱：深海優游（Deep Sea Aquarium）
- 完整程式版本：**v0.41.9**
- 目標 GitHub repository：**`deep-sea-new`**
- 舊 repository：**`deep-sea-aquarium`**；使用者希望新網站與存檔確認完成後移除舊 repository。
- 本 ZIP 是完整 GitHub Pages 靜態網站原始檔，不是差異補丁。解壓後請將 ZIP 內的所有檔案及資料夾放在新 repository 根目錄。
- 專案含 `.github/workflows/pages.yml`，由 `main` 分支推送觸發 GitHub Pages 部署；新 repo 的 Pages Source 要選 **GitHub Actions**。

## 最重要：GitHub 專案與遊戲存檔是兩件事

GitHub repository 存放程式碼、圖片、音樂和主題素材；它不是玩家進度資料庫。遊戲進度目前自動存在瀏覽器的 localStorage，使用的鍵是 `starsea-aquarium-v1`。換瀏覽器、裝置或網站網域時，請使用遊戲內的 JSON 匯出／匯入功能搬移存檔。

使用者會在舊網站仍可開啟時，先從「我的水族箱日常 → 存檔與操作 → 匯出存檔」下載 `深海優游-save.json`，並把它另外存放在本 ZIP 和 GitHub repository 之外。新網站成功部署後，再從同一個設定區匯入。**不要把存檔 JSON 公開提交到 GitHub。**

如果新舊 Pages 網址同屬一個 `username.github.io` 網域，瀏覽器可能會共用 localStorage；仍以匯出的 JSON 作為正式備份與搬移來源，不要只依賴瀏覽器自動沿用進度。

## 遊戲資料與相容性

此 ZIP 包含目前完整網站檔案、全部魚種與美人魚素材、14 個佈景、原創背景音樂、游動動畫、課程與經濟邏輯、無障礙介面、存檔匯入／匯出程式，以及 Pages 部署流程。

v0.41.9 修正一般美人魚畫面只接受三個舊變體名稱的問題；存檔中的六種外觀現在會連到正確素材顯示。原始美人魚 PNG 保持未修改。程式保留既有存檔鍵和舊存檔轉換，請勿改存檔鍵、刪除素材或拿舊版本覆蓋此 ZIP。

## 建議交接順序

1. **先匯出並保管存檔**：確認 `深海優游-save.json` 已下載，且檔案不在待刪除的 repo 或本 ZIP 內。
2. 建立名為 **`deep-sea-new`** 的新 GitHub repository。公開狀態沿用使用者先前的決定。
3. 解壓本 ZIP，把裡面的所有內容放到新 repository 根目錄；不要只上傳 ZIP 檔本身。
4. 確認預設分支為 `main`，在 repository 的 **Settings → Pages** 將部署來源設為 **GitHub Actions**。推送後查看 Actions，等待 Pages workflow 成功，再取得新網站網址。
5. 開啟新網站，先確認頁面版本為 **v0.41.9**，水族箱能顯示、游動和播放音樂；再匯入 `深海優游-save.json`。
6. 匯入後核對魚隻數量與名字、金幣、寶石、課程狀態、佈景，以及一般美人魚的髮色與魚尾配色。發生錯誤時不要清除瀏覽器資料；保留 JSON 和錯誤訊息以便排查。
7. 新網站與存檔確認可正常使用後，依使用者指示移除舊的 **`deep-sea-aquarium`** repository。刪除前確認選中的 repository 名稱完全相符；不要誤刪 `deep-sea-new`。

## 可直接貼給桌面版 ChatGPT 的交接指令

> 請接手「深海優游」網站專案。請先閱讀這份 `HANDOFF_TO_DESKTOP_CHATGPT.md`，並以同一個 ZIP 中的完整 v0.41.9 網站檔案為唯一最新基準。我要建立新的 GitHub repository `deep-sea-new`，部署至 GitHub Pages；舊 repo `deep-sea-aquarium` 在新網站成功部署、我匯入 JSON 存檔並確認遊戲正常後，依我的指示移除。先協助我把存檔從舊網站匯出並存到 ZIP 和 repo 之外，再建立新 repo、將 ZIP 內容放在根目錄、設定 Pages 使用 GitHub Actions、確認 v0.41.9 上線，最後協助匯入和核對存檔。請保留所有素材與原有 `starsea-aquarium-v1` 存檔鍵；不要拿舊版本覆蓋或把存檔 JSON 公開提交。每完成一個階段，清楚告訴我目前畫面上要檢查什麼。
