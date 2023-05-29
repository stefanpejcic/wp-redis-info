# wp-redis-info
Test Redis Object Cache and monitor usage via WP-CLI

Available commands:

- [redis-info status](#wp-redis-info-status)
- [redis-info connect](#wp-redis-info-connect)
- [redis-info flush](#wp-redis-info-flush)
- [redis-info keys](#wp-redis-info-keys)
- [redis-info value](#wp-redis-info-value)

----

## wp redis-info status
Tests connection to REDIS server and display version, port and process ID

EXAMPLES:
```
wp redis-info status
wp redis-info status 127.0.0.1:6019
wp redis-info status localhost
wp redis-info status :6200
```
 
EXAMPLE OUTPUT:
 ``` 
               _._
          _.-``__ ''-._
     _.-``    `.  `_.  ''-._           Redis 6.0.5
 .-`` .-```.  ```\/    _.,_ ''-._
(    '      ,       .-`  | `,    )
|`-._`-...-` __...-.``-._|'` _.-'|     Port: 6019
|    `-._   `._    /     _.-'    |     PID: 194881
 `-._    `-._  `-./  _.-'    _.-'
|`-._`-._    `-.__.-'    _.-'_.-'|
|    `-._`-._        _.-'_.-'    |           <https://redis.plugins.club/>
 `-._    `-._`-.__.-'_.-'    _.-'
|`-._`-._    `-.__.-'    _.-'_.-'|
|    `-._`-._        _.-'_.-'    |
 `-._    `-._`-.__.-'_.-'    _.-'
     `-._    `-.__.-'    _.-'
         `-._        _.-'
             `-.__.-'
```
  
----
 
## wp redis-info connect
Tests connection to REDIS server, by default uses 127.0.0.1:6379 and you can optionally specify the Redis server and port in the format ```<hostname>:<port>```.

EXAMPLES:
```
wp redis-info connect
wp redis-info connect 127.0.0.1:6019
wp redis-info connect localhost
wp redis-info connect :6200
```
 
EXAMPLE OUTPUT:
 ``` 
Redis Server Information
------------------------
Process ID: 34693
Uptime: 2 hours, 2 minutes, 31 seconds
Memory Usage: 2.74M / 244.14M
Connected Clients: 2
Total Connections Received: 502
Total Commands Processed: 23744
Expired Keys: 4828
```
  
----

## wp redis-info flush
Flush redis objects.
 
EXAMPLES:
```
wp redis-info flush
wp redis-info flush 127.0.0.1:6019
wp redis-info flush localhost
wp redis-info flush :6200
```
 
EXAMPLE OUTPUT:
 ``` 
Success: Redis cache flushed.
```
  
----
  
## wp redis-info keys
Display Redis keys.

EXAMPLES:
```
wp redis-info keys
wp redis-info keys 127.0.0.1:6379
wp redis-info keys localhost
wp redis-info keys :6379
``` 

EXAMPLE OUTPUT:
 ``` 
Key: 05446term_meta.1127
Type: 1
------------------------
Key: 05446options._transient_timeout_https-pcx3-com-wp-content-uploads-2022-11-image-14-png
Type: 1
------------------------
Key: 05446options._transient_timeout_https-pcx3-com-wp-content-uploads-2022-11-image-13-png
Type: 1
------------------------
Key: 05446post_meta.2676
Type: 1
------------------------
Key: 05446terms.1142
Type: 1
------------------------
Key: 05446options._transient_timeout_https-pcx3-com-wp-content-uploads-2022-10-image-5-png
Type: 1
------------------------
Key: 05446post_meta.7767
Type: 1
------------------------
Key: 05446terms.1136
Type: 1
------------------------
Key: 05446post_meta.7317
Type: 1
------------------------
Key: 05446posts.wp_query:3fa1b42246bbbf4246e05bd9ccff07f2:0.20156600 16852947970.70155200 1685294889
Type: 1
------------------------
Key: 05446post_meta.2695
Type: 1
------------------------
Key: 05446post_tag_relationships.9757
Type: 1
------------------------
Key: 05446post_meta.9290
Type: 1
------------------------
Key: 05446term_meta.1337
Type: 1
------------------------
```

 ----

## wp redis-info value
Display Redis value for a specific key.
 
EXAMPLES:
```
wp redis-info value 05446category_relationships.6376
wp redis-info value 05446category_relationships.6376 127.0.0.1:6379
```
 
EXAMPLE OUTPUT:
 
``` 
a:1:{s:4:"data";O:8:"stdClass":10:{s:7:"term_id";i:1036;s:4:"name";s:5:"check";s:4:"slug";s:5:"check";s:10:"term_group";i:0;s:16:"term_taxonomy_id";i:1036;s:8:"taxonomy";s:8:"post_tag";s:11:"description";s:0:"";s:6:"parent";i:0;s:5:"count";i:3;s:6:"filter";s:3:"raw";}}
```
  
----
 
