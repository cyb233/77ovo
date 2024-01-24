# [祁七七](https://live.bilibili.com/27573773)今天唱什么
https://shuvi.moe/77ovo/
## 歌单来源
|名称|最后检查|歌曲/视频数量|
|-----|-----|-----|
|[七七的翻唱~](https://space.bilibili.com/3493137920035605/channel/collectiondetail?sid=1535671&ctype=0)|2024-01-24|27|
|[祁七七的直播翻唱合集](https://space.bilibili.com/47275989/channel/seriesdetail?sid=3580738)|2024-01-24|1112|
|[祁七七的动态歌单](https://t.bilibili.com/814493547863474280)|2024-01-19|184|
## 相关脚本
### 合集
```javascript
let xhr = new XMLHttpRequest()
xhr.open('GET', `https://api.bilibili.com/x/polymer/web-space/seasons_archives_list?mid=${uid}&season_id=${sid}&sort_reverse=false&page_num=1&page_size=100`, false)
xhr.send()
let archives = JSON.parse(xhr.responseText).data.archives
archives.map(a=>{return {title:a.title,bvid:a.bvid}})
```
### 分P
```javascript
let xhr = new XMLHttpRequest()
xhr.open('GET', `https://api.bilibili.com/x/web-interface/view?bvid=${bvid}`, false)
xhr.send()
let pages = JSON.parse(xhr.responseText).data.pages
// pages.shift()
pages.map(a=>{return {title:a.part.match('《(.*?)》')[1],bvid:bvid,page:a.page}})
```
