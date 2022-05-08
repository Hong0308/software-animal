---
title: "API 網址這樣設定有夠棒！"
date: 2021-04-16T15:58:45+08:00
draft: false
tags: ["API"]
categories: ["API"]
---

網址是 API 的門面，大家使用 **API** 的第一步就是要看它，所以第一眼就要讓人就知道這隻 API 在做什麼？
甚至因為遵循標準（目前 **REST** 是主流），可以類推 **API** 應該會有什麼功能等等。

網址規劃的好，未來隨著需求變化也比較有彈性能夠修改 / 擴充。

![](https://images.unsplash.com/photo-1617854818583-09e7f077a156)

## 網址設定跟著這些原則走，輕鬆沒煩惱

### 1. 命名簡單明瞭

https://api.test.com/products/ **1234** 這個網址代表是一個 api 的位置，這會取得編號 **1234** 的商品資料 (products)

### 2. 不要使用過度簡化的單詞

https://api.test.com/ **p** /666 這邊 **p** 代表是 products 嗎？還是 plan ?

### 3. 以小寫英文為主

因為有些系統會識別大小寫英文（代表不同的東西：例如： Products vs. products 視為不同）

另外，國際主流語言還是以英文為主（畢竟電腦也是美國發明的～）

### 4. 避免使用自定義名詞

- https://api.test.com/free_choice/555 餐餐自由選？

- https://api.test.com/tuango/888 團購商品？

### 5. 使用複數名詞命名

這個牽涉到 REST 的設計原則：如果沒有帶識別詞（例如：編號）就等同於取得列表

> https://api.test.com/products

取得商品列表（一坨商品）

> https://api.test.com/products/1234

取得編號 **1234** 的商品資料（一個商品）

---

另外，使用名詞也是因為 REST 的原則而設計：動作應該由 HTTP 請求的 [方法] 決定

> [GET] https://api.test.com/products

取得商品資料

> [POST] https://api.test.com/products

新增商品資料

> [PUT] https://api.test.com/products/1234

更新商品資料（全部欄位）

> [DELETE] https://api.test.com/products/1234

刪除商品資料

> [PATCH] https://api.test.com/products/1234

更新商品資料（部分欄位）

### 6. 避免使用特殊符號

特殊符號可能會造成網址編碼上的問題，產生非預期的結果，不過現在瀏覽器很聰明都會幫忙[轉碼](https://en.wikipedia.org/wiki/Percent-encoding)。

但是，有些特殊符號是有特別意義的，例如：點 ( **.** ) 拿來區分網域、連接符號 ( **&** ) 用來連接 [GET] 複數參數用
