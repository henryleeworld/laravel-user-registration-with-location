# Laravel 8 帶有地點註冊帳號

選擇地點時別忘了營業場所也要留意，除了租金地段外，還有土地使用分區與建物使用用途都要合格，以免日後受罰。

### 使用方式
- 把整個專案複製一份到你的電腦裡，這裡指的「內容」不是只有檔案，而是指所有整個專案的歷史紀錄、分支、標籤等內容都會複製一份下來。
```sh
$ git clone
```
- 將 __.env.example__ 檔案重新命名成 __.env__，如果應用程式金鑰沒有被設定的話，你的使用者 sessions 和其他加密的資料都是不安全的！
- 當你的專案中已經有 composer.lock，可以直接執行指令以讓 Composer 安裝 composer.lock 中指定的套件及版本。
```sh
$ composer install
```
- 產生 Laravel 要使用的一組 32 字元長度的隨機字串 APP_KEY 並存在 .env 內。
```sh
$ php artisan key:generate
```
- 執行 __Artisan__ 指令的 __migrate__ 來執行所有未完成的遷移，並執行資料庫填充（如果要測試的話）。
```sh
$ php artisan migrate --seed
```
- 執行 __npm__ 指令的 __install__ 來執行安裝專案引用的依賴套件。
```sh
$ npm install
```
- 執行安裝 Laravel Mix 引用的依賴項目，並執行所有 Mix 任務。
```sh
$ npm install && npm run dev
```
- 在瀏覽器中輸入已定義的路由 URL 來訪問，例如：http://127.0.0.1:8000。
- 你可以經由 `/register` 來進行註冊。

----

## 畫面截圖
![](https://i.imgur.com/Scri5gD.png)
> 公司法並未規定地點是否同時需為實際營業地址，但若另有其它營業地址存在，仍需依照營業稅法申請營業稅籍登記

![](https://i.imgur.com/LCcdEWt.png)
> 就公司法而言，同一地點是可以同時存在多家公司的，也可以登記兩家以上同業別的公司