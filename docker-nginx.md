#### img

#### step1:how to run ?
```bash
➜  12nginx git:(md) ✗ cat Dockerfile
FROM nginx
COPY html /usr/share/nginx/html
➜  12nginx git:(md) ✗ cat html/index.html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>docker nginx</title>
  </head>
  <body>
    <h2>hello docker nginx</h2>

  </body>
</html>
➜  12nginx git:(md) ✗ docker build -t some-content-nginx .
➜  12nginx git:(md) ✗ docker run --name some-nginx -d -p 8080:80 some-content-nginx
```
#### step2: test
```bash
➜  12nginx git:(md) ✗ curl localhost:8080
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>docker nginx</title>
  </head>
  <body>
    <h2>hello docker nginx</h2>

  </body>
</html>
➜  12nginx git:(md) ✗
```
