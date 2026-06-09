# Horizonte de Risco - Módulo de Cibersegurança

## Descrição

Este repositório contém a implementação do módulo de cibersegurança desenvolvido para o projeto **Horizonte de Risco**, solução criada para monitoramento de eventos naturais utilizando dados fornecidos pela NASA através da API EONET.

A aplicação é composta por uma API desenvolvida em **Java Spring Boot**, integrada a um banco de dados **MySQL** e a um aplicativo mobile desenvolvido em **React Native**.

Os eventos coletados são processados e classificados em níveis de risco (**LOW**, **MEDIUM** e **CRITICAL**), permitindo a visualização de alertas ambientais pela aplicação mobile.

---

# Controle de Segurança Implementado

Para atender aos requisitos da disciplina de Cybersecurity, foi implementado um mecanismo de **monitoramento por logs** utilizando a biblioteca **SLF4J**, integrada ao Spring Boot.

Os logs registram operações importantes da aplicação, permitindo rastreamento e auditoria básica do sistema.

Foram monitoradas as seguintes operações:

- Consulta de eventos da NASA
- Consulta de alertas armazenados
- Execução da sincronização de eventos
- Finalização da sincronização

### Exemplo de registros gerados

```text
INFO Consulta de eventos NASA realizada

INFO Consulta de alertas realizada

INFO Sincronização iniciada

INFO Sincronização concluída. Total: 35
```

---

# Arquivos da Implementação

A implementação foi realizada principalmente no arquivo:

```text
src/main/java/br/com/global/controller/EventController.java
```

Foram adicionados registros utilizando:

```java
log.info(...)
```

para monitorar as principais operações da API.

---

# Evidências

A pasta **evidencias** contém:

- Print do código contendo a implementação dos logs
- Print do console da aplicação demonstrando os logs em execução

### Estrutura

```text
evidencias/
├── codigo_logs.png
└── console_logs.png
```

---

# Como Executar

## Pré-requisitos

- Java 21
- Maven
- MySQL
- Variáveis de ambiente configuradas

## Instalação

```bash
mvn clean install
```

## Execução

```bash
mvn spring-boot:run
```

---

# Endpoints Principais

## Consultar eventos da NASA

```http
GET /api/events
```

## Consultar alertas

```http
GET /api/events/alerts
```

## Executar sincronização

```http
POST /api/events/sync
```

---

# Integração com a Global Solution

O módulo de cibersegurança foi integrado ao projeto Horizonte de Risco com o objetivo de aumentar a confiabilidade da solução por meio do monitoramento das operações realizadas pela API.

Os logs permitem identificar falhas, acompanhar execuções e fornecer informações úteis para manutenção e auditoria do sistema.

---

# Objetivos de Desenvolvimento Sustentável (ODS)

## ODS 9 – Indústria, Inovação e Infraestrutura

Contribui para o desenvolvimento de soluções tecnológicas mais seguras, confiáveis e resilientes.

## ODS 11 – Cidades e Comunidades Sustentáveis

Auxilia na disseminação de informações relacionadas a riscos ambientais, apoiando a conscientização e preparação da população frente a eventos naturais.

---

# Estrutura do Repositório

```text
Horizonte_CyberSecurity/

├── evidencias/
    ├── trechosImplementacao.txt
    └── printSync.png
    └── printConsultaEvent.png
    └── printConsultaAlert.png
├── implementacao/
│   └── EventController.java
├── README.md
└── CyberSecurity_Horizonte.pdf
```
