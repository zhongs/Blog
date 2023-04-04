# 闭包

* 思考：

```
var name = "The Window";
var object = {
　  name : "My Object",
　　getNameFunc : function(){
　　　　 return function(){
　　　　　　 return this.name;
　　　　 };
　　}
};
alert(object.getNameFunc()());
```

```
var name = "The Window";
var object = {
　  name : "My Object",
　　getNameFunc : function(){
        var that = this;      
　　　　 return function(){
　　　　　　 return that.name;
　　　　 };
　　}
};
alert(object.getNameFunc()());
```
