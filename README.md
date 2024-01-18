# 祁七七今天唱什么
https://shuvi.moe/77ovo/
## 歌单来源
|名称|地址|最后检查|数量|
|-----|-----|-----|-----|
|七七的翻唱~|https://space.bilibili.com/3493137920035605/channel/collectiondetail?sid=1535671&ctype=0|2024-01-19|26|
|祁七七的直播翻唱合集|https://space.bilibili.com/47275989/channel/seriesdetail?sid=3580738|2024-01-19|998|
## 相关脚本
```javascript
let xhr = new XMLHttpRequest()
xhr.open('GET', `https://api.bilibili.com/x/web-interface/view?bvid=${bvid}`, false)
xhr.send()
let pages = JSON.parse(xhr.responseText).data.pages
// pages.shift()
pages.map(a=>{return {title:a.part.match('《(.*?)》')[1],bvid:bvid,page:a.page}})
```
