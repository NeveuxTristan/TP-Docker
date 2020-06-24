# TP-Docker


Etape 1 du TP
```
docker volume create srcApache && \
docker create --name myApache -p 8080:80 --mount source=srcApache,target=./src httpd && \
docker cp ./testFiles/htmlTest01.html myApache:srcApache && docker cp ./testFiles/htmlTest02.html myApache:srcApache
docker start myApache
```
