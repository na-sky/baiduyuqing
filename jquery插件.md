

## cdn (content deliver network) 内容分发网络

如果百度使用了'某个'cdn中的jquery.js,而且用户打开过百度，
我们自己同样使用了'同一个'cdn中的jquery.js,
用户打开


利用jquery的fullpage插件制作宣传展示页的流程

## 一.引入插件



##  三.开始制作页面

要制作的页面有自己各种需求，需要给插件添加一些配置项

```javascript
$('#fullpage').fullpage({

//滚动一屏需要的时间
  scrollingSpeed:1440,

//index.html#jiewei(分享给别人)
   给每一屏起个名字
  anchors:['youxiang','guangwang','jiewei']
//需要固定定位的元素
  fixedElements:'fix nav';
//当滚到顶部或底部能否继续滚动
  continuousVertical:true;

//是否出现导航小点
 navigation:true;
 navigationPosition:left;
//每一个小点提示文字
navigationTooltips:['a','b''c']
showActiveTooltip:true;



//进入一屏时会调用
  afterLoad:function(name,index){
    name:名字;
    index:第几页;
  }
  onLeave:function(index,next,dir){
    index:从那张离开;
    next:去到那张;
    dir:方向 up 和 down;
  }    

});


## 四.使用css结合js去制作页面动画

  一.使用 transition 结合 fullpage 去制作动画

  ```css
  transition:transform .5s ease 1s,opacity .6s ease;
  transform:rotateX() scale(0.3,0.3);
  transform:translate3d(20px,30px,0);
  ```

  1.要动的元素写到一个section
  2.正常状态下是一种样式
  3.当有