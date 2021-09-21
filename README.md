# nodejs-micro-services

> **DOC NOT FINISHED YET**

This is a app ([conference-app](conference-app)) sample to microservices with NodeJS.

## Service Registry

Project: [service-registry](service-registry)

To register: `PUT|DELETE /register/:servicename/:serviceversion/:serviceport`

To use service: `GET /find/:servicename/:serviceversion`

Return service data:
```js
{
    "timestamp": 1552334467,
    "ip": "[::1]",
    "port": "3009",
    "name": "service-1",
    "version": "1.2.0",
}
```
or
```js
{
    "result": "Service not found"
}
```

The service [expire](service-registry/server/lib/ServiceRegistry.js#L3).

### Version

![Service Version Control](images/version.png)

### Load Balancing

![Service Version Control](images/load_balancing.png)

## Microservices

Project: [feedback-service](feedback-service)

Project: [speakers-service](speakers-service)

## Tolerance and Resilience



## Queues