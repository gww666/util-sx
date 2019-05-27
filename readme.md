### 常用方法整理
* 日期类
    * [时间戳格式化为yy-mm-dd hh-mm-ss格式](#时间戳格式化为yy-mm-dd&nbsp;hh-mm-ss格式)
* 线程类
    * [线程休眠指定时间](#线程休眠指定时间)
&nbsp;&nbsp;  
&nbsp;&nbsp;  
&nbsp;&nbsp;  
&nbsp;&nbsp;  
### 日期类
#### 时间戳格式化为yy-mm-dd&nbsp;hh-mm-ss格式
  ```javascript
const formatDate = (time) => {
    if (typeof time === "string") time = Number(time);
    let date = new Date(time);
    let year = date.getFullYear();
    let month = date.getMonth() + 1 > 9 ? date.getMonth() + 1 : "0" + (date.getMonth() + 1);
    let day = date.getDate() > 9 ? date.getDate() : "0" + date.getDate();
    let hour = date.getHours() > 9 ? date.getHours() : "0" + date.getHours();
    let minutes = date.getMinutes() > 9 ? date.getMinutes() : "0" + date.getMinutes();
    return `${year}-${month}-${day} ${hour}:${minutes}`;
}
```
&nbsp;&nbsp;  
&nbsp;&nbsp;  
### 线程类
#### 线程休眠指定时间
  ```javascript
const sleep = (time) => {
    return new Promise(resolve => {
        setTimeout(resolve, time);
    });
}
```
