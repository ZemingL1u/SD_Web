---
title: SD_Test
language_tabs:
  - shell: Shell
  - http: HTTP
  - javascript: JavaScript
  - ruby: Ruby
  - python: Python
  - php: PHP
  - java: Java
  - go: Go
toc_footers: []
includes: []
search: true
code_clipboard: true
highlight_theme: darkula
headingLevel: 2
generator: "@tarslib/widdershins v4.0.20"

---

# SD_Test

Base URLs:

# Authentication

# Default

## POST 文生图接口

POST /txt2img

文生图API
请求路径：/txt2img 【POST】
参数格式：JSON

> Body Parameters

```json
{
  "seed": "reprehenderit ut"
}
```

### Params

|Name|Location|Type|Required|Title|Description|
|---|---|---|---|---|---|
|body|body|object| no ||none|
|» id|body|string| yes | 用户id|none|
|» prompt|body|string| yes | 正向提示词|none|
|» negative_prompt|body|string| yes | 反向提示词|none|
|» width|body|integer| yes | 宽|none|
|» height|body|integer| yes | 高|none|
|» seed|body|string| yes | 种子|none|
|» steps|body|integer| yes | 采样步数|none|
|» hr_upscaler|body|string| yes | 高清化采样器|none|
|» cfg_scale|body|integer| yes | 提示词关联程度|none|
|» style|body|string| yes | 风格|none|
|» batch_size|body|integer| yes | 作图数量|none|

> Response Examples

> 200 Response

```json
{}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功|Inline|

### Responses Data Schema

## POST 图生图接口

POST /img2img

图生图API
请求路径：/txt2img 【POST】
参数格式：JSON

> Body Parameters

```json
{
  "seed": "reprehenderit ut"
}
```

### Params

|Name|Location|Type|Required|Title|Description|
|---|---|---|---|---|---|
|body|body|object| no ||none|
|» id|body|string| yes | 用户id|none|
|» prompt|body|string| yes | 正向提示词|none|
|» negative_prompt|body|string| yes | 反向提示词|none|
|» width|body|integer| yes | 宽|none|
|» height|body|integer| yes | 高|none|
|» init_images|body|string| yes | 参考图|none|
|» seed|body|string| yes | 种子|none|
|» steps|body|integer| yes | 采样步数|none|
|» hr_upscaler|body|string| yes | 高清采样器|none|
|» cfg_scale|body|integer| yes | 提示词关联程度|none|
|» style|body|string| yes | 风格|none|
|» batch_size|body|integer| yes | 作图数量|none|

> Response Examples

> 200 Response

```json
{}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功|Inline|

### Responses Data Schema

## GET 查询文生图记录

GET /t2ihistory/{id}

查询文生图记录
请求路径：/t2ihistory/{id}  【GET】
请求格式：Params

### Params

|Name|Location|Type|Required|Title|Description|
|---|---|---|---|---|---|
|id|path|string| yes ||用户id|

> Response Examples

> 200 Response

```json
{}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功|Inline|

### Responses Data Schema

## GET 查询图生图记录

GET /i2ihistory/{id}

查询图生图记录
请求路径：/i2ihistory/{id}  【GET】
请求格式：Params

### Params

|Name|Location|Type|Required|Title|Description|
|---|---|---|---|---|---|
|id|path|string| yes ||用户id|

> Response Examples

> 200 Response

```json
{}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功|Inline|

### Responses Data Schema

## GET 请求图片

GET /get_images/{id}/{type}/{filename}

请求图片
请求路径：/get_images/{id}/{type}/{filename}  【GET】
请求格式：Path Params

### Params

|Name|Location|Type|Required|Title|Description|
|---|---|---|---|---|---|
|id|path|string| yes ||用户id|
|type|path|string| yes ||none|
|filename|path|string| yes ||图片相对id目录的路径|

> Response Examples

> 200 Response

```json
{}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功|Inline|

### Responses Data Schema

## GET 请求作图参数

GET /get_args/{id}/{type}/{filename}

请求图片
请求路径：/get_args/{id}/{type}/{filename}  【GET】
请求格式：Path Params

### Params

|Name|Location|Type|Required|Title|Description|
|---|---|---|---|---|---|
|id|path|string| yes ||用户id|
|type|path|string| yes ||作图类型|
|filename|path|string| yes ||图片相对id目录的路径|

> Response Examples

> 200 Response

```json
{}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功|Inline|

### Responses Data Schema

## DELETE 删除作图记录

DELETE /delete/{id}/{type}/{filename}

删除作图记录
请求路径：/delete/{id}/{type}/{filename}  【DELETE】
请求参数：Params

### Params

|Name|Location|Type|Required|Title|Description|
|---|---|---|---|---|---|
|id|path|string| yes ||用户id|
|type|path|string| yes ||作图类型|
|filename|path|string| yes ||记录名|

> Response Examples

> 200 Response

```json
{}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功|Inline|

### Responses Data Schema

# Data Schema

