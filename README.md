# Config Repo

Repositório de **configurações centralizadas** utilizado pelo [Config Service](../config-service).

---

## Estrutura

- **application.yml** → configurações globais
- **application-dev.yml** → configurações globais para ambiente dev
- **gateway-service.yml** → configs do Gateway
- **discovery-service.yml** → configs do Eureka Discovery

---

## Como acessar as configurações

- Configuração global:
- http://localhost:8888/application/default
- http://localhost:8888/application/dev

- Gateway Service:
- http://localhost:8888/gateway-service/default
- http://localhost:8888/gateway-service/dev

- Discovery Service:
- http://localhost:8888/discovery-service/default
- http://localhost:8888/discovery-service/dev

---

Esse `config-repo` já cobre:
- configs globais
- configs específicas de cada serviço
- suporte a perfis (`default` e `dev`)
- exemplo de rotas no gateway


