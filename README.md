yscroll
=======

##轻量级的区域滚动(暂时只支持手机事件，不依赖其他三方库js库，不只支持局部滚动，还支持H5翻屏动画)


### 调用方式
``` javascript
//第一个参数是选择器，第二个是配置参数
var w1 = new Yscroll('.wrapper', {
	Scontainer : '.container', //内部滚动区域的class
	hScroll : true, //横向滚动
	vScroll : false, //竖向滚动
	momentum : true, //滚动动量（加速度）
	bounce : true, //是否反弹
	snap: false //吸附（可以支持翻屏）
});
//事件绑定
w1.scrollBefore(function(){
	console.log('start'); 
}).scrollEnd(function(){
	console.log('end');
}).orientationchange(function(){
	this.wrapper.style.width = '80%';
	this.reset();
});
```



