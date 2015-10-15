## RabbitMQ iPython Examples
[Original tutorials](https://www.rabbitmq.com/getstarted.html)

#### Install environment

```sh
virtualenv .mqEnv
. ./.mqEnv/bin/activate
pip install -r requirements.txt --upgrade
```

#### Ramp up RabbitMQ(in docker)
```sh
docker pull rabbitmq:3-management
docker run -d  --hostname local_rabbitmq --name local_rabbitmq -p 15672:15672 -p 15674:15674 -p 5672:5672 rabbitmq:3-management
```

#### How to run
1. Run iPython notebook
```sh
. ./.mqEnv/bin/activate
./.mqEnv/bin/ipython notebook notebooks # it will automatically open browser with notebooks.
 ```
2. Visit RabbitMQ managment site `http://DOCKER_IP:15672/` to check how MQ works.

To get docker ip run `docker-machine ip default`

##### ToDo:
- Remote procedure call (RPC) example. [link](https://www.rabbitmq.com/tutorials/tutorial-six-python.html)

### Links:
- [Docker](https://www.docker.com/whatisdocker)
- [RabbitMQ](https://www.rabbitmq.com/features.html)
- [iPyhton Notebook](http://ipython.org/notebook.html)