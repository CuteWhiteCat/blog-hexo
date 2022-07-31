---
title: Freenom + CloudFlare + Github Pages 架站攻略
author: 白貓
banner_img: https://cdn.wallpapersafari.com/23/58/m0VLlg.jpg
index_img: ../../images/Freenom_CloudFlare.png
categories: [前端日誌]
tags: [網站, Github]
excerpt: 在我們使用 Github Pages 架設靜態網站時，常常都會看到 (github.io) 這種攏長的網址，那要如何擁有一個像平常一樣簡短又方便的域名呢，本篇文章將一步一步帶你了解如何從 Freenom 開始註冊並將域名套用到 Github Pages 上。
---

# 前言

在我們使用 Github Pages 架設靜態網站時，常常都會看到 (github.io) 這種攏長的網址，那要如何擁有一個像平常一樣簡短又方便的域名呢，本篇文章將一步一步帶你了解如何從 Freenom 開始註冊並將域名套用到 Github Pages 上。

<!-- more -->

# Freenom

<p class="note note-info">Freenom官網：<a href="https://www.freenom.com/" style="color: #1589E9;">https://www.freenom.com</a></p>

## Freenom 註冊

- Freenom 提供的免費網域有
  - `tk`
  - `ml`
  - `ga`
  - `cf`
  - `cq`

![](https://media.discordapp.net/attachments/418758998175776778/1001132812377796628/unknown.png?width=1714&height=905)

<figcaption aria-hidden="true" class="image-caption">官網首頁圖 | 來源 : 截圖</figcaption>

進到 Freenom 官網後，於上方搜索欄輸入

```txt
你想註冊的網域名稱.(tk/ml/ga/cf/cq)
```

<br />

並點擊 <span style="color: orange;">檢查可用性</span> 按鈕，本範例將以 `weakcat.tk` 作為示範。
![](https://media.discordapp.net/attachments/418758998175776778/1001137247199961108/unknown.png?width=1710&height=905)

確認可用後，點擊右上角付款，
接著選取 `12 Months @ FREE` 的選項。
![](https://media.discordapp.net/attachments/418758998175776778/1001138742578389112/unknown.png)
並點選 Continue 繼續，
接著下方會出現註冊的選項，填選完後便會跑到下方頁面。
![](https://media.discordapp.net/attachments/418758998175776778/1001141405739143260/unknown.png)

<p class="note note-success">盡量使用英文填寫</p>
完成後勾選 I have read and agree to the <a href="https://www.freenom.com/en/termsandconditions.html">Terms & Conditions</a> 並點擊 <span style="color: orange;">Complete Order</span>，便註冊完成。

![](https://media.discordapp.net/attachments/418758998175776778/1001173741310574592/unknown.png)

# Cloudflare

<p class="note note-info">Cloudflare官網：<a href="https://www.cloudflare.com/zh-tw/" style="color: #1589E9;">https://www.cloudflare.com/zh-tw</a></p>

## Cloudflare 註冊

![](https://media.discordapp.net/attachments/418758998175776778/1001728107260149840/unknown.png?width=1322&height=671)

<figcaption aria-hidden="true" class="image-caption">官網首頁圖 | 來源 : 截圖</figcaption>

進入官網後，點擊右上角 <span style="color: orange;">註冊按鈕</span>，並輸入郵件與信箱即可完成註冊。

## Cloudflare 設置

![](https://media.discordapp.net/attachments/418758998175776778/1001729896852238447/unknown.png)
點選左側 <span style="color: orange;">Website</span>，並點選中央的 <span style="color: orange;">Add Site</span> 按鈕。
![](https://media.discordapp.net/attachments/418758998175776778/1001730197369933896/unknown.png)
輸入剛剛於 Freenom 註冊的網域，範例為 : `weakcat.tk`。並點選 Add Site。
![](https://media.discordapp.net/attachments/418758998175776778/1001745613739794502/unknown.png)

### 選擇方案

![](https://media.discordapp.net/attachments/418758998175776778/1001747440728285224/unknown.png?width=661&height=671)
選擇下方的 <span style="color: orange;">Free 方案</span>，並點擊 <span style="color: orange;">Continue</span>。
![](https://media.discordapp.net/attachments/418758998175776778/1001748147573358642/unknown.png)
![](https://media.discordapp.net/attachments/418758998175776778/1001748476520046612/unknown.png)
我們先不設定 DNS Records 因此點擊 <span style="color: orange;">Continue</span> 和 <span style="color: orange;">Confirm</span>。

### Nameservers

![](https://media.discordapp.net/attachments/418758998175776778/1001748752060653628/unknown.png)
複製上方兩段的 Nameservers，並回到 Freenom 域名頁面。
![](https://media.discordapp.net/attachments/418758998175776778/1001749143397613608/unknown.png)
於 <span style="color: orange;">Management Tools</span> 選單中，點選 <span style="color: orange;">Nameservers</span> 選項。
![](https://media.discordapp.net/attachments/418758998175776778/1001749488748216361/unknown.png)
選擇 <span style="color: orange;">Use custom nameservers</span> 選項，並於下方輸入兩個 Cloudflare 指定的 Nameservers。
保存後回到 Cloudflare 頁面，點擊 <span style="color: orange;">Done, check nameservers</span>。
![](https://media.discordapp.net/attachments/418758998175776778/1001750363453542462/unknown.png)
接著點擊 <span style="color: orange;">Configuration recommendations</span>。
![](https://media.discordapp.net/attachments/418758998175776778/1001750602403033188/unknown.png)
點選右側的兩個 <span style="color: orange;">Apply recommendation</span> 按鈕，並回到主畫面。
![](https://media.discordapp.net/attachments/418758998175776778/1001750857425108992/unknown.png)

<p class="note note-warning">檢查 Nameservers 需要一些時間，不過我大概 5 分鐘就好了。 <br />
下圖為已驗證成功的範例。 <img src="https://media.discordapp.net/attachments/418758998175776778/1001751340990615602/unknown.png" /></p>

# Github Pages

接下來我們便要設置靜態網頁的部分，首先你會需要一個寫好的網頁。
以下為我使用的範例。

### 網頁 Code

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8" />
    <meta name="theme-color" content="#000000" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <link rel="stylesheet" href="./style.css" />
    <title>WeakCat | 測試網站</title>
  </head>
  <body>
    <div class="wrapper">
      <h1 class="text">Hello World!</h1>
    </div>
  </body>
</html>
```

```css
* {
  margin: 0;
  padding: 0;
  font-family: "Open Sans", sans-serif;
}

.wrapper {
  width: 100vw;
  height: 100vh;
  margin: auto;
  display: flex;
  justify-content: center;
  align-items: center;
}

.text {
  text-align: center;
  font-size: 100px;
}
```

### Github 倉庫

![](https://media.discordapp.net/attachments/418758998175776778/1002826727971631164/unknown.png?width=1656&height=904)
首先我們要創建一個新的倉庫來放我們網頁的檔案，名稱隨意，一定要設 <span style="color: orange;">Public</span>。
![](https://media.discordapp.net/attachments/418758998175776778/1003344005259612272/unknown.png)
接著依據指示在網頁資料夾中操作，並將檔案上傳到 Github 倉庫中。

```bash
git init
git add .
git commit -m "Basic Files"
git branch -M main
git remote add origin (https://github.com/CuteWhiteCat/test-website.git)
git push -u origin main
```

上傳完畢後，重新載入頁面，即可看到上傳完成的檔案。
![](https://media.discordapp.net/attachments/418758998175776778/1003345345008369734/unknown.png?width=1851&height=905)

### Github Pages

![](https://media.discordapp.net/attachments/418758998175776778/1003345884324573224/unknown.png?width=401&height=904)
接著點選頁面上方的 <span style="color: orange;">Settings</span>，並點選左欄的 <span style="color: orange;">Pages</span>。
![](https://media.discordapp.net/attachments/418758998175776778/1003346144333668393/unknown.png)
在 Branch 欄位選擇 <span style="color: orange;">main</span> 並點下 Save 按鈕。
等待幾分鐘後，刷新頁面，即可看到網頁成功部屬的信息。
![](https://media.discordapp.net/attachments/418758998175776778/1003347355627696238/unknown.png)

### Custom Domain
現在我們要設置自訂義域名的部分
首先回到 <span style="color: orange;">Cloudflare 頁面</span>，並點選左欄的 <span style="color: orange;">DNS</span>。
![](https://media.discordapp.net/attachments/418758998175776778/1003348036392591440/unknown.png)
點擊 <span style="color: orange;">Add record</span> 按鈕，並新增下列的 Records。
```txt
A - 185.199.108.153
A - 185.199.109.153
A - 185.199.110.153
A - 185.199.111.153
AAAA - 2606:50c0:8000::153
AAAA - 2606:50c0:8001::153
AAAA - 2606:50c0:8002::153
AAAA - 2606:50c0:8003::153
CNAME - www 用戶名.github.io.
[子域名新增 : (CNAME - 子域名名稱 用戶名.github.io.)]
```
如下圖。
![](https://media.discordapp.net/attachments/418758998175776778/1003349362308563014/unknown.png)
接著回到 <span style="color: orange;">Github 倉庫 -> Settings -> Pages</span>。
在 <span style="color: orange;">Custom domain</span> 處，填上你的自訂義域名，範例為 : `weakcat.tk`。
點擊 <span style="color: orange;">Save</span> 後，耐心等待一段時間。
![](https://media.discordapp.net/attachments/418758998175776778/1003350207347576862/unknown.png)
等到網頁出現 <span style="color: #57AB5A;">✔ DNS check successful</span> 後，便能使用自訂義域名連上你的網站了!
![](https://media.discordapp.net/attachments/418758998175776778/1003351045348524064/unknown.png)
![](https://media.discordapp.net/attachments/418758998175776778/1003351255382503464/unknown.png?width=1669&height=905)
<figcaption aria-hidden="true" class="image-caption">測試網站圖 | 來源 : 截圖</figcaption>

# 成果
<div>&nbsp;&nbsp;&nbsp;🔗 <a href="https://weakcat.tk" style="color: #1589E9;">weakcat.tk</a></div>