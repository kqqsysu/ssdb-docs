# hget name key

Get the value related to the specified key of a hashmap

## 参数

* `name` - The name of the hashmap
* `key` - The key of the key-value pair in the hashmap

## 返回值

Value reply.

Return the value to the key, if the key does not exists, return `not_found` Status Code.

## 示例

	ssdb 127.0.0.1:8888> hset h k v
	ok
	(0.000 sec)
	ssdb 127.0.0.1:8888> hget h k
	v
	(0.000 sec)
	ssdb 127.0.0.1:8888> hdel h k
	1
	(0.000 sec)
	ssdb 127.0.0.1:8888> hget h k
	not_found
	(0.000 sec)
	ssdb 127.0.0.1:8888> 
