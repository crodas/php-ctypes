php-ctypes
==========

What is it?
-----------

It is a PHP extension which allows you to load external library (`.dll` or `.so`) and call their functions directly from PHP. It is inspired in Python's (ctypes)[http://docs.python.org/2/library/ctypes.html] and (ffi's)[http://pecl.php.net/package/ffi] (an old php extension).

How does it works?
------------------

You need to load a library,

```php
<?php
use CTypes\Library;
$lib = new Library("something.dll");
```

Then you need to create a wrap function

```php
<?php
$lib->getFunction('isint', $return, (array)$arguments);
```

When you get a function you need to tell how to map the arguments and the return type of the function.
