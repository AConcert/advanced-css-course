# Heading



<img src="img\beautiful-header.png" style="zoom:60%;" />



```html
<div class="text-box">
    <h1 class="heading-primary">
        <span class="heading-primary-main">Outdoors</span>
        <span class="heading-primary-sub">is where life happens</span>
    </h1>
</div>
```



```css
.text-box {
  position: absolute;
  top: 40%;
  left: 50%;
  text-align: center;
  transform: translate(-50%, -50%);
}

.heading-primary {
  color: white;
  text-transform: uppercase;
  margin-bottom: 60px;
}

.heading-primary-main {
  display: block;
  font-size: 60px;
  font-weight: 400;
  letter-spacing: 35px;
}

.heading-primary-sub {
  display: block;
  font-size: 20px;
  font-weight: 700;
  letter-spacing: 17.4px;
}
```

## Heading Button



```html
<div class="text-box">
    <h1 class="heading-primary">
        <span class="heading-primary-main">Outdoors</span>
        <span class="heading-primary-sub">is where life happens</span>
    </h1>
    
    <a href="#" class="btn btn-white">discover our tour</a>
    
</div>
```

```css
.btn:link,
.btn:visited {
  display: inline-block;
  text-transform: uppercase;
  text-decoration: none;
  padding: 15px 40px;
  border-radius: 100px;
  transition: all 0.2s;
  /* transition 和 animation 一样都是设置动画 */
}

.btn:hover {
  transform: translateY(-3px);
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
  /* X 轴偏移量、Y 轴偏移量、模糊半径 blur、颜色 */
}

.btn:active {
  transform: translateY(-1px);
  box-shadow: 0 5px 10px rgba(0, 0, 0, 0.2);
}

.btn-white {
  background-color: #fff;
  color: #777;
}
```

