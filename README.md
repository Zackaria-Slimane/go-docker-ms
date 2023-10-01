# Go API with docker

Simple example of a go docker microservice

# start docker

docker compose up --build
If anything goes wrong try : docker compose down; docker compose up --build

# test with curl commands

curl -X GET localhost:8080/comments | jq
curl -X POST localhost:8080/comments -d "@request.json" | jq
curl -X PUT localhost:8080/comments/1 -d "@request.json" | jq
curl -X DELETE localhost:8080/comments/2 -d "@request.json" | jq
