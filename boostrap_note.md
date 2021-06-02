# Bootstrap
bootstrap主要是由上千行的css組成，在我們寫html時可以將class定義成已經寫好的class，取得其css設定

## Bootstrap 環境架設
網址：https://getbootstrap.com/docs/5.0/getting-started/introduction/
### CDN架設：
### 1. CSS
將樣式表 <link> 複製-貼上到 <head> 中其他所有的樣式表之前，以便載入 Bootstrap 的CSS。

```
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.0-beta1/dist/css/bootstrap.min.css" rel="stylesheet"integrity="sha384giJF6kkoqNQ00vy+HMDP7azOuL0xtbfIcaT9wjKHr8RbDVddVHyTfAAsrekwKmP1"crossorigin="anonymous">
```
### 2. Javascript
在</body> 結尾標籤前、頁面的末尾放置以下 <script>

```
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.0.0-beta1/dist/js/bootstrap.bundle.min.js" integrity="sha384-ygbV9kiqUc6oa4msXn9868pTtWMgiQaeYH7/t7LECLbyPA2x65Kgf80OJFdroafW" crossorigin="anonymous"><script> 
```

### 3.使用bootstrap所附的元件來測試是否有嵌入css

bootstrap網頁的“元件”-> "按鈕"
複製按鈕指令，測試是否具有顏色及形狀
網址：https://getbootstrap.com/docs/5.0/components/buttons/
```<button type="button" class="btn btn-primary">Primary</button>
<button type="button" class="btn btn-secondary">Secondary</button>
<button type="button" class="btn btn-success">Success</button>
<button type="button" class="btn btn-danger">Danger</button>
<button type="button" class="btn btn-warning">Warning</button>
<button type="button" class="btn btn-info">Info</button>
<button type="button" class="btn btn-light">Light</button>
<button type="button" class="btn btn-dark">Dark</button>

<button type="button" class="btn btn-link">Link</button>
```
### 4. 測試JS是否嵌入
bootstrap中文網頁的“元件”-> "互動視窗"->"範例"->“完整範例"
bootstrap英文網頁的“component”-> "modal"->"live demo"
![](https://i.imgur.com/twTNaPD.png =200x)

網址：https://getbootstrap.com/docs/5.0/components/modal/


### 本地下載：
### 1.官網下載檔案：
下載網址：https://getbootstrap.com/docs/5.0/getting-started/download/

在get started-> download->Compiled CSS and JS
下載資料夾
### 2.載入css
從下載的資料夾中找到bootstrap.min.css這個檔案或bootstrap.css，放入目標資料夾
### 3.載入js
從下載中檔案找到bootstrap.bundle.js或bootstrap.bundle.min.js，放入目標資料夾
- min相對於正常檔案，可以減少流量。正常檔案則可更好閱讀修改