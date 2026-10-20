我的智慧廚房｜截圖匯入食材版

檔案：
- index.html：App 主程式，包含食材、食譜、菜單、採買、截圖 OCR 匯入與食譜配對
- manifest.json：加入 iPhone 主畫面的基本設定
- sw.js：簡單離線快取

免費發布：
1. 將三個檔案放在同一個 GitHub repository 的根目錄。
2. Repository → Settings → Pages。
3. 在 Build and deployment 選擇 Deploy from a branch。
4. Branch 選 main，資料夾選 /(root)，按 Save。
5. 等待 GitHub Pages 部署完成，開啟它提供的網址。
6. iPhone 用 Safari 開啟網址 → 分享 → 加入主畫面。

截圖匯入：
- 到「食材」頁，點「截圖匯入」。
- 選購物訂單截圖，按「辨識訂單文字」。
- 確認/修改名稱、數量、單位，選擇預設保存位置，再加入庫存。
- OCR 使用 Tesseract.js 與繁體中文/英文語言資料，首次使用需要網路載入；辨識結果可能錯誤，請人工確認。
- 圖片由瀏覽器端處理，本程式不會主動將圖片上傳到自有伺服器。

料理推薦：
- 依食譜逐行列出的食材，與庫存名稱做簡易文字配對。
- 推薦比例只是文字比對，不是 AI 對食物的理解；請檢查缺料與份量。
- 菜單採買清單為簡易規則，產生後請人工確認數量。

重要：
- 資料存在本機瀏覽器 localStorage，不會自動同步到其他裝置。
- 定期到「採買」頁匯出 JSON 備份。
- 清除 Safari 網站資料可能造成資料遺失。
- 這是第一版，尚未串接雲端資料庫或 AI API。
