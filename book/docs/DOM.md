# DOM

文档对象模型是用来呈现以及与任意 HTML 或 XML 文档交互的 API 。执行下面的代码，查找并获取符合条件的指定 DOM 元素。

```html
<!DOCTYPE html>
<html lang="zh-Hans">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JavaScript</title>
</head>
<body>
    <nav id="nav">Hello World!</nav>
    <div class="box">Hello JavaScript!</div>
    <ul>
        <li>1</li>
        <li>2</li>
        <li>3</li>
    </ul>
    <script type="text/javascript">
        const nav = document.querySelector('#nav');
        console.log(nav);
        const box = document.querySelector('.box');
        console.log(box);
        const li = document.querySelector('ul li');
        console.log(li);
        const li1 = document.querySelector('ul li:first-child');
        console.log(li1);
    </script>
</body>
</html>
```

执行下面的代码，查找并获取符合条件的所有 DOM 元素。

```html
<!DOCTYPE html>
<html lang="zh-Hans">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JavaScript</title>
</head>
<body>
    <ul>
        <li>1</li>
        <li>2</li>
        <li>3</li>
    </ul>
    <script type="text/javascript">
        const li = document.querySelectorAll('ul li');
        console.log(li);
    </script>
</body>
</html>
```

执行下面的代码，使用其他方式获取 DOM 元素。

```html
<!DOCTYPE html>
<html lang="zh-Hans">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JavaScript</title>
</head>
<body>
    <nav id="nav">Hello World!</nav>
    <div class="box">Hello JavaScript!</div>
    <div class="box">Hello JavaScript!</div>
    <ul>
        <li>1</li>
        <li>2</li>
        <li>3</li>
    </ul>
    <script type="text/javascript">
        const nav = document.getElementById('nav');
        console.log(nav);
        const box = document.getElementsByClassName('box');
        console.log(box);
        const li = document.getElementsByTagName('li');
        console.log(li);
    </script>
</body>
</html>
```

执行下面的代码，修改指定 DOM 元素中的 HTML 内容。

```html
<!DOCTYPE html>
<html lang="zh-Hans">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JavaScript</title>
</head>
<body>
    <nav id="nav">Hello World!</nav>
    <script type="text/javascript">
        const nav = document.querySelector('#nav');
        console.log(nav);
        nav.innerHTML = '<p>Hello JavaScript!</p>';
    </script>
</body>
</html>
```

执行下面的代码，修改指定 DOM 元素的 CSS 属性。

```html
<!DOCTYPE html>
<html lang="zh-Hans">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JavaScript</title>
</head>
<body>
    <div class="box">Hello World!</div>
    <script type="text/javascript">
        const box = document.querySelector('.box');
        box.style.color = 'red';
    </script>
</body>
</html>
```

执行下面的代码，修改指定 DOM 元素的类名。

```html
<!DOCTYPE html>
<html lang="zh-Hans">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JavaScript</title>
</head>
<body>
    <div class="box">Hello World!</div>
    <script type="text/javascript">
        const box = document.querySelector('.box');
        console.log(box.className);
        box.className = 'nav';
        console.log(box.className);
    </script>
</body>
</html>
```

执行下面的代码，操作指定 DOM 元素的类名。

```html
<!DOCTYPE html>
<html lang="zh-Hans">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JavaScript</title>
    <style type="text/css">
        .nav {
            color: red;
        }
    </style>
</head>
<body>
    <div class="box">Hello World!</div>
    <script type="text/javascript">
        const box = document.querySelector('.box');
        console.log(box.className);
        box.classList.add('nav');
        console.log(box.className);
        box.classList.remove('box');
        console.log(box.className);
        box.classList.toggle('box');
        console.log(box.className);
    </script>
</body>
</html>
```

执行下面的代码，修改指定 DOM 元素的自定义属性。

```html
<!DOCTYPE html>
<html lang="zh-Hans">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JavaScript</title>
</head>
<body>
    <div class="box" data-id="1">Hello World!</div>
    <script type="text/javascript">
        const box = document.querySelector('.box');
        console.log(box.dataset);
        console.log(box.dataset.id);
    </script>
</body>
</html>
```

执行下面的代码，查找指定 DOM 元素的父节点。

```html
<!DOCTYPE html>
<html lang="zh-Hans">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JavaScript</title>
</head>
<body>
    <nav class="nav">
        <div class="box"></div>
    </nav>
    <script type="text/javascript">
        const box = document.querySelector('.box');
        console.log(box.parentNode);
    </script>
</body>
</html>
```

执行下面的代码，查找指定 DOM 元素的所有子节点。

```html
<!DOCTYPE html>
<html lang="zh-Hans">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JavaScript</title>
</head>
<body>
    <ul>
        <li>1</li>
        <li>2</li>
        <li>3</li>
    </ul>
    <script type="text/javascript">
        const ul = document.querySelector('ul');
        console.log(ul.children);
    </script>
</body>
</html>
```

执行下面的代码，查找指定 DOM 元素的兄弟节点。

```html
<!DOCTYPE html>
<html lang="zh-Hans">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JavaScript</title>
</head>
<body>
    <ul>
        <li>1</li>
        <li class="li">2</li>
        <li>3</li>
    </ul>
    <script type="text/javascript">
        const li = document.querySelector('.li');
        console.log(li.previousElementSibling);
        console.log(li.nextElementSibling);
    </script>
</body>
</html>
```

执行下面的代码，创建新的 DOM 节点并插入。

```html
<!DOCTYPE html>
<html lang="zh-Hans">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JavaScript</title>
</head>
<body>
    <ul>
        <li>1</li>
        <li>2</li>
        <li>3</li>
    </ul>
    <script type="text/javascript">
        const div = document.createElement('div');
        document.body.appendChild(div);
        const ul = document.querySelector('ul');
        const p = document.createElement('p');
        ul.insertBefore(p, ul.children[0]);
    </script>
</body>
</html>
```

执行下面的代码，克隆指定节点并插入。

```html
<!DOCTYPE html>
<html lang="zh-Hans">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JavaScript</title>
</head>
<body>
    <div></div>
    <ul>
        <li>1</li>
        <li>2</li>
        <li>3</li>
    </ul>
    <script type="text/javascript">
        const div = document.querySelector('div');
        const ul = document.querySelector('ul');
        const new_ul = ul.cloneNode(true);
        div.appendChild(new_ul);
    </script>
</body>
</html>
```

执行下面的代码，删除指定节点。

```html
<!DOCTYPE html>
<html lang="zh-Hans">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JavaScript</title>
</head>
<body>
    <ul>
        <li>1</li>
        <li>2</li>
        <li>3</li>
    </ul>
    <script type="text/javascript">
        const ul = document.querySelector('ul');
        ul.removeChild(ul.children[0]);
    </script>
</body>
</html>
```

