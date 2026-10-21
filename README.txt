小兵傳奇：Emoji 星途｜PWA iPhone 6 優先版

內容
- index.html：遊戲主程式，保留原始星際 RPG 玩法並加強手機觸控與小螢幕版面。
- manifest.webmanifest：主畫面捷徑與 PWA 設定。
- sw.js：核心資源快取；成功載入一次後，核心遊戲可離線開啟。
- jspdf.umd.min.js：本機 PDF 函式庫，避免 PDF 功能必須連線下載程式庫。
- icon-192.png / icon-512.png / icon-maskable-512.png / apple-touch-icon.png：應用程式圖示。

iPhone 6 使用方式
1. 將此資料夾部署到支援 HTTPS 的靜態網站（例如 GitHub Pages）。
2. 在 iPhone 6 的 Safari 開啟部署網址。
3. 點「分享」→「加入主畫面」。
4. 第一次載入時請保持網路連線，讓遊戲與資源完成載入；之後可測試離線啟動。

重要相容性說明
- iPhone 6 的實際 iOS 版本、Safari 版本與裝置狀態會影響結果。此版本採用 iOS 12 世代可用的基本 Web API 與 CSS 回退寫法，但仍需在實機完成最終驗收。
- 直接從「檔案」App 開啟 HTML 可玩核心遊戲，但 Service Worker / PWA 安裝通常需要 HTTPS 網站；建議透過 HTTPS 部署。
- AI 小說改寫需要網路及 Puter 服務；核心探索、戰鬥、遊戲存檔與離線範本不依賴 AI。
- 遊戲存檔使用瀏覽器 localStorage；清除 Safari 網站資料可能刪除存檔，建議定期保留存檔備份。

驗收清單
□ iPhone 6 直向：地圖、隊伍狀態、操作按鈕均可見且可觸控
□ 戰鬥視窗可上下捲動，技能與關閉／撤退按鈕可操作
□ 據點商店、招募、治療、強化、躍遷門可操作
□ 遊戲重整後可恢復 localStorage 存檔
□ HTTPS 部署後可加入主畫面，第二次載入後可測試離線啟動
□ 首領戰、敗北返航、第二周目及小說匯出流程完成實機測試

本包為相容性優化版本；以上勾選項目應由實際 iPhone 6 測試後再標記完成。
