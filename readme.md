## 功能
从思源的源代码仓库拉取代码,然后一通鼓捣生成一个api列表类

## 使用

如果你担心列表不够新的话,运行

```js
npm run gen
```
会生成一个新的index.js

生成之后


```js
import kernelAPI from '@siyuan-community/kernelapilist' 
//返回一个初始化好的后端接口列表对象
kernelAPI.sql()
```

或者你自己配置思源的地址

```js 
import {kernelApiList} from '@siyuan-community/kernelapilist' 
let 核心api = new kernelApiList(
            思源伺服ip:window.location.hostname,
        思源伺服端口:'',
        思源伺服协议:"http",
		apitoken:""

)
await 核心api.重命名文档({
  "notebook": "20210831090520-7dvbdv0",
  "path": "/20210902210113-0avi12f.sy",
  "title": "文档新标题"
})

```

或者这样也行

```js 
import {kernelApiList} from '@siyuan-community/kernelapilist' 
let kernelApi = new kernelApiList(
        siYuanIp:window.location.hostname,
        siYuanPort:'',
        siYuanScheme:"http",
		apitoken:""

)
kernelApi.renameDoc(
    {
          "notebook": "20210831090520-7dvbdv0",
  "path": "/20210902210113-0avi12f.sy",
  "title": "文档新标题"
    },
    '',
    (data)=>{
        console.log(data)
    }

)
```
或者把index.js拿出去用也可以

## 如果这玩意对你有用

可以去[我的爱发电](https://afdian.net/a/leolee9086)给我买杯咖啡