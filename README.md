# GeoLite2-City
GeoLite2-City 城市定位库

1. 在 `laravel使用` 根据ip获取城市定位
     ```php
    require_once("../public/geoip2.phar");
    use GeoIp2\Database\Reader;
    Route::get('/location', function (Request $request) {
        $reader = new Reader(public_path('GeoLite2-City.mmdb'));
        $record = $reader->city('220.170.34.18');
    });
    ```
