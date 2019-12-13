# php_docker

This set up allows you to serve your php project on docker.

stop anything on you local dev using port 80
install mongdb compass from: https://www.mongodb.com/download-center/compass

copy .env.sample to .env
copy init-mongo.js.sample to init-mongo.js under mongo folder

under .docker folder run:

  docker-compose up                                 # fresh build 

  docker-compose up --build                         # rebuild containers, use when changes have been made on containers config

  docker-compose down                               # Politely request containers to stop, sends a kill signal after 10 seconds if the container refuses to stop.

  docker system prune -a && docker volume prune     # Remove all images and volumes from system

once all containers are running you can access mongodb at: 0.0.0.0"27017 with the username and password that you set on the db configuration
