# A website

## Setup
本項目使用node.js，配合gulp、nunjucks等套件進行靜態網站生成。
要建置此專案，你需要先安裝npm，並用以下指令安裝依賴
```bash
npm install
```

## Workflow

### 日常資料更新

若有新的內容，更新 data/data.xlsx 中的資料，若是圖片內容則可放在 data/dataImages 下面，並在 data/data.xlsx 中的對應欄位以右鍵加入連結的方式將相對路徑填入儲存格中。

更新好資料後，運行
```bash
npm run build
```
即可將更新過後的網頁html生成於theme資料夾下

### 項目結構與開發

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

### Development Detail
專案建置方法定義在gulpfile.js，建置時會將data/data.xlsx的內容根據nunjucks填入在source資料夾定義好的模板中。
在source下的html中，可以使用以下程式碼將data.xlsx的資料填入html中(注意lineIndex的地方有點反直覺)
```
{{data.sheetName[lineIndex].key}}
```
#### TODO
1. 將模板網站上的資料連結到xlsx中 (模板中的圖片好像都沒有授權)
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
