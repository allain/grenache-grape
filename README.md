# Grenache Grape

DHT based high-performance microservices framework, by Bitfinex

### Usage

##### Install

```
// Install global (run binary)
npm install -g grenache-grape
```

```
// Install locally to project (programmatic approach)
npm install --save grenache-grape
```

##### Run Binary

```
// help
grape --help
````

````
// Run 3 Grapes
grape --dp 20001 --ap 30001 --bn '127.0.0.1:20002,127.0.0.1:20003'
grape --dp 20002 --ap 30002 --bn '127.0.0.1:20001,127.0.0.1:20003'
grape --dp 20003 --ap 30003 --bn '127.0.0.1:20001,127.0.0.1:20002'
```

### Technology
* DHT definition: http://www.bittorrent.org/beps/bep_0005.html

#### Definitions

##### 1. Grape: Grenache Discovery Node
* Grenache Network building
* DHT interaction APIs for Clients: service discovery, DHT data storage

API:
* announce Service
* lookup Service
* write to DHT

##### 2. Client: Grenache Client implementation on specific Transports
* Client/Worker: offer/publish and request/subscribe Services
* Patterns: request/reply, publish/subscribe
* Transports: ZeroMQ, WebSocket

API:
* offer/publish Service: create and announce a Service on the DHT
* request/subscribe Service: find a Service throught the DHT and connect to it


#### Features
* Decentralised / Distributed
* High-Performance
* Indefinite growth and shapes

#### Structure Example

![Grenache Structure](https://raw.githubusercontent.com/bitfinexcom/grenache-grape/master/doc/structure.png)

* client: can both offer/publish or request/subscribe Services

### Client Implementations

##### Node.JS
* https://github.com/bitfinexcom/grenache-nodejs-zmq : ZeroMQ based Grape microservices
* https://github.com/bitfinexcom/grenache-nodejs-ws : WebSocket based Grape microservices

##### Ruby
