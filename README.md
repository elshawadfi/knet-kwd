# knet-payment


`
## Installation
```composer
composer require elshawadfi/knetkwd
```


## usage
```php
use Elshawadfi\Knetkwd;


$config = [
    "response_url" => "https://domain.com/result.php",
    "error_url" => "https://domain.com/error.php",
    "tranportal_id"=>"",
    "password"=>"",
    "resource_key"=>"",
    "amount"=> 100,
    "udf1"=> "",
    "udf2"=> "",
    "udf3"=> "",
    "udf4"=> "",
    "udf5"=> "",
    "testmode"=>true   // for test 
];

$knet  = new Knet($config);

// **************  request from knet *************//
$request = $knet->request();

if($request["status"] == 1)
{
    //  $request["data"]["url"];
}
else
{
    // print_r($request["errors"]);
}



```



## response page
```php

$config = [
    "response_url" => "https://domain.com/result.php",
    "error_url" => "https://domain.com/error.php",
    "tranportal_id"=>"",
    "password"=>"",
    "resource_key"=>"",
    "amount"=> 100,
    "udf1"=> "",
    "udf2"=> "",
    "udf3"=> "",
    "udf4"=> "",
    "udf5"=> "",
];

$knet  = new Knet($config);


$resutl = $knet->responce();

if($resutl["status"] == "success"){

  //you success code
}
else
{
    // error
}
```