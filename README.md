# today
 
历史上的今天

[示例网页](xxx)

### 结构

`data` 为根目录, 目前有 `anime` 和 `meme` 两个子类

子类下的日期按照`mm-dd`格式排序, 日期文件夹内储存当日事件数据

事件数据为 `json` 格式, 标准如下: 

(以 `data/meme/05-24/cherry.json` 为例)

```
{
    "id": "cherry",
    "res": ".png",
    "date": "2016-5-24",
    "title": "陈睿 —— b站未来有可能会倒闭，但绝不会变质。"
}
```

- `id`: 用于识别此事件, 同一日期下不能重复
- `res`: 资源文件(图片格式); 可简写为拓展名(`".png"`等价于`"cherry.png"`)
- `date`: 日期, `yyyy-mm-dd` 格式
- `title`: 事件描述，自由发挥

各级目录下由`index.json`索引

### 提交

对事件进行~~垃圾~~分类是非常麻烦的, 本项目由机器人完成自动分类

在子类下有`autoFile`目录, 可以直接提交更改到此目录

机器人会在几秒钟内自动将事件移动到正确目录