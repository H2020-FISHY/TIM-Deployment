# TIM-Deployment

Contains the yml definition for starting up the Central Repository on a k8s cluster (FRF). Other deployments will go in this repository as they become available.

## Central Repository

### API

Central Repository is available in the FRF Sandbox on the management interface at 192.168.5.2, port 10010. 

### Pub/Sub, RabbitMQ

RabbitMQ is deployed as a k8s service and is not attached to a management interface. Components can connect to it by using the environment variables
"CENTRAL_REPOSITORY_RMQ_SERVICE_HOST" for the address and "CENTRAL_REPOSITORY_RMQ_SERVICE_PORT" for the port. The default "guest/guest" user is active.
