# 編目與館藏

## 編目與館藏之別

編目（Catalog）是圖書館紀錄一本書的資料，同一本書只會有一筆編目資料；館藏（Item）是在圖書館中的書的資料，一本館藏依賴於一個編目資料，一個編目可以有多本館藏，只有館藏可以被借還書。

編目資料使用 MARC 編目格式儲存，紀錄書名、作者、出版社、ISBN 等等的資料。館藏資料則是紀錄在哪個分館、索書號（Call Number）、登錄號（Barcode）。

### 編目格式 MARC

編目資料在資料庫是以 MARC 編目格式進行儲存的，它是以 **數字$英文字符** 作為欄位，舉例書名的欄位是 **245$a**、作者欄位是 **245$c**。在 Koha 中是直接操作 MARC 的欄位，因此在編目過程需要記得各個欄位對應的資料，常用資料列表將列在下方。

**本圖書館採用 MARC 21 編目格式。**

## 單筆新增編目

### Z39.50 查詢書目

> 注意：在開始使用 Z39.50 前，須先設定好外部標的。請參考 [設定篇](config.md)

進入 更多 / 編目，點選新增自 Z39.50/SRU （也可從 MARC 編輯頁面中進入）。

輸入查詢的內容，並勾選搜尋標的（即將搜尋之圖書館），此例為搜尋 *你的孩子不是你的孩子* 一書。

![Z39.50 查詢畫面](image/z39.50-1.png)

如果成功搜尋到內容，將會看到以下頁面：

![z39.50-2](image/z39.50-2.png)

選擇要使用的書目資料，點選卡片格式預覽即可看到書目資料。

![卡片格式預覽](image/z39.50-3.png)

如果確認資料無誤，即可點擊 **匯入**，開始編輯 MARC 資料。查詢到的資料內容即可匯入到欄位中，大大節省編目的時間。

------

先進入 更多 / 編目（More / Cataloging），點選**新增紀錄（add record）**，然後選擇框架，先選擇預設框架。

![編目頁面](image/catalog.png)

![新增 MARC 紀錄](image/catalog-new-marc.png)

我們開始在指定欄位填入資料

| 欄位  | 內容                  |
| ----- | --------------------- |
| 020$a | ISBN                  |
| 020$c | 定價                  |
| 090$a | 分類號                |
| 245$a | 題名（書名）          |
| 245$b | 副題名                |
| 245$c | 作者（譯者）          |
| 260$a | 出版地                |
| 260$b | 出版者                |
| 260$c | 出版日期              |
| 490$a | 集叢名                |
| 650$a | 標題（主題標籤）      |
| 942$c | 館藏類型（Koha 專用） |

填寫完畢後，點按**儲存並編輯館藏（Save and Edit items）**加入一筆館藏紀錄。

![加入館藏](image/add-items.png)



館藏紀錄須填入下列資料：

* 2 - Source of classification or shelving scheme：分類法
* Permanent location：主要分館
* Current location：現在所在分館
* Full call number：索書號
* Barcode：登錄號
* Koha Item type：Koha 中的館藏類型

然後按下儲存即可新增一筆館藏紀錄

![編目記錄完成](image/details.png)

# 參考資料

[MARC 21 欄位對應 RDA](http://klkly23.pixnet.net/blog/post/176271744-%E8%B3%87%E8%A8%8A%E7%B5%84%E7%B9%94-%E5%8F%83%E8%B3%87marc-21%E6%AC%84%E4%BD%8D%E5%B0%8D%E6%98%A0rda)

[Koha Manual - Cataloging]()

[Koha 圖書館員手冊](http://lins.fju.edu.tw/mao/koha/libraiansmanual.html)

[加入 Z39.50 伺服器](https://www.youtube.com/watch?v=G5_H4YsgHX4)

