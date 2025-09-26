# aws-cloudformation-dio-challenge
### Implementando a Primeira Stack com AWS CloudFormation
Este projeto documenta a conclusão do desafio "Implementando sua Primeira Stack com AWS CloudFormation", parte do curso de AWS da DIO (Digital Innovation One). O objetivo foi demonstrar a criação e gerenciamento de infraestrutura como código (IaC) na AWS, usando modelos CloudFormation para provisionar recursos de forma automatizada.

### Objetivos do Desafio
O desafio foi projetado para me ajudar a:

* Aplicar os conceitos de CloudFormation em um ambiente prático.

* Criar e gerenciar recursos da AWS de forma automatizada.

* Documentar processos técnicos de maneira clara e estruturada.

* Utilizar o GitHub como uma ferramenta para compartilhar documentação técnica e portfólio.

### Modelos de CloudFormation (.yaml)
Neste projeto, utilizei diferentes modelos de CloudFormation para criar recursos variados. O foco principal foi o arquivo 01-EC2.yaml, que serviu como ponto de partida, mas os outros arquivos estão aqui para demonstrar a evolução do aprendizado.

* 01-EC2.yaml: Um modelo simples que cria uma instância EC2 básica com o tipo t2.micro em uma zona de disponibilidade específica.

* 02-Apache.yaml: Um modelo que cria uma instância EC2 e, através de UserData, instala e configura um servidor Apache.

* 03-Firewall.yaml: Este modelo expande o anterior, adicionando a criação de um Grupo de Segurança (Security Group) para permitir o acesso HTTP (porta 80) à instância EC2.

### Passo a Passo da Implementação
Criei três stacks na AWS, cada uma correspondendo a um dos modelos YAML. O processo geral foi o mesmo para todas: acessei o serviço CloudFormation, selecionei "Create stack", fiz o upload do arquivo de modelo e segui as etapas de configuração.

1. Stack: MinhaPrimeiraStack
Modelo Utilizado: 01-EC2.yaml

Descrição: Esta foi minha primeira stack. O objetivo era entender o fluxo básico do CloudFormation. Deixei as opções de "IAM role" e "Stack failure" com as configurações padrão, o que demonstrou uma abordagem segura e alinhada com as boas práticas.

2. Stack: Minha-Stack-Apache
Modelo Utilizado: 02-Apache.yaml

Descrição: Esta stack me ensinou sobre a automatização de tarefas. O CloudFormation provisionou a instância EC2 e, logo em seguida, o script em UserData executou a instalação e o início do serviço Apache.

3. Stack: Minha-Stack-Com-Firewall
Modelo Utilizado: 03-Firewall.yaml

Descrição: Esta stack foi a mais completa. Além de provisionar a instância e instalar o Apache, ela criou um Security Group para permitir o acesso HTTP. Isso destacou a importância de configurar regras de firewall para que o servidor web seja acessível.

<img width="1440" height="701" alt="3 stacks" src="https://github.com/user-attachments/assets/cf129f59-4d3c-4608-9be3-2e5947469b26" />


### Insights e Conclusões
Este desafio prático foi essencial para consolidar meu entendimento sobre CloudFormation. Aprendi que:

* Infraestrutura como Código (IaC): O CloudFormation permite definir a infraestrutura em um arquivo de texto, tornando-a reutilizável, versionável e automatizada.

* Diferença entre Stack e StackSet: Inicialmente, me deparei com a interface de StackSets, que é para implantações em larga escala (múltiplas contas/regiões), enquanto o que eu precisava era uma stack simples (uma única conta/região).

* Política de Falhas: A opção de "roll back" é uma funcionalidade poderosa que evita ambientes inconsistentes, o que é uma das grandes vantagens do CloudFormation.

A documentação do processo no GitHub não apenas me ajudou a cumprir o desafio, mas também serviu como uma ótima forma de fixar o aprendizado e criar um material de referência para futuros projetos.
