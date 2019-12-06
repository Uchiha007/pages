---
title: "Elasticsearch 之范围查询"
date: 2019-12-04T09:28:55+08:00
draft: false 
---

#### 范围查询
匹配字段在某一特定范围的文档。Lucene 查询取决于字段类型，对于字符串字段使用 `TermRangeQuery`，数字/日期类型使用 `NumericRangeQuery`。下面示例将返回 `age` 在 10 到 20 之间所有的文档。

```shell
curl -X GET "localhost:9200/_search?pretty" -H 'Content-Type: application/json' -d'
{
    "query": {
        "range" : {
            "age" : {
                "gte" : 10,
                "lte" : 20,
                "boost" : 2.0
            }
        }
    }
}
'
```

```json
GET _search
{
    "query": {
        "range" : {
            "age" : {
                "gte" : 10,
                "lte" : 20,
                "boost" : 2.0
            }
        }
    }
}
```
```golang
// 测试
fmt.Println("xxx")
```

```
color:#f8f8f2;background-color:#272822;-moz-tab-size:4;-o-tab-size:4;tab-size:4
```