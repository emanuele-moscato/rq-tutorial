# Experimenting with RQ

### Dependencies
- [Redis](https://redis.io/): a non relational  database that stores key-value pairs.

- `redis`: Python library exposing an API to connect to a Redis database.

- `rq`: Python library to orchestrate job queues using Redis ("rq" = "Redis queue").

### Installation

#### Redis
To install Redis and run it locally, first download the required files,
```
wget http://download.redis.io/releases/redis-4.0.11.tar.gz
```
and untar the archive. This will create a directory `redis-x.x.xx` (depending on the version of Redis): navigate into it and run `make`.

Done! You are ready to run Redis locally. To do so, navigate to the `src` directory and run
```
redis-server
```

### `redis`
```
pip install -U redis
```

### `rq`
```
pip install -U rq
```

### Starting workers
To start a worker, run
```
rq worker
```
__Note:__ workers must be started in the same directory in which the functions that get called are defined (i.e. where the Python module with their definition is).