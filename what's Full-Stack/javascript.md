## 浏览器资源监控
- window.performance.getEntriesByType("resource")
- window.performance.getEntriesByType("navigation")
## Event Loop(JS)
- [EventLoop](https://zhuanlan.zhihu.com/p/41543963)
## defineProperty(get和set的双向绑定实现)
```
var $watch=function(myObject,callback){
    initWatch(myObject);
    function initWatch(obj){
        for(var i in obj){
            if(typeof obj!='object'){
                return;
            }
            (function(value,o,attr){
                var v=value;
                var oldValue=value;
                Object.defineProperty(o,attr,{
                    get:function(){
                        return v;
                    },
                    set:function (newValue){
                        oldValue=v;
                        v=newValue;
                        callback(newValue,oldValue)
                    }
                });
            })(obj[i],obj,i);
            initWatch(obj[i]);
        }
    }
};
var a = {
　　count:'1',
　　count2:{
　　　　count2_1:'2_1',
　　　　count2_2:'2_2'
　　}
}
Object.prototype.setValue = function(key,value){//设置新Key数据
    this[key] = value;
    $watch(this,function(newValue,oldValue){
        console.log('旧数据~'+oldValue+'    '+'新数据~'+newValue);
    })
}
$watch(a,function(newValue,oldValue){
    console.log('旧数据'+oldValue+'    '+'新数据'+newValue);
})
```
## ow JS类型检查
- [ow](https://github.com/sindresorhus/ow)
- JavaScript 语言没有类型检查，运行时无法知道函数的参数是否为指定的类型。这个库就用来检查函数参数的类型，如果不符合要求就抛错。
## ES6
- [ES6](http://es6.ruanyifeng.com/)
## React/React-native
- [React](https://reactjs.org/)
- [React-native](https://facebook.github.io/react-native/)
## Vue
- [Vue](https://cn.vuejs.org/)
## Canvas
- [Canvas](https://github.com/supperjet/H5-Animation)
## 鲜为人知的JS
- [what the js is that](https://www.infoq.cn/article/QMteVFAMMeBpDhWE-m01)
## Prettier
- [Prettier](https://www.infoq.cn/article/IzAMXQtkJv3N0rXX_G6a)
## 团队建立
- [团队建立](https://www.infoq.cn/article/2kJpJl8*CPK3UZXHm2By)
## Flutter
- [Flutter]()
- [:)](https://www.infoq.cn/article/FYJEtAI5-fvIoSrqJ9Ok)
## 2019 React
- [React](https://www.infoq.cn/article/AEkiVAiJf25LZmoUe_yc)
## 2019 Node.js
- [Node.js](https://www.infoq.cn/article/mXd3WWq_8fd3xoEH9zjG)
- [Node.js](https://www.infoq.cn/article/dDXK8AHUq_tNxXtfb4rE)
## Nginx
- [Nginx] (https://www.infoq.cn/article/m*8bzJOGGLwDEYEfZBy9)
## 前端模块化
- [module] (https://www.infoq.cn/article/QdLtxgNU63-AuY1VOSm7)
## PWA
- [pwa] (https://www.w3cplus.com/pwa/your-first-pwapp.html)
## Vue 小程序
- [小程序VUE](http://mpvue.com/mpvue/simple/)
## 2018 前端
- [前端](https://www.infoq.cn/article/omWDKQXA3I*0fcPqJFTD)
- [前端](https://time.geekbang.org/column/article/77749?utm_term=zeusV2R4J&utm_source=website&utm_medium=infoq&utm_campaign=154-presell&utm_content=textlink0121)
## 软技能
- [软技能](https://www.infoq.cn/article/zE5KFjB*6Bs2ZBEUDzWX)
## React 实践
- [React](https://www.infoq.cn/article/vXkNh*HVrW7HUeiNdlsk)
- [React](https://scrimba.com/g/glearnreact)
## Facebook 技术栈
- [Facebook](https://opensource.fb.com/)
## Node.js 图像识别
- [images](https://www.chenng.cn/post/Node-command-line-tool-production.html)
## 某前端博客
- [某前端博客](https://www.chenng.cn/)
## stack overflow
- [stack overflow](https://www.infoq.cn/article/zEo3O3bs*buxA6FpHjzE)
## 2019 full-stack
- [full-stack](https://www.infoq.cn/article/CQCF0ETQVZVgE8_7dDrw)
## 代码整洁
- [clean code](https://www.zcfy.cc/article/clean-code-javascript-readme-md-at-master-ryanmcdermott-clean-code-javascript-github-2273.html)
## HTML演示文稿
- [reveal.js](https://github.com/hakimel/reveal.js)
## expo
- [expo](https://docs.expo.io/versions/v32.0.0/)
## 算法必备
- [:)](https://www.infoq.cn/article/ur1QLockeQ*hXobPm0kI)
## WebAssembly
- [:)](https://www.ibm.com/developerworks/cn/web/wa-lo-webassembly-status-and-reality/index.html)
## Ant design
- [Ant design](https://ant.design/index-cn)
## 前端面经
- [前端面经](https://www.infoq.cn/article/1ejJvPjm*V0QUVLIJYW7)