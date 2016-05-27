# TinyMemcache
Tiny memcache class

### Install

If you have Composer, just include Router as a project dependency in your `composer.json`. If you don't just install it by downloading the .ZIP file and extracting it to your project directory.

```
require: {
    "hongjh/tiny-memcache": "dev-master"
}
```

### How to use lock ?

```
$mc = new TinyMemcache($host, $port);

if ($mc->lock($key, $expire)) {
  // lock success
  // TO DO YOUR CODE
  $mc->unlock($key);
} else {
  // lock fail, it has been lock now
  // wait for unlock
  // END
}
```

### Flow
![](https://github.com/hongjh/TinyMemcache/blob/master/images/lock-flow.jpg)

