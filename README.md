# Laboratório AWS CloudFormation — Documentação Técnica

Este repositório foi criado como parte de um estudo prático para consolidar conhecimentos sobre **AWS CloudFormation**, simulando os principais passos de criação, configuração e gerenciamento automatizado de infraestrutura na nuvem.

A **AWS CloudFormation** é um serviço que permite criar, provisionar e gerenciar recursos de forma automatizada utilizando *Infrastructure as Code* (IaC). Com ele, é possível descrever toda a infraestrutura em arquivos YAML ou JSON, garantindo padronização, reprodutibilidade e controle de versão.

---

## Tecnologias e Serviços

- **AWS CloudFormation**  
- **AWS Free Tier**  
- **Amazon EC2** (exemplo de recurso provisionado)  
- **Amazon S3** (armazenamento de artefatos)  
- **GitHub** (documentação do projeto)

---

## Objetivos do Laboratório

- Compreender a estrutura de templates YAML e JSON no CloudFormation  
- Provisionar recursos automaticamente por meio de templates versionáveis  
- Criar e gerenciar *stacks* de infraestrutura na AWS  
- Entender o funcionamento de *change sets* e rollback automático  
- Documentar e versionar a infraestrutura de forma reprodutível

---

## Exemplo de Template (YAML)

```yaml
AWSTemplateFormatVersion: '2010-09-09'
Description: Exemplo simples de criação de uma instância EC2

Resources:
  MinhaInstanciaEC2:
    Type: AWS::EC2::Instance
    Properties:
      InstanceType: t2.micro
      ImageId: ami-0c55b159cbfafe1f0
      KeyName: minha-chave-ec2
