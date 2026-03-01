# A website
網址：https://fogmaze.github.io/OrgWebTest/theme/

## Setup
本項目使用node.js，配合gulp、nunjucks等套件進行靜態網站生成，使用Bootstrap風格定義模板。
要建置此專案，你需要先安裝npm，並用以下指令安裝依賴
```bash
npm install
```

## 如何協作
1. 基本方法  
   在電腦上安裝git，並使用git來進行資料檔案同步，git使用方法可以在網路上找到，基本會用到clone / add / commit / pull / push指令  
   目前使用git pages架設此網站，使用git push更新檔案內容後等個一下子就會自動更新在網站頁面上。

## 日常資料更新

若有新的內容，更新 data/data.xlsx 中的資料，請根據不同資料表中定義好的格式寫入：
  公告與課程資料表中一行代表一個課程/公告，若要新增資料請自行編號index後創建新的一筆資料，index不能重複。
  若是圖片內容則可放在 data/dataImages 下面，並在 data/data.xlsx 中的對應欄位以右鍵加入連結的方式將相對路徑填入儲存格中(用相對路徑)。
  若是公告中要加入attachment則放在data/dataAttachments中，然後在data.xlsx的attachments資料表中加上該公告的index與attachment 文件的連結(和圖片一樣的方法)。

更新好資料後，運行
```bash
npm run build
```
即可將更新過後的網頁html生成於theme資料夾下

## 項目結構與開發

網頁原始碼放在 source 資料夾下面，透過指令
```bash
npm run build
```
即可將theme中的內容，生成html網頁於 theme 資料夾下

開發時，可以用
```bash
npm run dev
```
在修改後即時更新網頁狀態

建議使用vscode內建的copilot或是codex 進行 vibe coding。

## Trouble shooting

建議使用vscode內建的copilot或是codex 進行 vibe coding。

## Development Detail & Framework
專案建置方法定義在gulpfile.js，建置時會將data/data.xlsx的內容透過nunjucks填入在source資料夾定義好的模板中。
在source下的html中，可以使用以下程式碼將data.xlsx的資料填入html中(注意lineIndex的地方有點反直覺)
```
{{data.sheetName[lineIndex].key}}
```
## TODO
1. 確認內容與排版 footer.htm須改
2. 找一個好的上架流程、託管網站
3. domain
## License

Copyright (c) 2016 - Present, Designed & Developed by [Themefisher](https://themefisher.com)

**Code License:** Released under the [MIT](https://github.com/themefisher/revolve/blob/main/LICENSE) license.

**Image license:** The images are only for demonstration purposes. They have their license, we don't have permission to share those images.

<!-- resources -->
## Resources

Some third-party plugins that we used to build this template. Please check their license.

* **Bootstrap v4.5**: <https://getbootstrap.com/docs/4.5/getting-started/introduction/>
* **Jquery v3.5.1**: <https://jquery.com/download/>
* **Themify Icons**: <https://themify.me/themify-icons>
* **Google Fonts**: <http://fonts.google.com/>
* **AOS**: <https://michalsnik.github.io/aos/>
* **Venobox**: <https://veno.es/venobox/>
* **Slick**: <https://kenwheeler.github.io/slick/>
* **Filterizr**: <https://yiotis.net/filterizr/>
