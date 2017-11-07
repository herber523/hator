# hator

`hator` doesn't hate.  
`hator` distributes your HTTP requests into tor network via `HAProxy`.  

***

### Initialization

Create a swarm manager:

    docker swarm init

Or join to other docker swarm as a node:

    docker swarm join --token <token> <ip:port>

### Create a docker stack

    docker stack deploy --compose-file=docker-compose.yml hator

### Monitor

`hator_lb` and `hator_tor` should be listed in:

    docker service ls 

To see `hator` tasks:

    docker service ps hator

To see the statistics report for HAProxy, open your browser and visit:  

[http://localhost:19360](http://localhost:19360)

Default username: `stats`  
Default password: `stats`  

### Scale up:

    docker service scale hator_tor=<num_you_want>


### Test IP

    curl --socks5 localhost:9050 api.ipify.org
