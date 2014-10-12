## wechat-tools 让您的公众平台有可以回复‘天气预报’、‘历史上的今天’ 等

推荐微信公众平台的开发者配合使用 [node-webot/wechat](https://github.com/node-webot/wechat)

## 安装
```
npm install wechat-tools -save;
```
### 1 生成可以直接回复的‘天气预报’
此为共享 ak = uD67wmZzhi3RFcmTkGoks2Dr,实际应用时建议去[百度开发者](http://developer.baidu.com/map/index.php)自行申请ak

```
var wt = request('wechat-tools');
var ak = 'uD67wmZzhi3RFcmTkGoks2Dr';//
var city = '北京';
wt.weather(ak,city,function(err , data){
    if(err){
      throw err;
    }else{
     console.log(data);
   }
});
```
#### console.log(data); 结果如下图
![参考图片](http://pistatic.qiniudn.com/images/weather01.png?imageView2/1/w/500/)
### 2 生成可以直接回复的‘历史上的今天’
```
wt.history(function (err,data) {
    if(err){
      throw err;
    }else{
      console.log(data);
    }
  })
```
#### console.log(data); 结果如下图
![参考图片](http://pistatic.qiniudn.com/images/history01.png?imageView2/1/w/400/)
##  应用
![参考图片](http://pistatic.qiniudn.com/images/history-code.jpg?imageView2/1/w/300/)