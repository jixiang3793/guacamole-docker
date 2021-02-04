## steps

1. docker run --rm guacamole/guacamole /opt/guacamole/bin/initdb.sh --mysql > initdb-mysql.sql
2. docker-compose -f mysql.yml up
3. open browser http://localhost:9100, user/password is root/gzx12345678
4. create db, name is guacamole,then import sql script, exec it
5. docker-compose -f mysql.yml down
6. docker-compose -f main.yml up -d
7. open browser http://localhost:9200/guacamole, user/password is guacadmin/guacadmin
8. open browser http://localhost:9300, user/password is admin/admin
### links

- https://hub.docker.com/r/guacamole/guacamole
- http://elatov.github.io/2018/06/install-guacamole-on-docker/
- https://hub.docker.com/_/mariadb
