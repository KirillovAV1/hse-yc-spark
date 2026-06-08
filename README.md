# Домашнее задание #1 Yandex-Cloud, Apache Spark

## 1. Создание данных.

Для создания данных использовался код, представленный в pdf/app.holst.so

```python
%spark.pyspark
from pyspark.sql import functions as F
users = spark.createDataFrame(
    [
        ("u1", "Berlin"),
        ("u2", "Berlin"),
        ("u3", "Munich"),
        ("u4", "Hamburg"),
    ],
    ["user_id", "city"]
)
orders = spark.createDataFrame(
    [
        ("o1", "u1", "p1", 2, 10.0),
        ("o2", "u1", "p2", 1, 30.0),
        ("o3", "u2", "p1", 1, 10.0),
        ("o4", "u2", "p3", 5, 7.0),
        ("o5", "u3", "p2", 3, 30.0),
        ("o6", "u3", "p3", 1, 7.0),
        ("o7", "u4", "p1", 10, 10.0),
    ],
    ["order_id", "user_id", "product_id", "qty", "price"]
)
products = spark.createDataFrame(
    [
        ("p1", "Ring VOLA"),
        ("p2", "Ring POROG"),
        ("p3", "Ring TISHINA"),
    ],
    ["product_id", "product_name"]
)
```

## 2. Подсчет revenue

<img width="366" height="196" alt="image" src="https://github.com/user-attachments/assets/0c91df8d-57a5-4308-9766-212943f627b4" />

## 3. Объединение orders с другими таблицами

<img width="515" height="189" alt="image" src="https://github.com/user-attachments/assets/cfc8dfc7-fc19-4fae-b9fd-be3aace6b309" />

## 4. Подсчет метрик

<img width="483" height="174" alt="image" src="https://github.com/user-attachments/assets/ba1a322d-8536-4b90-8cdd-d8d9639b3259" />

## 5. Запись результатов в S3/HDFS

<img width="1188" height="570" alt="image" src="https://github.com/user-attachments/assets/59989269-9dc2-498c-bc35-033373f5636c" />

<img width="1489" height="362" alt="image" src="https://github.com/user-attachments/assets/6baa4051-fa13-484c-b202-2ab66a4977b2" />

## 6. Считывает и показ топ-результатов

<img width="532" height="162" alt="image" src="https://github.com/user-attachments/assets/60cef793-2bfc-40c0-af6d-e2941b2a959f" />
