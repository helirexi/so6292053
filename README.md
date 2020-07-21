1. When you start it using `docker-compose up -d`, http://test.localhost:8011 will only show you status code 200 with a blank page.
2. Copy `./docker/nginx/conf.d/working-default.conf.dist` to `./docker/nginx/conf.d/default.conf`
3. reload nginx: `docker container exec -it so6292053_proxy_1 /etc/init.d/nginx reload`

You will now see a `phpinfo();` page at http://test.localhost:8011