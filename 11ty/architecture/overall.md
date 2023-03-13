---
permalink: architecture/overall-architecture.html
layout: page
---
# Arquitetura Geral

![Overall Architecture](/images/overall-architecture.jpg)

## Contextos
A arquitetura foi definida em dois grandes contextos: o core do sistema e o contexto de gerenciamento. São eles:
* **Core do sistema**: consiste nas funções de marcação de pontos, conferência e ajuste de horários
* **Contexto de gerenciamento**: funções de gerenciamento de times, pessoas e empresas
* **Contexto de segurança e autorização**: camada de login e autorização de acessos

## Serviços
* **register-service**: serviço separado apenas para o registro de horários, dada a carga que esse fluxo deve suportar (lambda?)
* **mirror-service**: serviço separado apenas para a conferência de horários, também pela carga mais elevada que esse fluxo deve suportar
* **register-management-service**: reúne as funcionalidades de realização e análise de pedidos de marcação
* **business-service**: responsável por gerenciar funcionários, times e empresas (serviço gigante?)
* **auth-service**: funcionalidades de login e camada de autorização no acesso de cada endpoint
* **log-service**: responsável por registrar os logs de todos os serviços

