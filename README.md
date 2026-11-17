# house-contract.com 離線備份

備份日期：2026-11-16（Asia/Taipei）
來源：https://house-contract.com/

本備份已放在 GitHub 儲存庫：https://github.com/kovatw/house-contract  
GitHub Pages 已從 `main` 分支根目錄啟用，並設定自訂網域 house-contract.com。目前正式網域仍指向原本的託管，尚未切換 DNS。

這是一份可自行架設的完整靜態備份。圖片、字型、JS、CSS 都已下載到本資料夾。訂購表單、試算表、LINE 連結仍指向原本的外部網站。

## 裡面有什麼

- `index.html`、`contracts/`、`faq/`、`contact/`：網站各頁（SPA，並已預先填入渲染後的 HTML）
- `404.html`：給 GitHub Pages 用的 SPA 後備頁
- `assets/`：JS、CSS、圖片、字型
- `prerendered/`：各路由完整渲染後的 HTML 快照
- `robots.txt`、`sitemap.xml`、`favicon.png`

頁面路由：`/`、`/contracts`、`/faq`、`/contact`
契約分類篩選：`/contracts?category=sales-commission` 等。

## 本機預覽

在本資料夾執行：

```bash
python3 -m http.server 8080
```

然後打開 http://127.0.0.1:8080/

請從網站根目錄啟動，不要用 `file://`，否則絕對路徑 `/assets/...` 會失效。

## 之後放到 GitHub Pages

1. 把這個資料夾內容推到 GitHub 儲存庫（放在根目錄）。
2. 開啟 GitHub Pages。
3. 若使用自訂網域 house-contract.com，在儲存庫加上 `CNAME` 檔（內容一行：`house-contract.com`），再到 Cloudflare 把 DNS 指到 GitHub Pages。
4. `404.html` 已準備好，用來處理前端路由。

請先確認新網站能正常打開，再把網域指過去、並停用原本的網站託管。

## 保留的外部連結

- Google 訂購表單
- Google 試算表訂購單
- 電話 `tel:04-35023788`
- LINE 加入好友（楊小姐，ID：ivanok88）
