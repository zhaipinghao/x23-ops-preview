# X23 電商營運中台｜妹妹預覽版

妹妹不用看 `docs` 裡面的 `.md` 文件，那些是給我和 GitHub 部署用的備忘錄。

她真正要看的只有網站本身：

- 本機預覽：直接開 `index.html`
- GitHub Pages 上線後：直接開網站網址，例如 `https://你的帳號.github.io/x23-ops-preview/`

這是給內部夥伴快速理解流程的靜態預覽版，不是正式後台。

## 預覽內容

- X23 每日營運總覽
- 多工 Agent 分工
- 貼文排程與素材庫存概念
- 資料源與缺報表清單
- Meta Ads / 蝦皮廣告判讀規則
- 人工出貨與高風險審核邏輯

## 安全說明

此版本不包含：

- 平台帳密
- API Key / Token
- 真實客戶資料
- 真實訂單資料
- 真實廣告報表
- 本機 SQLite 資料庫
- FB、IG、蝦皮、Momo、PChome 後台連線

所有數字與資料皆為示範或本機回填資料，只用來讓妹妹或內部夥伴看懂系統會怎麼管理。

## GitHub Pages

建議將 GitHub Pages 設為從 repository root 發布，入口檔案為 `index.html`。

若要正式多人使用，需要另外做登入、權限、雲端資料庫與平台授權，不要用這份靜態版承接真實營運。

如果看不懂 GitHub 文件，請忽略 `docs` 資料夾；只要把 GitHub Pages 網址丟給妹妹就好。
