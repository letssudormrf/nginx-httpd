# nginx-httpd

Quick Start
-----------

For docker run command.

    docker run -d -p 80:8080/tcp -p 443:8443/udp --name nginx-httpd letssudormrf/nginx-httpd

Keep the Docker container running automatically after starting, add **--restart always**.

    docker run --restart always -d -p 80:8080/tcp -p 443:8443/udp --name nginx-httpd letssudormrf/nginx-httpd

Outbound enable the socks5 proxy

    docker run --restart always -d -p 80:8080/tcp -p 443:8443/udp -e PROXY="ON" -e PROXYIP="127.0.0.1" -e PROXYPORT="1080" --name nginx-httpd letssudormrf/nginx-httpd

