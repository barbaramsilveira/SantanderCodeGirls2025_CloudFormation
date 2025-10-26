# AWS CloudFormation

A **AWS CloudFormation** é uma ferramenta que permite criar, provisionar e gerenciar recursos na nuvem de forma automatizada, utilizando o conceito de *Infrastructure as Code* (IaC).  
Com ela, é possível descrever toda a infraestrutura de uma aplicação em arquivos `.yaml` ou `.json`, garantindo consistência e agilidade na criação de ambientes na AWS.

Entre as principais vantagens desse modelo de implementação estão:

- Economia de tempo, evitando configurações manuais
- Automação de processos por meio de templates versionáveis
- Rastreabilidade das mudanças realizadas

---

## Exemplo de Template — Instância EC2

Abaixo, um exemplo simples de template YAML para criar uma instância EC2:

```yaml
AWSTemplateFormatVersion: '2010-09-09'
Description: Exemplo simples de criação de uma instância EC2

Resources:
  MinhaInstanciaEC2:
    Type: AWS::EC2::Instance
    Properties:
      InstanceType: t2.micro
      ImageId: ami-0c55b159cbfafe1f0  # Exemplo - AMI da Amazon Linux 2
      KeyName: minha-chave-ec2


