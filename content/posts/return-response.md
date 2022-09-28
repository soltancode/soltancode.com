---
title: "PHP Return Response Package"
tags: ["api", "json", "laravel", "response", "return"]
date: 2022-09-19T23:33:20+04:00
description: "Simple package for returning standard json responses for Laravel Framework."
draft: false
---

Simple package for returning standard json responses for Laravel Framework. Here is the <a href="https://github.com/soltancode/ReturnResponse" target="_blank">GitHub link</a>.

## Installation

```
composer require soltancode/return-response
```

## Usage

#### Code example:
```php
# If you don't use this as helper, import this.
use Soltancode\ReturnResponse\Facades\ReturnResponse;

// $httpResponse = 200;
// $data         = ['success' => true];
// $message      = "Operation done successfully.";

# Using as facade:
return ReturnResponse::response($httpResponse, $data, $message);

# Using as helper:
return returnResponse()->response($httpResponse, $data, $message);
```

#### Response example:
```json
{
  "status_code": 200,
  "message": "Operation done successfully.",
  "count": 1,
  "data": {
    "success": true
  }
}
```

## Other Packages
[SendRequest](https://github.com/soltancode/SendRequest) - PHP cURL class that makes it easy to send HTTP requests and integrate with web APIs.

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[MIT](https://github.com/soltancode/ReturnResponse/blob/main/LICENSE)