docker build -t ionicbuild -f ionic-docker --build-arg store_pass="" --build-arg key_pass="" --build-arg alias="" .

docker run --name ionic -d --rm -v $PWD/build:/opt/build ionicbuild
docker logs -f ionic