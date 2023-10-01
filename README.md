# Go API with docker

Simple example of a go docker microservice

# start docker

docker compose up --build
If anything goes wrong try : docker compose down; docker compose up --build

# Test with .json file and curl commands

Create a .json file in the root of the project and use the fields : "user_id" - "comment"
to send tests with curl commands :

curl -X GET localhost:8080/comments | jq
curl -X POST localhost:8080/comments -d "@file.json" | jq
curl -X PUT localhost:8080/comments/1 -d "@file.json" | jq
curl -X DELETE localhost:8080/comments/2 -d "@file.json" | jq
