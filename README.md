# APP 2 DOCKER APP CONNECTED TO A POSTGRES DATABASE

docker build -f Dockerfile.dev -t continuous-integration-front .

docker run -it -p 4002:3000 continuous-integration-front

docker build -f Dockerfile.dev -t continuous-integration-back .

docker run -it -p 4003:5000 continuous-integration-back

# to execute all (FRONT + BACK) EN UN COMANDO
docker-compose up --build