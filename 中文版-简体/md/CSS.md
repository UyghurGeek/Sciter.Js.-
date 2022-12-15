# CSS 命名空间

这个命名空间对象包含 CSS 辅助函数。

## Methods:

### `CSS.supports(prop,value):bool`

报告引擎是否支持给定的属性名称和值。

### `CSS.set(string):StyleSet`

Sciter 特定的 StyleSet 构造函数。

此函数允许在运行时构造样式集对象。主要目的是在 Reactor 组件中用于在与组件本身相同的 JS 文件中定义组件样式：

```JavaScript 

const h = 64;

const myStyles = CSS.set`
  :root { // the component itself
     width: 100px;
     height: ${h}px;
  }
  :root > span {
     color:red;
  } 
`;

class MyComponent extends Element {
  render() {
    return <div styleset={myStyles}>
       Hello <span>embedded</span> CSS
    </div>
  } 
}

```
Content of CSS.set literal is normal `@set`  declaration but without `@set name` preambula and without enclosing `{`,`}` brackets.