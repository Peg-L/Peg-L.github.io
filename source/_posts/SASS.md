---
title: SASS
date: 2022-08-24 20:10:22
tags:
---

# [CSS 樣板語言 - SASS](https://hahow.in/courses/56189df9df7b3d0b005c6639/main?item=5a1e1745a2c4b000589dd21c)

### Sass: Syntactically Awesome Style Sheets 是 CSS 的樣板語言

<br/>

## 解決 CSS 的缺點

- 每個樣式最後都要加分號，缺少分號，導致前後樣式都出錯
- 要加一個大括號包住所有樣式
- 沒辦法一目了然層級關係  
  <br/>

## SASS 的特性

- 最後面不需要分號和大括號，打了反而錯
- 透過縮排來表示層級關係，元素只要跳一行縮排輸入，每個元素打完換行繼續打下一個元素
- 表現 class 內部的樣式，例如: .namecard h2，與前面元素同一層級，輸入 & h2 來表示
- 中間冒號後面記得要空一格
- 內部文字是在 「元素後」或是「class 後」空一格輸入  
  <br/>

## 變數概念管理色彩 & 內容

為網站設定視覺時，通常會有 3-5 個主要用色，反覆用在按鈕、邊框、背景等地方，如要修改主色，卻沒使用變數，必須要「一個一個剪貼將新色碼貼上」或是用「尋找+取代」，很麻煩又浪費時間

變數建立: `$變數名稱`

- 顏色變數 $color_word: #2D3748
- 距離變數 $margin_zero: 0px
- 內容變數 $title_front: "範例"

語法

```Pug
//- Pug
a.namecard
  h2.name 阿榮
    span.little_eng (Arong)
  h5.job 前端工程師
  hr
  p.description 前端菜鳥，為了轉職努力學習中
```

```SASS
<!-- SASS -->
$color_main: #f24
$color_background: #d1d1d1
$namecard_width: 350px
$namecard_height: 200px

.namecard
  color: $color_main
  backgound-color: $color_background
  width: $namecard_width
  height: $namecard_height
```

  <br/>

## 動態產生模組 mixin 概念

mixin 是將重複的 css 模組化，且可以帶入參數，依需求客製化模組，方便又保有彈性

語法範例 1

```Pug
//- Pug
.block1
.block2
.block3
```

```CSS
/* SASS */
@mixin block($length:40px, $color: black)
  width: $length
  height: $length
  border: solid 2px $color

.block1
  +block(70px, red)
.block2
  +block(100px, blue)
.block3
  +block(150px, green)
```

語法範例 2

```Pug
//- Pug
h3 標題文字
h4 副標題
.button
```

```CSS
/* SASS */
@mixin text($font-size: 30px, $color: red, $letter-spacing: 20px)
  font-size: $font-size
  color: $color
  letter-spacing: $letter-spacing

h3
  +text(30px, #333, 2px)
  font-family: 微軟正黑體

h4
  +text(20px, #777, 1px)
  font-family: 微軟正黑體

@mixin size($w, $h)
  width: $w
  height: $h

.button
  border: solid 1px
  +size(300px, 200px)
```

## [常用 mixin 與累積資源](https://codepen.io/mogzbvfl-the-reactor/pen/JjLqZZW)

```Pug
.block
  .block1
  h3 title
```

```CSS
*
  font-family: Helvetica, "Microsoft JhengHei"

html, body
  margin: 0px
  padding: 0px

@mixin indep
  position: absolute

/* 垂直水平置中 */
@mixin center
  position: absolute
  left: 50%
  top: 50%
  transform: translateX(-50%) translateY(-50%)

@mixin trans($s)
  transition: $s

@mixin size($w, $h)
  width: $w
  height: $h

@mixin fill
  width: 100%
  height: 100%

@mixin text($size, $spacing, $color)
  font-size: $size
  letter-spacing: $spacing
  color: $color !important

.block
  position: relative
  border: solid 1px
  +size(200px, 200px)

.block1
  +center
  +size(50px, 50px)
  border: solid 1px


h3
  +center
  margin: 0px
  +text(20px, 2px, red)

```
