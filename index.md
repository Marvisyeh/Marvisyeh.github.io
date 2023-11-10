---
layout: default
---
### ETL Pipeline with Apache Airflow
這個專案使用Apache Airflow建立一個ETL管道。主要目標是從中央氣象署接取36小時的天氣預報、轉換成需求的格式，然後寫入PostgresSQL資料庫中。

#### 資料管線設計
<img src="assets\img\airflow.png"/>
<p></p>

管線包含以下Task:
1. extract_data_from_api: <br>
    使用Python Operator，向API請求台北市天氣資訊，並將資料存成Json檔案。

2. transform_data_use_pandas： <br>
    一樣使用Python Operator，將檔案整理成需要的格式，最後寫成SQL script。

3. write_to_sqlserever： <br>
    Postgres Operator，執行SQL script 將資料更新到資料庫中。


### 資料倉儲架設
因應分析需求日益增長，為了維護交易資料庫的效能、降低其負擔，建立資料倉儲。

#### DataFlow
<img src="assets\img\datamart.png"/>

#### Data Modeling
<img src="assets\img\data_modeling.png"/>

[![](https://img.shields.io/badge/Python-lightgrey?logo=Python)](#) 
[![](https://img.shields.io/badge/MySQL-lightgrey?logo=MySQL)](#)
[![](https://img.shields.io/badge/Trinity-lightgrey?logo=Trinity)](#)



### Side-Project｜FindGoods 找好家飾
疫情改變了消費型態，線上購物成為人們生活的一部分，時常的遠端工作提升了家居環境佈置的關注，我們設計了一個電商整合網站，除了讓使用者可以掌握當下流行趨勢外，也結合了ＡＩ應用「個人化的商品推薦」和「以圖搜圖」功能，希望幫助大家更快速、方便找到想要的傢飾品。
[View code on Github](https://github.com/Marvisyeh/FindGoods-web)

<img src="assets\img\findgood-dataflow.png"/>
<p></p>
<img src="assets\img\findgood-structure.png"/>


[![](https://img.shields.io/badge/Python-lightgrey?logo=Python)](#) 
[![](https://img.shields.io/badge/Flask-lightgrey?logo=flask)](#)
[![](https://img.shields.io/badge/Mongodb-lightgrey?logo=mongodb)](#)
[![](https://img.shields.io/badge/MySQL-lightgrey?logo=MySQL)](#)
[![](https://img.shields.io/badge/sklearn-lightgrey?logo=scikit-learn)](#) 


<!-- 

[Link to another page](./another-page.md)


```
Long, single-line code blocks should not wrap. They should horizontally scroll if they are too long. This line should be long enough to demonstrate this.
```

```
The final element.
``` -->
