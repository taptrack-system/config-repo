# Config Repo

Repositório de **configurações centralizadas** utilizado pelo serviço [`config-service`](https://github.com/taptrack-system/infra-domain/tree/main/config-service).

Este repositório segue o padrão do **Spring Cloud Config** para gerenciar configurações externas de microsserviços, permitindo atualização sem necessidade de rebuild ou redeploy.

---

## Estrutura

```
config-repo/
├─ .gitignore
├─ LICENSE # Licença Apache-2.0
├─ README.md
├─ application.yml # Configurações globais
├─ application-dev.yml # Configurações globais para ambiente dev
├─ gateway-service.yml # Configurações do Gateway
├─ gateway-service-dev.yml # Configurações do Gateway em dev
├─ discovery-service.yml # Configurações do Eureka Discovery
└─ discovery-service-dev.yml # Configurações do Discovery em dev
```

---

## Repositório

- **GitHub:** [taptrack-system/config-repo](https://github.com/taptrack-system/config-repo)  
- **HTTPS:** `https://github.com/taptrack-system/config-repo.git`  
- **SSH:** `git@github.com:taptrack-system/config-repo.git`  

---

## Como utilizar

O `config-service` deve ser configurado para buscar este repositório.  
Exemplo em `application.yml` do `config-service`:

```yaml
spring:
  cloud:
    config:
      server:
        git:
          uri: https://github.com/taptrack-system/config-repo
          default-label: main
```

---

## Endpoints de Configuração

Após subir o `config-service` (porta padrão: **8888**):

- Configuração Global:
    - [Application Default](http://localhost:8888/application/default)
    - [Application Dev](http://localhost:8888/application/dev)
- Gateway Service:
    - [Gateway Service Default](http://localhost:8888/gateway-service/default)
    - [Gateway Service Dev](http://localhost:8888/gateway-service/dev)
- Discovery Service:
    - [Discovery Service Default](http://localhost:8888/discovery-service/default)
    - [Discovery Service Dev](http://localhost:8888/discovery-service/dev)

---

## Licença

Este projeto está licenciado sob a [Apache License 2.0](LICENSE)
