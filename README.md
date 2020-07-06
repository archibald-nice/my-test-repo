# my-test-repo
# 日常记录用测试型仓库
  [My blog](http://blog.csdn.net/archiewade "点击跳转")<br><br>
# Model-menu-slider
## html
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="x-ua-compatible" content="id=edge">
    <!--  link或script中的 integrity 属性：为了防止 CDN 篡改 javascript 用的  -->
    <!-- cloudflare是部署在国外的一个免费CDN服务平台 -->
<!--    <link-->
<!--            rel="stylesheet"-->
<!--            href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.11.2/css/all.min.css"-->
<!--            integrity="sha256-+N4/V/SbAFiW1MPBCXnfnP9QSN3+Keu+NlB+0ev/YKQ="-->
<!--            crossorigin="anonymous"-->
<!--    />-->
    <link rel="stylesheet" href="menu.css">
    <title>登录界面</title>
</head>
<body>
<!-- 导航栏 -->
<nav id="navbar">
    <div class="logo">
<!--        <img src="https://randomuser.me/api/portraits/men/76.jpg" alt="user">-->
        <img src="huawei_logo.png" alt="user">
    </div>
    <ul>
        <li><a href="#" name="Home">主页</a></li>
        <li><a href="#" name="Portfolio">作品集</a></li>
        <li><a href="#" name="Blog">博客</a></li>
        <li><a href="#" name="Contaction">联系我</a></li>
    </ul>
</nav>
<!-- 内容头部 -->
<header>
    <button id="toggle" class="toggle">
        <i class="fa fa-bar fa-2x"></i>
    </button>
    <h1>登录界面</h1>
    <p>学而不思则罔，思而不学则殆</p>

    <button class="cta-btn" id="open">登录</button>
</header>

<div class="container">
    <h2>本页面简介</h2>
    <p>
        aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa
        aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa
        aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa
        aaaaaaaaaaaaaaaaaa
        aaaaaaaaaaaaaaa
        aaaaaaaaaaaaaaaaaaaaaaaa
        aaaaaaaaaaaaaaaaaaaaaaaaaaaaaa
        aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa
        aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa.
    </p>
    <p>
        bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb
        bbbbbbbbb
        bbbbbbbbbbbbbbbbbbbbbbb
        bbbbbbbbbb
        bbbbbbbbbbbbbbbbbbbbbbbbbbb
        bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb
        bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb
        bbbbbbbbbbbbbbbbbbb
        bbbbbbbbbbbbbbbb
        bbbbbbbbbbbbb
        bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb
        bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb
        bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb
        bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb
        bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb
        bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb.
    </p>

    <h2>和我交流</h2>
    <p>ccccccccccccccccccccccccccccccc
    ccccccccccccccccccccccccccccccccccccc
    cccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccc
    cccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccc
    </p>

    <h2>Benefits</h2>
    <ul>
        <li>Lifetime Access</li>
        <li>30 Day Money Back</li>
        <li>Tailored Customer Support</li>
    </ul>

    <p></p>
</div>

<!-- Model -->
<div class="model-container" id="model">
    <div class="model">
        <button class="close-btn" id="close">
            <i class="fa fa-times"></i>
        </button>
        <div class="model-header">
            <h3>登入</h3>
        </div>
        <div class="model-content">
            <p>通过注册可以获得更多帮助和信息
            <form class="model-form">
                <div>
                    <label for="name">Name</label>
                    <input type="text" id="name" class="form-input" placeholder="请输入...">
                </div>
                <div>
                    <label for="email">Email</label>
                    <input type="email" id="email" class="form-input" placeholder="请输入...">
                </div>
                <div>
                    <label for="pwd">Password</label>
                    <input type="password" id="pwd" class="form-input" placeholder="请输入...">
                </div>
                <div>
                    <label for="pwd2">Password2</label>
                    <input type="password" id="pwd2" class="form-input" placeholder="请输入...">
                </div>
                <input type="submit" value="Submit" class="submit-btn">
            </form>
            </p>
        </div>
    </div>
</div>
<script src="menu.js"></script>
</body>
</html>
```

## css
``` (css)
@import url('https://fonts.googleapis.com/css?family=Lato&display=swap');

:root {
    --model-duration: 1s;
    --primary-color: #30336b;
    --secondary-color: #be2edd;
}

* {
    box-sizing: border-box;
}

body {
    font-family: 'Lato', sans-serif;
    margin: 0;
    transition: transform 0.3s ease;
}

body.show-nav {
    transform: translateX(200px);
}

nav {
    background-color: var( --primary-color);
    border-right: 2px solid rgba(200, 200, 200, 0.1);
    color: #f0f0f0;
    position: fixed;
    top: 0;
    left: 0;
    width: 200px;
    height: 100%;
    z-index: 100;
    transform: translateX(-100%);
}

nav .logo {
    padding: 30px 0;
    text-align: center;
}

nav .logo img {
    height: 75px;
    width: 75px;
    border-radius: 50%;
}

nav ul {
    padding: 0;
    list-style-type: none;
    margin: 0;
}

nav ul li {
    border-bottom: 2px solid rgba(200, 200, 200, 0.1);
    padding: 20px;
}

nav ul li:first-of-type {
    border-top: 2px solid rgba(200, 200, 200, 0.1);
}

nav ul li a {
    color: #fff;
    text-decoration: none;
}

nav ul li a:hover {
    text-decoration: underline;
}

header {
    background-color: var(--primary-color);
    color: #fff;
    font-size: 130%;
    position: relative;
    padding: 40px 15px;
    text-align: center;
}

header h1 {
    margin: 0;
}

header p {
    margin: 30px 0;
}

button,
input[type='submit'] {
    background-color: var(--secondary-color);
    border: 0;
    border-radius: 5px;
    color: #fff;
    cursor: pointer;
    padding: 8px 12px;
}

button:focus {
    outline: none;
}

.toggle {
    background-color: rgba(0, 0, 0, 0.3);
    position: absolute;
    top: 20px;
    left: 20px;
}

.cta-btn {
    padding: 12px 30px;
    font-size: 20px;
}

.container {
    padding: 15px;
    margin: 0 auto;
    max-width: 100%;
    width: 800px;
}

.model-container {
    background-color: rgba(0, 0, 0, 0.6);
    display: none;
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
}

.model-container.show-model {
    display: block;
}

.model {
    background-color: #fff;
    border-radius: 5px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.3);
    position: absolute;
    overflow: hidden;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    max-width: 100%;
    width: 400px;
    animation-name: modelopen;
    animation-duration: var(--model-duration);
}

.model-header {
    background: var(--primary-color);
    color: #fff;
    padding: 15px;
}

.model-header h3 {
    margin: 0;
    border-bottom: 1px solid #333;
}

.model-content {
    padding: 20px;
}

.model-form div {
    margin: 15px 0;
}

.model-form label {
    display: block;
    margin-bottom: 5px;
}

.model-form .form-input {
    padding: 8px;
    width: 100%;
}

.close-btn {
    background: transparent;
    font-size: 25px;
    position: absolute;
    top: 0;
    right: 0;
}

@keyframes modelopen {
    from {
        opacity: 0;
    }

    to {
        opacity: 1;
    }
}
```

## js
```
const toggle = document.getElementById('toggle');
const close = document.getElementById('close');
const open = document.getElementById('open');
const model = document.getElementById('model');
const navbar = document.getElementById('navbar');

function closeNavbar(e) {
    if (document.body.classList.contains('show-nav') &&
        e.target !== toggle && !toggle.contains(e.target) &&
        e.target !== navbar && !navbar.contains(e.target)) {
        document.body.classList.toggle('show-nav');
        document.body.removeEventListener('click', closeNavbar);
    } else if (!document.body.classList.contains('show-nav')) {
        document.body.removeEventListener('click', closeNavbar);
    }
}

// 切换导航栏
toggle.addEventListener('click', () => {
    document.body.classList.toggle('show-nav');
    document.body.addEventListener('click', closeNavbar);
});

// 展示登录模型块
open.addEventListener('click', () => model.classList.add('show-model'));

// 隐藏登录模型块
close.addEventListener('click', () => model.classList.remove('show-model'));

// 通过块外点击实现隐藏登录模型块
window.addEventListener('click', e =>
    e.target == model ? model.classList.remove('show-model') : false
)
;
```

