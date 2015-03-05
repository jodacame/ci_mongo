# ci_mongo
## Installation
This is a basic library for CI and MongoDB

-Copy folders into CI Application folder

Usage
-------------------
Set your credentials (Host, username, password and database) in the application/config/mongo.php file

Load library "mongo" you can load this using autoload.php 

or 

$this->load->library("mongo");

And now you can use this in your models files with this structure

```
$this->mongo->**DATABASE_NAME**->**COLLECTION_NAME**->**ACTION**;
```


**Example**

```
$response = $this->mongo->sales->customers->find(array("username" => "jhon.doe"));
```

**Get Results**

```
foreach($response as $data)
{
  print_r($data);
}
```

**Count Results**

```
echo $response->count();
```

For more information about mongodb methods  with php go to

http://php.net/manual/es/class.mongodb.php
