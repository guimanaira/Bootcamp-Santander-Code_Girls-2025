# Gerenciando Instâncias EC2 na AWS

## 💡 Desafio

No setor de **financiamento imobiliário**, é comum que empresas precisem processar grandes volumes de dados sobre propostas de crédito, avaliações de imóveis e simulações financeiras. O desafio é **garantir que esses processos rodem de forma automática, escalável e com custos otimizados**, especialmente em horários de pico. Para resolver isso, este projeto propõe um **sistema automatizado de gerenciamento de instâncias EC2** utilizando **Lambda Functions, S3 e EBS**, com foco em **eficiência e controle de custos** na nuvem.


## 🎯 Objetivo Geral

Desenvolver uma **solução serverless** que automatize o ciclo de vida das **instâncias EC2** usadas no processamento de dados de **financiamento imobiliário**, integrando:

- **S3** para armazenar relatórios e logs das operações,
- **EBS** para persistência dos dados das instâncias, e
- **Lambda Function** para iniciar, parar e monitorar automaticamente as instâncias conforme regras de negócio.


## 🧰 Ferramentas Utilizadas

- **AWS EC2** — para executar os processos de simulação e análise de crédito imobiliário.
- **AWS Lambda** — para automatizar o start/stop e monitoramento das instâncias EC2.
- **Amazon S3** — para armazenar relatórios e arquivos gerados pelos sistemas de análise.
- **Amazon EBS (Elastic Block Store)** — para manter dados persistentes das instâncias.
- **AWS CloudWatch** — para monitoramento e gatilhos de automação.
- **IAM (Identity and Access Management)** — para controle de permissões.
- **AWS Console / CLI** — para gerenciamento e configuração dos serviços.
- **Draw.io** — para construção do diagrama.


## ⚙️ Processo de Criação

- **Planejamento do cenário de financiamento imobiliário**
    - Definiu-se que cada instância EC2 representaria um *processador de análises de crédito*.
    - Os resultados (relatórios, simulações e logs) seriam armazenados automaticamente no **S3**.
- **Configuração das instâncias EC2**
    - Criação de uma instância EC2 otimizada para processamento de dados.
    - Associação de um volume **EBS** para persistir informações entre execuções.
- **Criação da função Lambda**
    - Desenvolvimento de uma **Lambda Function** para iniciar e parar automaticamente as instâncias EC2 com base em horários de operação (ex: 8h às 18h).
    - Integração com **CloudWatch Events** para agendar execuções.
- **Integração com S3**
    - A função Lambda salva os **logs de execução e relatórios** no bucket **S3**, garantindo histórico e rastreabilidade.
- **Monitoramento e otimização**
    - Configuração de **CloudWatch Alarms** para alertar sobre consumo elevado de CPU, memória e custos.
    - Ajustes automáticos para desligar instâncias ociosas e reduzir custos operacionais.


## 📈 Resultados Esperados

Um ambiente automatizado e inteligente que:

- Reduz o custo de operação das instâncias EC2;
- Garante persistência e segurança dos dados via EBS;
- Centraliza relatórios e logs no S3;
- Melhora a eficiência no processamento de dados de financiamento imobiliário;
- Promove boas práticas de **FinOps (Financial Operations)** na nuvem.

## 📈 Diagrama de Gerenciamento de Instâncias EC2
<p align="center">
  <img src="https://raw.githubusercontent.com/SEU_USUARIO/SEU_REPOSITORIO/main/01_Gerenciando_Instâncias_EC2_na_AWS/img_instancias.gif" width="400" alt="Demonstração do projeto">
</p>


