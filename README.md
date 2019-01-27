From https://github.com/riboseinc/digicert-cli

# Usage

1. obtain an api key from digicert: https://www.digicert.com/rest-api
2. if exists, set the IP restriction for your account

```
docker run --rm -e DIGICERT_API_KEY=<api-key> szabogyula/digicert-cli digicert 
```

## list orders

```
docker run --rm -e DIGICERT_API_KEY=<api-key> szabogyula/digicert-cli digicert order list
```

## download certificate

```
docker run --rm -e DIGICERT_API_KEY=<api-key> -v $PWD:/download szabogyula/digicert-cli digicert certificate download -o download --order_id <the-order-id>
```
