<p align="center">
    <a href="https://https://github.com/shiguangxiaotou3/wordpress" target="_blank">
        <img src="https://www.shiguangxiaotou.com/favicon.ico" height="100px">
    </a>
    <h1 align="center">Rely是一个composer依赖转换为html的可视化工具 </h1>
    <br>
</p>

### 它是通过分析composer.json文件实现的
![composer依赖可视化](https://www.shiguangxiaotou.com/wp-content/uploads/2022/12/截屏2022-12-03-23.04.03.png)

~~~shell
composer require shiguangxiaotou3/rely
~~~
~~~php
// 使用
require  './vendor/autoload.php';
use ShiGuangXiaoTou3\Rely\Rely;
$model = new Rely;
$model-> vendorDir = './vendor';
$model->baseComposerJson = './composer.json';
$model->baseComposerLock='./composer.lock';
$model->env = true;
$model->projectName="shiguangxiaotou3/rely";
echo $model->renderHtml();
~~~