# Bug description

When unserializing an autoloaded namespaced-class instance, PHP seems to look for the class in a case-sensitive way (whereas it uses case-insensitive lookup when instanciating from the code).

# Run the code

```
php -f test.php
```

The script should output :
```
object(__PHP_Incomplete_Class)#3 (1) {
  ["__PHP_Incomplete_Class_Name"]=>
  string(8) "Test\FoO"
}
```
