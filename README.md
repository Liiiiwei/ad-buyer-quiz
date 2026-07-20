# 廣告投手屬性鑑定

一支單檔測驗網頁。三軸（數據↔創意、進攻↔穩健、策略↔執行）加實力題計分，測完給出 8 型其中一型的結果卡。

## 特性

- **單一 HTML 檔**，沒有框架、沒有外部資源、沒有後端
- **斷網可用**，直接 AirDrop 給人也能開
- 手機優先，作答進度存在 `localStorage`
- 支援 `prefers-reduced-motion`

## 部署

GitHub Pages 直接發布 `main` 分支根目錄即可，不需要建置流程。

## 本機預覽

```bash
python3 -m http.server 8899
# 開 http://localhost:8899
```

`file://` 直接開會被瀏覽器的 `localStorage` 限制擋掉，用上面的方式起一個本機伺服器。

## 角色圖

結果卡的角色形象放在 `TYPES` 各型別的 `art` 欄位，以及全能游走型專用的 `SWAY_ART`，格式是 base64 data URI（用 WebP，PNG 會讓檔案過大）。留空時顯示虛線佔位框，不影響版面，可以一張一張補。

原始碼來源：`ad-course-v2/docs/meetup-2026-07-25/quiz-app/`
