# Exercício Extra

Procure pelo histórico de versões dos seguintes itens de Software:

- Apache HTTP Server
- NGINX
- WordPress

Para cada software, obtenha a lista de modificações da penúltima para a última versão.

## Apache HTTP Server - Versões

Apache HTTP Server 1.3, Apache HTTP Server 2.0, Apache HTTP Server 2.1, Apache HTTP Server 2.2, Apache HTTP Server 2.4.

Source: https://archive.apache.org/dist/httpd/

## Lista de Modificações

### Apache HTTP Server 2.2
- Authn/Authz
- Caching
- Proxying
- Filtragem Inteligente (Smart Filtering)

### Apache HTTP Server 2.4
- Run-time Loadable MPMs
- Event MPM
- Asynchronous support
- Per-module and per-directory LogLevel configuration
- Per-request configuration sections
- General-purpose expression parser
- KeepAliveTimeout in milliseconds
- NameVirtualHost directive
- Override Configuration
- Config file variables
- Reduced memory usage


## NGINX - Versões

NGINX 0.1.x, NGINX 0.2.x, NGINX 0.3.x, NGINX 0.4.x, NGINX 0.5.x, NGINX 0.6.x, NGINX 0.7.x, NGINX 0.8.x, NGINX 0.9.x, NGINX 1.0.x,
NGINX 1.1.x, NGINX 1.2.x, NGINX 1.3.x, NGINX 1.4, NGINX 1.5.x, NGINX 1.7.x, NGINX 1.9.x, NGINX 1.11.x.

Source: http://nginx.org/en/CHANGES

## Lista de Modificações

### NGINX 1.11.9
- Bugfix: nginx might hog CPU when using the stream module; the bug had
appeared in 1.11.5.

- Bugfix: EXTERNAL authentication mechanism in mail proxy was accepted
even if it was not enabled in the configuration.

- Bugfix: a segmentation fault might occur in a worker process if the
"ssl_verify_client" directive of the stream module was used.

- Bugfix: the "ssl_verify_client" directive of the stream module might
not work.

- Bugfix: closing keepalive connections due to no free worker
connections might be too aggressive.
Thanks to Joel Cunningham.

- Bugfix: an incorrect response might be returned when using the
"sendfile" directive on FreeBSD and macOS; the bug had appeared in
1.7.8.

- Bugfix: a truncated response might be stored in cache when using the
"aio_write" directive.

- Bugfix: a socket leak might occur when using the "aio_write"
directive.

### NGINX 1.11.10
- Change: cache header format has been changed, previously cached
responses will be invalidated.

- Feature: support of "stale-while-revalidate" and "stale-if-error"
extensions in the "Cache-Control" backend response header line.

- Feature: the "proxy_cache_background_update",
"fastcgi_cache_background_update", "scgi_cache_background_update",
and "uwsgi_cache_background_update" directives.

- Feature: nginx is now able to cache responses with the "Vary" header
line up to 128 characters long (instead of 42 characters in previous
versions).

- Feature: the "build" parameter of the "server_tokens" directive.
Thanks to Tom Thorogood.

- Bugfix: "[crit] SSL_write() failed" messages might appear in logs
when handling requests with the "Expect: 100-continue" request header
line.

- Bugfix: the ngx_http_slice_module did not work in named locations.

- Bugfix: a segmentation fault might occur in a worker process when
using AIO after an "X-Accel-Redirect" redirection.

- Bugfix: reduced memory consumption for long-lived requests using
gzipping.

