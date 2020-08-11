<h1 align="center"> laravel-weather </h1>

<p align="center"> A Weather SDK For Laravel</p>


## 安装

```shell
$ composer require oscarmx/laravel-weather -vvv
```

## 配置

本扩展需要使用高德开放平台，你可以自行注册账号，然后创建应用，获取API Key。申请地址：
https://lbs.amap.com/dev/id/newuser

## 使用
```php
use Oscarmx\LaravelWeather\Weather;

$key = '你的高德开放平台API Key';

$weather = new Weather($key);

##获取实时天气
$response = $weather->getWeather('深圳');

##获取近期天气预报
$response = $weather->getWeather('深圳', 'all');

##第三个参数为返回值类型，可选 json 与 xml，默认 json
$response = $weather->getWeather('深圳', 'all', 'xml');
```
## Tips

目前代码为1.0版本，有问题可以给我提Issues 
https://github.com/oscar-mx/laravel-weather/issues

## License

[LICENSE](https://github.com/oscar-mx/laravel-weather/blob/master/LICENSE)
