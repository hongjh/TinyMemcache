# TinyMemcache
Tiny memcache class


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

