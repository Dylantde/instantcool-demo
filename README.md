# Instantcool — 示範網站 / Demos

Instantcool Technology Limited 共享掛頸風扇服務的兩個前端示範。
兩者皆為單一自足的 HTML 檔案，無外部依賴、無後端。

| | 連結 | 內容 |
|---|---|---|
| **用戶端 H5** | https://dylantde.github.io/instantcool-demo/ | 地圖站點、掃碼租借、計時計費、異櫃歸還、零售購買、退貨／私隱／送貨政策 |
| **營運後台** | https://dylantde.github.io/instantcool-demo/admin/ | 機櫃、風扇、消毒記錄、租借及零售訂單、用戶、場地夥伴、收益報表、分成提現 |

---

## 這些是示範，不是營運系統

- **全部資料為模擬。** 站點、訂單、用戶、金額均非真實營運紀錄。
- **沒有後端。** 後台的登入頁接受任何密碼，因為背後沒有任何東西可供驗證。
- **政策文件為草擬版本**，尚未經法律專業人士審閱。

## ⚠️ 後台上線前必讀

這個倉庫是公開的（GitHub Pages 免費方案的要求）。目前無妨——後台只是一個
沒有後端的空殼。**但一旦把它接上真實 API，就必須立即停止公開存取：**

- 移至內部網絡或需登入的主機，不應公開於互聯網
- 實作角色權限（前端收起選單不構成權限控制，每個端點都要自己驗證）
- 啟用雙重認證
- 加入審計紀錄：批核提現、遠端開櫃等動作須記錄誰、何時、對哪一筆

## 更新

兩個示範都由各自的原始碼打包成單一檔案：

```bash
python3 tools/build.py      # 產生 dist/public/index.html
```

再把 `index.html` 上載回本倉庫（用戶端放根目錄，後台放 `admin/`）。

---

Instantcool Technology Limited · dylan@instant-cool.com
