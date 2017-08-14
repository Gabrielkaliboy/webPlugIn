ie7-js
---

### 1.说明
ie7 – js中是一个JavaScript库（解决IE与W3C标准的冲突的JS库），使微软的Internet Explorer的行为像一个Web标准兼容的浏览器，支持更多的W3C标准，支持CSS2、CSS3选择器。它修复了许多的HTML和CSS问题，并使 得透明PNG在IE5、IE6下正确显示。

### 2.项目地址
https://code.google.com/archive/p/ie7-js/


### 3.用法
IE7.js
使IE5、IE6升级至兼容IE7
注释使Internet Explorer版本号低于IE7的IE浏览器载入该代码。
```
<!–[if lt IE 7]>
<script src=”http://ie7-js.googlecode.com/svn/version/2.0(beta3)/IE7.js” type=”text/javascript”></script>
<![endif]–>
```

IE8.js
使IE5、IE6、IE7支持更多的W3C标准（修复了许多的HTML和CSS问题）。
注释使Internet Explorer版本号小于8的IE浏览器载入该代码，而其它符合标准的浏览器则会忽略该代码，并在IE8出来后不干扰其工作。
```
<!–[if lt IE 8]>
<script src=”http://ie7-js.googlecode.com/svn/version/2.0(beta3)/IE8.js” type=”text/javascript”></script>
<![endif]–>
```

IE9.js

使IE5,IE6,IE7,IE8兼容到IE9模式
```
<!--[if lt IE 9]>
<script src=http://up.2cto.com/2013/0222/20130222021951794.png";</script>
<![endif]-->
```