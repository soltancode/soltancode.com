---
title: "PHP Send Request Package"
tags: ["php", "curl", "json", "rest", "api", "Guzzle", "requests", "laravel", "httpclient", "http-client", "soltancode"]
date: 2022-09-21T20:53:54+04:00
description: "PHP cURL class that makes it easy to send HTTP requests and integrate with web APIs."
draft: false
---

PHP cURL class that makes it easy to send HTTP requests and integrate with web APIs. Here is the <a href="https://github.com/soltancode/SendRequest" target="_blank">GitHub link</a>.

## Installation

```
composer require soltancode/send-request
```

## Usage

```php
require __DIR__ . '/vendor/autoload.php';

use Soltancode\SendRequest\ConnectApi;

$baseUrl = "https://dummyjson.com";
$service = "/products/1";

$curl = new ConnectApi();
$curl->get($baseUrl, $service);
```

```php
$baseUrl = "https://dummyjson.com";
$service = "/products/1";
$params  = [
    'q' => 'phone'
]

$curl = new ConnectApi();
$curl->get($baseUrl, $service, $params); # https://dummyjson.com/products/search?q=phone
```

```php
$baseUrl = "https://api.example.com";
$service = "/login";

$curl = new ConnectApi();
$curl->post($baseUrl, $service, [
    'username' => 'myusername',
    'password' => 'mypassword'
]);
```

```php
$baseUrl = "https://api.example.com";
$service = "/users/1";

$curl = new ConnectApi();
$curl->put($baseUrl, $service, [
    'first_name' => 'John',
    'last_name' => 'Doe'
]);
```

```php
$baseUrl = "https://api.example.com";
$service = "/users/1";

$curl = new ConnectApi();
$curl->patch($baseUrl, $service, [
    'first_name' => 'John'
]);
```

```php
$baseUrl = "https://api.example.com";
$service = "/users";

$curl = new ConnectApi();
$curl->delete($baseUrl, $service, [
    'id' => 'John'
]);
```

## Other Packages
[ReturnResponse](https://github.com/soltancode/ReturnResponse) - It's a return helper for showing standard json responses.

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[MIT](https://github.com/soltancode/SendRequest/blob/main/LICENSE)