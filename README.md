# Config Repo

Repositório de **configurações centralizadas** utilizado pelo [Config Service](../config-service).

---

## Estrutura

- **application.yml**: configurações globais
- **application-dev.yml**: configurações globais para ambiente dev
- **gateway-service.yml**: configs do Gateway
- **discovery-service.yml**: configs do Eureka Discovery

---

## Como acessar as configurações

- Configuração global:
    - [Application Default](http://localhost:8888/application/default)
    - [Application Dev](http://localhost:8888/application/dev)

- Gateway Service:
    - [Gateway Service Default](http://localhost:8888/gateway-service/default)
    - [Gateway Service Dev](http://localhost:8888/gateway-service/dev)

- Discovery Service:
    - [Discovery Service Default](http://localhost:8888/discovery-service/default)
    - [Discovery Service Dev](http://localhost:8888/discovery-service/dev)

