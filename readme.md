docker rm $(docker ps -aq)
docker image rm example_console
docker image ls

docker-compose build
docker image ls

docker create --name app-01 -e NAME=Bob example_console
docker create --name app-02 -e NAME=Jack example_console

docker start app-01
docker start app-02

docker logs app-01
docker logs app-02
