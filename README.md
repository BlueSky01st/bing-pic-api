# Bing图片 API


> Bing API 接口文档

## 使用方法
<hr/>

安装node.js

```bash
npm install #安装依赖项

npm start #运行
```


## 特性
<hr />

- Bing原生返回值
- 支持json格式
- 支持xml格式
- 支持自定义返回图片数量（max16）



## 接口
<hr />


#### 原生Bing返回接口

> 调用地址：`/bing?{format,idx,n}`
>
> 方式：`GET`

| 参数名 | 是否必要 |                    备注                    |
| :----: | :------: | :----------------------------------------: |
| format |    否    | 默认返回json，若需要xml，则指定值为xml即可 |
|  idx   |    是    |  图片偏移天数，例如为1，则返回昨天的图片   |
|   n    |    是    |      返回图片数量，最大为16，最小为1       |



#### 查看今日图片

>访问地址：`/showtoday`
>
>方式`GET`

无参数



#### Bing今日图片地址

> 调用地址： `/today?{res, cus}`
>
> 方式： `GET`

| 参数 | 是否必要 | 备注                                                      |
| ---- | -------- | --------------------------------------------------------- |
| id   | 否       | 输入分辨率的ID值，ID值查看下表即可，**默认返回1920x1080** |
| res  | 否       | 此值接受一个分辨率值，例如：1366x768。                    |

**<span style="color:red">注意：res值存在时，id参数失效。且res的值必须为下表中存在的值</span>**



- ##### 分辨率ID表

| 分辨率ID | 分辨率    |
| -------- | --------- |
| 0        | 1920x1200 |
| 1        | 1920x1080 |
| 2        | 1366x768  |
| 3        | 1280x768  |
| 4        | 1240x768  |
| 5        | 800x600   |
| 6        | 800x480   |
| 7        | 640x480   |
| 8        | 400x240   |
| 9        | 320x240   |
| 10       | 768x1280  |
| 11       | 720x1280  |
| 12       | 480x800   |

