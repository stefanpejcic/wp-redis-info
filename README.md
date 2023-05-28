# wp-redis-info
Test Redis ObjectCache and view usage via WP-CLI


### wp redis-info connect
Tests connection to REDIS server, by default uses 127.0.0.1:6379 and you can optionally specify the Redis server and port in the format <hostname>:<port>.

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
  
### wp redis-info connect
Tests connection to REDIS server, by default uses 127.0.0.1:6379 and you can optionally specify the Redis server and port in the format <hostname>:<port>.

EXAMPLES:
```
wp redis-info connect
wp redis-info connect 127.0.0.1:6019
wp redis-info connect localhost
wp redis-info connect :6200
``` 
  
