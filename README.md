# Projeto de Finalização do Curso Engenharia de Dados How Bootcamps


# Objetivo
O objetivo deste projeto é desenvolver uma plataforma de dados que faça uso da API library do Yahoo Finance (yfinance) e disponibilizar dados de performance das organizações listadas. O sistema irá coletar dados financeiros de várias empresas e instrumentos financeiros, como ações, fundos de investimento, índices, moedas e commodities.

# Motivação
A principal motivação é a possibilidade de rápido acesso a dados financeiros atualizados e confiáveis das companhias listadas nas bolsas de valores. Essas informações são cruciais e podem ser a diferença entre tomar decisões estratégicas e informadas ou ficar para trás no mercado financeiro.

# Fonte de dados
A biblioteca yfinance em Python é uma interface simples e fácil de usar para acessar dados financeiros fornecidos pelo Yahoo. Ela permite que os desenvolvedores recuperem informações como cotações de ações, histórico de preços e informações fundamentais de empresas para uma análise mais fundamentalista entre outros dados de mercado relevantes.
O acesso à documentação e à instação da biblioteca estão disponíveis neste link: https://pypi.org/project/yfinance/

# Métodos
O AWS Lambda permite que você execute código sem provisionar ou gerenciar servidores, tornando-o uma opção conveniente para executar scripts Python de forma escalável e flexível. Este serviço será utilizado para as requisições;

O Amazon S3 (bucket) será utilizado para o armazenamento temporário ou histórico dos dados;

O AWS Glue será utilizado para realizar a transformação dos dados coletados. Toda a limpeza, normalização e transformação dos dados serão realizados aqui, ou seja, antes de serem disponibilizados para consulta. O Glue será utilizado também para catalogar os dados transformados e manter um catálogo centralizado de metadados;

O Athena será utilizado para consultar os dados armazenados no bucket do S3 e no catálogo do Glue. Serão criadas tabelas para representar a estrutura dos dados, com base nos metadados catalogados pelo Glue. As consultas SQL padrão poderam ser executadas no próprio Athena para acessar e analisar os dados coletados quando necessário;

Os dados serão disponibilizados a partir do Athena para ferramentas de data visualization como por exemplo o Power Bi, que é hoje em dia uma das ferramentas mais conhecidas e utilizadas no mercado de Business Intelligence e Analytics;


# Serviços
AWS Lambda
AWS S3 Bucket
AWS Glue
AWS Athena
Library Python - yfinance

# Arquitetura

![Captura de Tela 2023-05-18 às 17 41 06](https://github.com/FlavioPulli/projeto-how-bootcamps/assets/91956134/3fe0c4a6-b1bf-42c2-adf0-22f4904d5610)
