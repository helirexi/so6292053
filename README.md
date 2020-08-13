This repository refers to https://stackoverflow.com/questions/62920539/how-do-i-get-php-fpm-to-work-with-nginx-proxy-with-fastcgi .

Subject to be deleted at any time!

License: https://creativecommons.org/licenses/by-sa/4.0/

---




1. When you start it using `docker-compose up -d`, http://test.localhost:8011 will only show you status code 200 with a blank page.
2. Copy `./docker/nginx/conf.d/working-default.conf.dist` to `./docker/nginx/conf.d/default.conf`
3. reload nginx: `docker container exec -it so6292053_proxy_1 /etc/init.d/nginx reload`

You will now see a `phpinfo();` page at http://test.localhost:8011