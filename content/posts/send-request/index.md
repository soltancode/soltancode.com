---
title: "PHP Send Request Package for Laravel Framework"
tags: ["php", "curl", "json", "rest", "api", "Guzzle", "requests", "laravel", "httpclient", "http-client", "soltancode"]
date: 2022-09-30T16:00:00+04:00
description: "Simple package for Laravel Framework that makes it easy to send HTTP requests and integrate with web APIs."
draft: false
images: ["https://soltancode.com/posts/send-request/images/soltancode_send_request.png"]
---

Simple package for Laravel Framework that makes it easy to send HTTP requests and integrate with web APIs. Here is the <a href="https://github.com/soltancode/SendRequest" target="_blank">GitHub link</a>.

## Installation

```
composer require soltancode/send-request
```

## Usage

#### If you use it as class (facade), import this:
```php
use Soltancode\SendRequest\Facades\SendRequest;
```

#### GET Request:
```php
// $baseUrl = "https://dummyjson.com";
// $service = "/products/1";

# Using as class:
SendRequest::get($baseUrl, $service);

# Using as helper:
sendRequest()->get($baseUrl, $service)
```

#### GET Request with params:
```php
// $baseUrl = "https://dummyjson.com";
// $service = "/products/1";
// $params  = [
//     'q' => 'phone'
// ];

# Using as class:
SendRequest::get($baseUrl, $service, $params); # https://dummyjson.com/products/search?q=phone

# Using as helper:
sendRequest()->get($baseUrl, $service, $params); # https://dummyjson.com/products/search?q=phone
```

#### POST Request with params:
```php
// $baseUrl = "https://api.example.com";
// $service = "/login";

# Using as class:
SendRequest::post($baseUrl, $service, [
    'username' => 'myusername',
    'password' => 'mypassword'
]);

# Using as helper:
sendRequest()->post($baseUrl, $service, [
    'username' => 'myusername',
    'password' => 'mypassword'
]);
```

#### PUT Request with params:
```php
// $baseUrl = "https://api.example.com";
// $service = "/users/1";

# Using as class:
SendRequest::put($baseUrl, $service, [
    'first_name' => 'John',
    'last_name' => 'Doe'
]);

# Using as helper:
sendRequest()->put($baseUrl, $service, [
    'first_name' => 'John',
    'last_name' => 'Doe'
]);
```

#### PATCH Request with params:
```php
// $baseUrl = "https://api.example.com";
// $service = "/users/1";

# Using as class:
SendRequest::patch($baseUrl, $service, [
    'first_name' => 'John'
]);

# Using as helper:
sendRequest()->patch($baseUrl, $service, [
    'first_name' => 'John'
]);
```

#### DELETE Request with params:
```php
// $baseUrl = "https://api.example.com";
// $service = "/users";

# Using as class:
SendRequest::delete($baseUrl, $service, [
    'id' => 'John'
]);

# Using as helper:
sendRequest()->delete($baseUrl, $service, [
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