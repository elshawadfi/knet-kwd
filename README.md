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
    "tranportal_id"=>"",
    "password"=>"",
    "resource_key"=>"",
    "response_url" => "https://domain.com/result.php",
    "error_url" => "https://domain.com/error.php",
    "amount"=> 100,
    "udf1"=> "",
    "udf2"=> "",
    "udf3"=> "",
    "udf4"=> "",
    "udf5"=> "",
    "is_test"=>true   // for test 
];

$knet  = new Knet($config);

// **************  request from knet *************//
$request = $knet->request();

if($request["status"] == 1)
{
    // redirect to knet payment page using $request["data"]["url"];
}
else
{
    // display errors print_r($request["errors"]);
}



```



## response page
```php

$config = [
    "tranportal_id"=>"",
    "password"=>"",
    "resource_key"=>"",
    "response_url" => "https://domain.com/result.php",
    "error_url" => "https://domain.com/error.php",
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

    // get reult and update your database
}
else
{
    // print error $resutl["ErrorText"]
}
```