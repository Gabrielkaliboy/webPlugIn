1.文件说明：阿里的轮播图，全响应式的，有多种配置接口
2.插件地址：http://www.jq22.com/jquery-info366
3.兼容性：IE6/7/8/9/10/11 Firefox   Chrome  Safari
4.实现方法
引用js
```html
<script type="text/javascript" src="js/jquery-1.7.2.min.js"></script>
<script type="text/javascript" src="js/jquery.flexslider-min.js"></script>
```
html
```html
<div class="flexslider">
    <ul class="slides">
        <li style="background:url(images/img1.jpg) 50% 0 no-repeat;"></li>
        <li style="background:url(images/img2.jpg) 50% 0 no-repeat;"></li>
        <li style="background:url(images/img3.jpg) 50% 0 no-repeat;"></li>
        <li style="background:url(images/img4.jpg) 50% 0 no-repeat;"></li>
        <li style="background:url(images/img5.jpg) 50% 0 no-repeat;"></li>
    </ul>
</div>
```
css
```css
<style type="text/css">
*{margin:0;padding:0;list-style-type:none;}
a,img{border:0;}
body{font:12px/180% Arial, Helvetica, sans-serif, "新宋体";}
 
/* flexslider */
.flexslider{position:relative;height:400px;overflow:hidden;background:url(images/loading.gif) 50% no-repeat;}
.slides{position:relative;z-index:1;}
.slides li{height:400px;}
.flex-control-nav{position:absolute;bottom:10px;z-index:2;width:100%;text-align:center;}
.flex-control-nav li{display:inline-block;width:14px;height:14px;margin:0 5px;*display:inline;zoom:1;}
.flex-control-nav a{display:inline-block;width:14px;height:14px;line-height:40px;overflow:hidden;background:url(images/dot.png) right 0 no-repeat;cursor:pointer;}
.flex-control-nav .flex-active{background-position:0 0;}
 
.flex-direction-nav{position:absolute;z-index:3;width:100%;top:45%;}
.flex-direction-nav li a{display:block;width:50px;height:50px;overflow:hidden;cursor:pointer;position:absolute;}
.flex-direction-nav li a.flex-prev{left:40px;background:url(images/prev.png) center center no-repeat;}
.flex-direction-nav li a.flex-next{right:40px;background:url(images/next.png) center center no-repeat;}
</style>
```
js初始化
```javascript
<script type="text/javascript">
$(document).ready(function(){
    $('.flexslider').flexslider({
        directionNav: true,
        pauseOnAction: false
    });
});
</script>
```
参数解释
```javascript
$('.flexslider').flexslider({
 
        namespace: 'flex-',    //控件的命名空间，会影响样式前缀 
        animation: "slide", //String: Select your animation type, "fade" or "slide"图片变换方式：淡入淡出或者滑动
        slideDirection: "horizontal", //String: Select the sliding direction, "horizontal" or "vertical"图片设置为滑动式时的滑动方向：左右或者上下
         
        selector: '.thumbnails .thumbnail',
        slideshowSpeed: 5000, // 自动播放速度毫秒
        animationSpeed: 600, //滚动效果播放时长
        pausePlay: false,//是否显示播放暂停按钮
        minItems: common.globals.SCREEN.ITEM,//最少显示多少项
        itemWidth: 220,//一个滚动项目的宽度
        itemMargin: 20,//滚动项目之间的间距
        slideshow: true, //Boolean: Animate slider automatically 载入页面时，是否自动播放
        animationDuration: 600, //Integer: S动画淡入淡出效果延时
        directionNav: true, //Boolean:  (true/false)是否显示左右控制按钮
        controlNav: true, //Boolean:  usage是否显示控制菜单//什么是控制菜单？
        keyboardNav: true, //Boolean:left/right keys键盘左右方向键控制图片滑动
        mousewheel: false, //Boolean: mousewheel鼠标滚轮控制制图片滑动
        prevText: "Previous", //String: 上一项的文字
        nextText: "Next", //String: 下一项的文字
        pauseText: 'Pause', //String: 暂停文字
        playText: 'Play', //String: 播放文字
        randomize: false, //Boolean: Randomize slide order 是否随机幻灯片
        slideToStart: 0, //Integer:  (0 = first slide)初始化第一次显示图片位置
        animationLoop: true, //  "disable" classes at either end 是否循环滚动 循环播放
        pauseOnAction: true, //Boolean:  highly recommended.
        pauseOnHover: false, //Boolean: ng
        controlsContainer: "", //Selector:  be taken.
        manualControls: ".js-slidernav i", //Selector: .自定义控制导航// 小圆点活数字标示 css 选择器        
        manualControlEvent: "", //String:自定义导航控制触发事件:默认是click,可以设定hover
        start: function() {}, //Callback: function(slider) - 当第一张幻灯片加载时引发的回调
        before: function() {}, //Callback: function(slider) - 每张幻灯片切换动画之前的回调
        after: function() {}, //Callback: function(slider) -  每张幻灯片切换动画完成后的回调
        end: function() {} //Callback: function(slider) -  到达最后一张幻灯片引发的回调
         
    });
```