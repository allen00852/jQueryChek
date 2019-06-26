# jQuery-chek

## 1.简介

&emsp;功能&nbsp;: 实现单选/反选————实现获取 checkbox value 值

## 2.使用方法

### 2.1.引入 jQuery.js 以及 jQuery.chek.js

```JavaScript
// jQuery.js
<script src="https://code.jquery.com/jquery-3.4.1.min.js" integrity="sha256-CSXorXvZcTkaix6Yvo6HppcZGetbYMGWSFlBw8HfCJo=" crossorigin="anonymous"></script>
// jQuery.chek.js
<script src="jQuery.chek.js"></script>
```

### 2.2.使用

```JavaScript
<script>
     $('#table').chek({
         AllDele: ".allDelete", // 按钮
         url: './datas.php' // 发送请求的路径
     });
</script>
```

## 3.演示代码

### html

```html
<table>
  <thead>
    <tr>
      <th>
        <!-- 单选反选 开关 -->
        <input type="checkbox" name="" />
      </th>
    </tr>
  </thead>
  <tbody>
    <!-- 这下面的checkbox 一定要给个value值 -->
    <tr>
      <td>
        <input type="checkbox" name="" id="" value="1" />
      </td>
    </tr>
    <tr>
      <td>
        <input type="checkbox" name="" id="" value="2" />
      </td>
    </tr>
    <tr>
      <td>
        <input type="checkbox" name="" id="" value="3" />
      </td>
    </tr>
  </tbody>
</table>
<input type="submit" value="按钮" class="allDelete" />
```

### JavaScript

```JavaScript
<script src="https://code.jquery.com/jquery-3.4.1.min.js" integrity="sha256-CSXorXvZcTkaix6Yvo6HppcZGetbYMGWSFlBw8HfCJo=" crossorigin="anonymous"></script>
<script src="jQuery.chek.js"></script>
<script>
    $('#table').chek({
        AllDele: ".allDelete", // 按钮
        url: './datas.php' // 发送请求的路径
    });
</script>
```

### 后台代码 php 演示

```php
<?php
header('Content-Type:text/json;charset=utf-8');
$arrays = $_POST['data'];
$arrays = json_decode($arrays);
// echo count($arrays);
if (count($arrays) >= 1) {
    echo json_encode($arrays);
} else {
    echo '0';
}
```

#注意: 需要在服务器环境下 控制台才会打印出需要的数据
