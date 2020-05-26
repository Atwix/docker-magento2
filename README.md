# docker-magento2

Opinionated docker image for Magento 2.2+.

## Base image

 - Alpine 3.8

## Included software

 - nginx
 - PHP 7.3 with FPM
 - Redis
 - MySQL client
 - msmtp, aliased as sendmail

## Extra bits

 - Node.js
 - runit
 - sassc
 - dockerize

## Getting started

```sh-session
# Build image
docker build -t furseyev/magento2 .

# Test image, visit http://magento2.local/
cd /path/to/magento2/project
docker run --init --rm -p 80:80 -v $(pwd):/var/www/magento2 furseyev/magento2
```
