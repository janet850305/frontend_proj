# HISKIO 18 小時 零基礎網頁前端入門秘笈
## 單元 4&5 - HTML 實作
* 快捷鍵: 
    * ! =
    ```html
      <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta http-equiv="X-UA-Compatible" content="IE=edge">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Document</title>
    </head>
    <body>

    </body>
    </html>
    ```
    * #header =
    ```html
    <div id="header"></div>
    ```

    * img=
    ```html
     <img src="" alt=""> 
     ```
    *  (li>a[href=#])*9=
    ```html
       <li><a href="#"></a></li>
       <li><a href="#"></a></li>
       <li><a href="#"></a></li>
       <li><a href="#"></a></li>
       <li><a href="#"></a></li>
       <li><a href="#"></a></li>
       <li><a href="#"></a></li>
       <li><a href="#"></a></li>
       <li><a href="#"></a></li>
     ```    
    * .slider=
    ```html
    <div class="slider"></div>
    ```
    * row/column 用法
    ![](https://i.imgur.com/dTbAONL.png)
    這裡Grid的概念，常用把畫面分成12份，由於上面有兩張，下面有三張，要把五張圖用row包起來，然後依據上面的一張圖佔6份，下面一張圖佔4份等分
    ```html
    <div class="row">
        <div class="col-6"><a href="#"></a></div>
        <div class="col-6"><a href="#"></a></div>
        <div class="col-4"><a href="#"></a></div>
        <div class="col-4"><a href="#"></a></div>
        <div class="col-4"><a href="#"></a></div>

    </div>
    ```
    * 減少tab 縮排: shift+tab
    * span.title =
    ```html
    <span class="class">outdoor lighting</span>
    ```
    * & amp; 去除空格 = &
    * & lt; 去除空格 = <
    * & gt; 去除空格 = >
    * Lorem Picsum:
        visual studio code內裝套件
        可使用 picsum快速產生假圖
    * Lorem ipsum:
        visual studio code內裝套件
        可使用lorem快速產生假文字
        ex : lorem10 =產生十個字的假字
        
    * 假按鈕
    ```html
    <a href="#" class="button">shop now</a>
    ```
    * email/phone 連結製作
    ```html
    <a href="mailto:testmail@yourdomail.com">testmail@yourdomail.com</a>
    <a href="tel:+62-500-800-123">+62-500-800-123</a>
    ```
    
* tips:
    * 假圖網站:https://picsum.photos/
    * 量測大小工具:
        * Markman http://www.getmarkman.com/#/download-modal
            * 馬克鰻還可以標記顏色
        * mac 截圖工具
    * 量測顏色工具: Sip
    * HTML 特別文字查詢  https://dev.w3.org/html5/html-author/charref

* 觀念
   ```html
   <a href="#"></a> //假連結
   <a href="#footer"></a> //跳轉到footer
   <a href="page.html"></a> //跳轉到另一個html
   ```
   * container 常用在置中


## CSS實作觀念
* html與css串聯
    1. html 內部直接修改框架css:
    ```html
    <style></style>
    ```
    2. html連結到外部css檔案:
    ```html
    <link rel="stylesheet" href="css/main.css"/>
    ```
* css快捷鍵
    * bc= background-color:
    * w1170 = width: 1170px;
    * tax = text-align: center;
    * db = display: block;
    * m0-a = margin: 0 auto;
    * 快速註解in vscode = ctrl +k +c
    * 自動整理程式碼 alt + shift + f
    * lst-n = list-style-type: none;
    * p0-12 = padding: 0 12px;
    * tdn= text-decoration: none;
    * ttu =text-transform: uppercase;
* css 好用工具:
    * normalize.css:reset 框架，將不必要的外框去除，並且調成大多現在網站的格式，統一將不同瀏覽器的設定設為一致，避免logo大小等在不同瀏覽器上大小有誤差
    https://github.com/necolas/normalize.css

* css觀念
    * 容器置中:大部分現在網站都有置中效果，是利用下面的code做的
   ```css
    .container{
        display: block; //讓container占據整行
        width: 1170px; //限制container寬度
        margin: 0 auto; //將原本因為container限制寬度產生的右側margin，左右平均分攤
    }   
   ```
   * 分左右兩側
   ```css
    #logo{
        float: left;
    }
    #nav{
        float:right;
    }
   ```
   * li 由直排列變橫排列
   ```css
   #nav li{
    float: left;  //每一個li都會緊跟著前一個li
    list-style-type: none;  //讓li前面的點去除
    }    
   ```
   * li 加 padding VS a 加 padding
     li 加 padding:只有在文字上才可以點連結
     a 加 padding: 文字周圍也可以點到連結
   * 文字大寫:
       * 全部大寫:text-transform: uppercase;
       * 字首大寫:text-transform: capitalize;
   * 一般給定一個100x100的img 會output 一個 100x104的 div:
   這是因為像gp這種超過底線的文字需要留白，所以預設display:inline。
   去除這種狀況只需要在css最初加上
   ```css
   img{
    display: block;
    }
   ```
   * 文字行置中:
    ![](https://i.imgur.com/B51Y8Rd.png)
    ![](https://i.imgur.com/Z1jeGjN.png) 

   ```css
    #nav{
       line-height: 100px;
    }
    ul{
    margin: 0;
    }
   ```
   * ul、li預設:
   由於大多設計師不會採用ul預設的點和設計，所以在最開始就可以如下設定
   ```css
    ul{
    margin: 0;
    }
    li{
        list-style-type: none;
    }
   ```
   * clearfix :去除雜邊的方法 
   https://css-tricks.com/clearfix-a-lesson-in-web-development-evolution/
   ```
   .container {
    display: flow-root;
    }
   ```
   * 讓全螢幕圖片可以依照螢幕大小等比例切換:
   ```
   .slider img{
    width: 100%;;
    height: auto;;
    }
   ```
   * 當你設定一個元素樣式為 box-sizing: border-box;，這個元素的內距和邊框將不會增加元素本身的寬度
   ```
   *{
    -moz-box-sizing: border-box;
    -webkit-box-sizing: border-box;
    box-sizing: border-box;
    }
   ```
   * clearfix 很重要，在使用position進行設定之後會有跑圖的情形，利用clearfix可以將等階層的div清楚的分隔開，不會向上跑到上一個定位位置

   * background-attachment: fixed;
   可以做出隨著滑動移動觀看位置的特殊效果
   * background-position: 50% 50%;
   當存放圖片的box大小有限制時，可以用這個來顯示我們想要的背景圖片位置
   * 文字中的上下左右置中
       左右置中: text-align: center;
       上下置中:  line-height: 40px(與文字設定時的高度相同);