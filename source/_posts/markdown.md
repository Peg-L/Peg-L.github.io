---
title: Markdown
date: 2022-08-24 20:10:22
tags:
---

# **Markdown(MD)**

- 易讀易寫
- 很多軟體和服務支援 (Obsidian, Notion, Github, HackMD...等)  
  <br/>

---

## **資源 Sources**

- [官方文件(中)](https://markdown.tw/)

- [官方文件(Eng)](https://www.markdownguide.org/basic-syntax/)

- [Youtube 教學影片(Eng): Learn Markdown in 30 minutes!](https://www.youtube.com/watch?v=bTVIMt3XllM)  
  <br/>

---

## **預覽 Preview**

使用 VS Code 編輯 MD，先打開預覽頁面，可在編輯時同時觀看頁面呈現

#### 預覽頁面開啟方式:

- 右鍵 --> open preview
- 快捷鍵: ctrl + shift + v  
  <br/>

---

## **標題 Title**

```
# H1

## H2

### H3

#### H4

##### H5

###### H6
```

<br/>

---

## **重點標註 Emphasize**

可以合併使用

- 粗體
  - 呈現 **粗體內容**
  - 語法 `**粗體內容**`
- 斜體
  - 呈現 _斜體內容_
  - 語法 `*斜體內容*`
- 刪除線
  - 呈現 ~~劃掉內容~~
  - 語法 `~~劃掉內容~~`  
    <br/>
- 引用

  - 呈現

    > Never Give up, Keep Going.

    語法  
    `> Never Give up, Keep Going.`

---

## **清單 List**

### **有序 ol**

輸入 1. 2. 3.....，或是全部輸入 1. 1. 1. 使用後者佳，呈現時仍會自動排序，調動順序就不用手動重新編號 <br/>

呈現

1. 有序清單
1. 清單有序
1. 有序的清單

語法

```
1. 有序清單
1. 清單有序
1. 有序的清單
```

### **無序 ul**

呈現

- 有序清單
- 清單有序
- 有序的清單

語法

```
- 有序清單
- 清單有序
- 有序的清單
```

  <br/>

---

## **連結 Link**

### 外部連結

#### 呈現 [Markdown 連結教學(Eng)](https://youtu.be/bTVIMt3XllM?t=1305)

#### 語法 `[Markdown連結教學(Eng)](https://youtu.be/bTVIMt3XllM?t=1305)`

<br/>

#### 內部標題跳轉連結

#### 呈現 [預覽](#預覽-preview)

#### 語法 `[預覽](#預覽-preview)`

<br/>

### 圖片連結

#### 呈現 ![Markdown](https://geekytheory.com/content/images/2014/03/markdown.png)

<br/>

#### 語法 `![Markdown](https://geekytheory.com/content/images/2014/03/markdown.png)`

<br/>

---

## **程式碼區塊 Code Block**

#### 呈現

`單行標註`

```
多行標註
```

#### 語法

`` `單行標註` ``

````
```
多行標註
```
````

<br/>

---

## **核取方塊**

VS code 不支援 checkbox，可安裝擴充功能 markdown checkboxes (Matt Bierner)

#### 呈現

- [x] Task #1
- [ ] Task #2

#### 語法

```
- [x] Task #1
- [ ] Task #2
```

<br/>

---

## **表格 Table**

#### 呈現

| Number | Name             |
| ------ | ---------------- |
| 1      | Harry Potter     |
| 2      | Hermione Granger |
| 3      | Ron Weasley      |

#### 語法

```
| Number | Name             |
| ------ | ---------------- |
| 1      | Harry Potter     |
| 2      | Hermione Granger |
| 3      | Ron Weasley      |
```

<br/>

---

## **隱藏說明**

#### 呈現

<details>
 <summary>躲貓貓</summary>

#### 不在這裡喔

 <br/>

## _再找找_

也不是這裡哈哈

| 哈囉 | 你好   |
| ---- | ------ |
| 找錯 | 地方拉 |
| 加油 | ~~~~   |

**被你找到了...下次見**

</details>

#### 語法

```markdown
<details>
 <summary>躲貓貓</summary>

#### 不在這裡喔

 <br/>

## _再找找_

也不是這裡哈哈

| 哈囉 | 你好   |
| ---- | ------ |
| 找錯 | 地方拉 |
| 加油 | ~~~~   |

**被你找到了...下次見**

</details>
```
