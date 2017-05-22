## Welcome to Wtoip - A Frontend Framework base on jQuery ^1.12.0 & compatible with ^IE8
    欢迎来到 Wtoip - 一款基于 `jQuery^1.12.0` 兼容 `IE8` 的前端框架

You can fork on [GitHub](https://github.com/avlcjw/Fuck-framework) to maintain the content of the framework.

您可以在[GitHub](https://github.com/avlcjw/Fuck-framework)上分支框架来维护内容。

### Diagram   [框架图表]
![Diagram](https://raw.githubusercontent.com/avlcjw/wtoip-frontend-framework/master/framework.diagram.png)

link: [Diagram](https://www.draw.io/?lightbox=1&highlight=0000ff&edit=_blank&layers=1&nav=1&title=framework.diagram.xml#Uhttps%3A%2F%2Fraw.githubusercontent.com%2Favlcjw%2Fwtoip-frontend-framework%2Fmaster%2Fframework.diagram.xml)

### startup [启动并返回实例]
  
```
//return an Instance. Used to manipulate datas with the servals APIs;
var wtoip = new Wtoip({
    model: {
      datas: {
        atestData: '这是测试初始化数据',
        username: '用户名',
        password: '123123123123ss',
        items: [
          {
            name: 'name1',
          },
          {
            name: 'name2',
          }
        ]
      }
    },
    view: {
      container: '#container',
      events: {
        init: function (e) {         
          // console.log(this, '程序初始化回调函数!');
        },
        buy: function (e) {
          // console.log(this);
        },
        test: function (e) {
          // console.log(this);
          alert('test');
        }
      }
    }
  });
  
   wtoip.$datas.password = 321;
   //this operation with change the Instance, and the framework will automatic update the view inside the app.
  
```  
  
### Template & Directive  [模版指令]

- Fuck-bind：显示数据
- Fuck-each：循环数据
- Fuck-if：条件显隐
```html
<div class="row">
    <div class="col-sm-12">
      <h4>1.循环指令： fuck-each</h4>
      <ul class="swiper-wrapper">
        <li Fuck-each="items">
          <span Fuck-bind="name"></span>
        </li>
      </ul>
    </div>
    <div class="col-sm-12">
      <h4>2.绑定指令： fuck-bind</h4>
      <p Fuck-bind="atestData3"></p>
    </div>
</div>
```

  
### DataFlow  [数据绑定]

- Fuck-model：绑定数据
```html
<div class="form-group">
        <label for="username">
          双向绑定：username -
          <span fuck-bind="username"></span>
        </label>
        <input type="text" class="form-control" id="username" placeholder="请输入username" fuck-model="username">
</div>
```




### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
