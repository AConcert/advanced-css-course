Section2 主要讲了两种动画写法，animation 和 transition。



# animation



animation 和 @keyframe 一起使用，用 @keyframe 指定初态，中间任意时刻形态，终态，就可以渲染：

```css
@keyframes moveInLeft {
  0% {
    opacity: 0;
    transform: translateX(-100px);
  }
  80% {
    transform: translateX(10px);
  }
  100% {
    opacity: 1;
    transform: translateX(0);
  }
}

.heading-primary-sub {
  display: block;
  font-size: 20px;
  font-weight: 700;
  letter-spacing: 17.4px;

  animation: moveInRight 1s ease-out; /* 简写 */

  /* animation-name: moveInRight;
  animation-duration: 1s;
  animation-timing-function: ease-out; 一开始快，后来慢 */
}
```

# transition



只要指定终态，就可以渲染。终态一般用 transform 属性，opacity（不透明度，值为 0 表示透明）属性指定：

```css
.btn:hover {
  transform: translateY(-3px);
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
  /* X 轴偏移量、Y 轴偏移量、模糊半径 blur、颜色 */
}

.btn:hover::after {
  transform: scaleX(1.4) scaleY(1.6);
  opacity: 0;
}

.btn:link,
.btn:visited {
  display: inline-block;
  text-transform: uppercase;
  text-decoration: none;
  padding: 15px 40px;
  border-radius: 100px;
  transition: all 0.2s;
  /* transition 和 animation 一样都是设置动画 */
  position: relative;
}

/* pseudo-elements 伪元素 不同于上面的 伪类 pseudo-class :hover */
.btn::after {
  content: "";
  display: inline-block;
  height: 100%;
  width: 100%;
  border-radius: 100px;
  position: absolute;
  top: 0;
  left: 0;
  z-index: -1;
  transition: all 0.4s;
}
```

# 伪类和伪元素

## 伪类

伪类用于选择处于特定状态的元素，比如鼠标挪到上面的状态，第一个孩子元素等

```css
a:hover {
    color:hotpink;
} 

p:first-child {
    font-size: 120%;
    font-weight: bold;
} 
```



## 伪元素

伪元素像往标记文本中新加入的 HTML 元素一样，新长的，伪元素开头为双冒号`::`

> 现代的浏览器为了保持后向兼容，支持早期的带有单双冒号语法的伪元素。

其中最常用的，::before 和 ::after 是使用 CSS 将内容插入到文档中的方法，它们必须和`content`属性一同使用

```css
.btn::after {
  content: "";
  display: inline-block;
  height: 100%;
  width: 100%;
  border-radius: 100px;
  position: absolute;
  top: 0;
  left: 0;
  z-index: -1;
  transition: all 0.4s;
}

.btn:hover::after {
  transform: scaleX(1.4) scaleY(1.6);
  opacity: 0;
}
```



# 单词



transition：过渡

transform：转换

translate：译，怎么转换...