# Nginx-Proxy

Composer solution to use NGINX for routing HTTP Request to other containers that do not have port forwarding.


## Run

```docker compose up```

## Test

```curl localhost``` - should return "selcome to nginx"

```curl localhost/web1``` - should return "selcome to web1"

```curl localhost/web2``` - should return "selcome to web2"

## Modify

### change HTML content

Add or edit HTML files in each container src/html directory

### change container names

If changed services names in compose.yml file, change it accordinly in nginx/src/nginx.conf, in each location under proxy_pass

## Tear down
```docker compose down -v --rmi all```
