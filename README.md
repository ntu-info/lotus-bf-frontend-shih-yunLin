

# NOUS Frontend

現代化 React 前端，專為神經科學文獻搜尋、分析、可視化打造。
本專案採用 Vite + React 19，支援 Nii 檔案瀏覽、條件搜尋、書籤管理、作者聚焦等多元功能。

## 主要功能與特色

- **布林查詢與關鍵字搜尋**
	- 支援 AND / OR / NOT 布林運算，精確搜尋神經科學文獻。
	- 搜尋欄可即時提示、下拉選單選擇相關性詞彙。

- **書籤系統**
	- 可將任意文獻加入書籤，並於 bookmarks 頁面集中管理。
	- 書籤可編輯備註，支援 localStorage 永久保存。
	- 書籤按鈕即時同步狀態，支援多頁面互動。

- **表格管理**
	- 書籤頁以現代化表格呈現，欄位自動寬度、title 欄自動換行。
	- 支援橫向滑動，適合大量欄位瀏覽。
	- 欄位可拖曳調整寬度（部分瀏覽器支援）。
	- 表格可即時編輯備註、座標選擇。
    - 小箭頭可即時查看 Nifti viewer。

- **Nii 檔案瀏覽與座標選擇**
	- 整合 @niivue/niivue，支援 NIfTI 檔案可視化。
	- 可於文獻表格直接選擇座標，並同步顯示於 NiiViewer。

- **作者聚焦與團隊介紹**
	- Authors 頁面展示 NOUS 團隊成員、專長、代表論文。
	- 支援自訂作者 spotlight 卡片。

- **現代化 UI/UX 設計**
	- 採用 Sora、Playfair Display 字型，乾淨易讀。
	- 支援深色/淺色主題（可擴充）。
	- 響應式設計，桌機與行動裝置皆適用。

- **進階功能**
	- 支援條件篩選（Filters），可依年份、作者、期刊等多條件篩選。
	- 支援分頁、拖曳調整主區塊寬度。
	- 支援 API 端點自訂（api.js 可調整後端路徑）。

## 安裝與啟動

1. 安裝 Node.js (建議使用 nvm)
	 ```sh
	 nvm install --lts
	 ```

2. 清除舊套件（如遇安裝衝突）
	 ```sh
	 rm -rf node_modules package-lock.json
	 ```

3. 安裝依賴
	 ```sh
	 npm install
	 ```

4. 啟動開發伺服器
	 ```sh
	 npm run dev
	 ```

5. 建置正式版（產生 dist 資料夾，可部署到伺服器）
	 ```sh
	 npm run build
	 ```

## 專案結構

- `src/`：主要程式碼
	- `components/`：React 元件（Header, BookmarksPage, BookmarkButton, Studies, Filters, NiiViewer, QueryBuilder, Terms 等）
	- `lib/`：工具函式（如 bookmarks.js，管理 localStorage 書籤）
	- `hooks/`：自訂 hook（如 useUrlQueryState）
	- `App.jsx`：主頁面邏輯，負責路由與主 UI
- `public/static/`：logo 與靜態資源
- `index.html`：入口 HTML
- `vite.config.js`：Vite 設定

## 其他

- 若遇到套件相容性問題，請優先清除 node_modules 並重新安裝。
- 書籤、備註等資料會儲存於 localStorage。
- 若需部署，請將 `dist/` 資料夾上傳至伺服器。

## 聯絡與貢獻

- 本專案由 NOUS 團隊與台大心理所資訊組協作開發。
- 歡迎 issue、pull request 或聯絡 maintainer 討論改進。
