have docker app running

make docker.build

docker image ls

docker run --rm \
-d -p 3000:8080 \
-v "${PWD}/searxng:/etc/searxng" \
-e "BASE_URL=http://localhost:3000/" \
-e "INSTANCE_NAME=my-instance" \
searxng/searxng
