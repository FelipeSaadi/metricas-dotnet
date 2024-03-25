# Ponderada de Métricas 22-03

## Tecnologias
Foram implementadas ferramentas responsáveis pelo monitoramento da aplicação (OpenTelemetry, Prometheus, Grafana e Jaeger), assim como a construção de uma aplicação para ser monitorada (.NET). Foi configurada a métrica de Counter de Requisições para os 2 endpoints construídos.

OpenTelemetry: ferramenta adicionada na aplicação .NET, responsável por coletar dados e emití-los para as demais ferramentas de monitoramento, utilizando o protocolo de ligação OTLP para envio dos dados para o Jaeger e do Prometheus Exporter para envio para o Prometheus, como é possível ver na imagem abaixo.

![image](https://github.com/FelipeSaadi/metricas-dotnet/assets/54749257/02bbd7c5-2b0c-4ec7-b5b3-fb3deddc28ec)


Prometheus: é um sistema de banco de dados de coleta, agregação e série temporal de métricas, sendo capaz de coletar dados periódicamente para cada serviço devidamente configurado, podendo analisá-las como séries temporais, assim como visualizá-las por meio de gráficos. 

Grafana: ferramenta que permite a criação de dashboards com diferentes fontes de dados, na implementação atual foi utilizado os dados providos do Prometheus.

Jaeger: ferramenta utilizada para rastrear atividades de sistemas distribuídos, permitindo monitorar dados, requisições e a comunicação entre múltiplas aplicações por meio de uma interface de visualização. 

## Aprendizado
Por meio dessa atividade fui capaz de aprender a configurar uma ferramenta de telemetria de métricas para monitorar uma aplicação em .NET; configurar o Prometheus para coleta e análise de métricas customizadas com exibição de gráficos temporais; configurar o Grafana para receber os dados providos do Prometheus e criar um dashboard customizado para acompanhamento das métricas; e por fim, implementar o Jaeger para monitorar a correlação de atividades da aplicação.

Fazendo todo o processo de configuração foi possível entender melhor como criar um monitoramento de uma aplicação, que utiliza diferentes endpoints. Sendo possível também identificar a possibilidade da criação de dashboards para diferentes Stakeholders, que será muito útil para meus projetos no futuro. 

## Visualizando a Métrica
Executando a aplicação:
![image](https://github.com/FelipeSaadi/metricas-dotnet/assets/54749257/968a26f1-f729-475a-8980-a07d2d70820b)

Fazendo a requisição para o endpoint:
![image](https://github.com/FelipeSaadi/metricas-dotnet/assets/54749257/c97050cd-41b9-446f-b239-4bc08c9eeeb4)

Resposta do Counter de requisições:
![image](https://github.com/FelipeSaadi/metricas-dotnet/assets/54749257/775b5103-27ac-49d9-b84c-d1852837c854)

## Prometheus
Executando o Prometheus:
![image](https://github.com/FelipeSaadi/metricas-dotnet/assets/54749257/12768e76-0c23-4aca-b509-6da5bf6d5739)

Exibindo a métrica do Counter de requisições:
![image](https://github.com/FelipeSaadi/metricas-dotnet/assets/54749257/f33fc2e8-85f7-4f96-abed-e744bb579770)

## Grafana
Exibindo a métrica do Counter de requisições:
![image](https://github.com/FelipeSaadi/metricas-dotnet/assets/54749257/a1e7a8e0-20d2-47d4-98c6-0844e5674384)

## Jaeger
Exibindo o rastreamento de atividades:
![image](https://github.com/FelipeSaadi/metricas-dotnet/assets/54749257/1081533f-585e-48e9-bba0-adaf004372d8)

Visualizando a atividade de Greeting:
![image](https://github.com/FelipeSaadi/metricas-dotnet/assets/54749257/fd607013-4777-4b24-a3a9-38fcb3f52cc3)

Visualizando a atividade de NestedGreeting:
![image](https://github.com/FelipeSaadi/metricas-dotnet/assets/54749257/8082b40c-5546-4819-b635-53aad67d53a5)
