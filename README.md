# dockerplay
Some core docker examples

# How to build this example
```
docker build -t dockerplay .
```

# How to run this example 
docker run -p 4000:80 dockerplay

# How to test test the example works as expected
```
curl http://localhost:4000
```

# Swarm scale and load balancing tests
```
docker swarm init
```

# [Re]deploy with varying loading balancing configurations
```
docker stack deploy -c docker-compose.yml  dockerswarmtest
```

# Test load balancing with
```
curl http://localhost
```
Note different host id with each successive curl call

# See instances running
```
docker stack ps dockerswarmtest
```

# Stop stop
```
docker stack rm dockerswarmtest
```

# View the one-node swarm (our stack)
```
docker node ls
```

# Remove the swarm
```
docker swarm leave --force
```
