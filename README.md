This is a sample codes to work with redis and go redis client

Run:

```
docker run -d --rm --name redis-test redis:5.0.14
# TODO replace hash value
HOST = docker inspect 797 | jq .[0].Containers.f8723cdf26efb942c8813ad6e3b7fdc6fe12bcbd4cc5d4372ae74edb337d9594.IPv4Address | sed -e 's/"//g'  | sed -e 's/\/.*//g'
docker run -it --network 797 --rm redis:5.0.14 redis-cli -h $HOST
```