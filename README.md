# aws-cloudformation-dio-challenge
### Implementando a Primeira Stack com AWS CloudFormation
Este repositório documenta a conclusão do desafio "Implementando sua Primeira Stack com AWS CloudFormation" do curso da DIO (Digital Innovation One), com o objetivo de demonstrar a criação e gerenciamento de infraestrutura como código na AWS.

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
Para este desafio, decidi focar na criação de uma stack simples usando o arquivo 01-EC2.yaml. Abaixo estão os passos que segui e as escolhas que fiz durante o processo.

* Acesso ao CloudFormation: Naveguei até o serviço CloudFormation no console da AWS, garantindo que estava na seção de "Stacks" e não de "StackSets".

* Criação da Stack: Cliquei em "Create stack" e, na próxima tela, escolhi a opção de carregar um arquivo de modelo. Fiz o upload do arquivo 01-EC2.yaml.

* Configuração da Stack: Dei um nome à minha stack (MinhaPrimeiraStack) e deixei as configurações padrão para as opções de "IAM role" e "Stack failure".

IAM Role: Deixei o campo vazio, pois o CloudFormation usaria as permissões do meu usuário logado, o que é suficiente para este caso.

* Stack Failure: Mantive a opção padrão "Roll back all stack resources". Isso garante que, se algo falhar, todos os recursos serão excluídos para manter um ambiente limpo e consistente.

* Criação e Revisão: Revisei todas as informações e confirmei a criação da stack. O CloudFormation começou a provisionar a instância EC2. A stack mudou de status para CREATE_COMPLETE quando o processo foi concluído.

### Insights e Conclusões
Este desafio prático foi essencial para consolidar meu entendimento sobre CloudFormation. Aprendi que:

* Infraestrutura como Código (IaC): O CloudFormation permite definir a infraestrutura em um arquivo de texto, tornando-a reutilizável, versionável e automatizada.

* Diferença entre Stack e StackSet: Inicialmente, me deparei com a interface de StackSets, que é para implantações em larga escala (múltiplas contas/regiões), enquanto o que eu precisava era uma stack simples (uma única conta/região).

* Política de Falhas: A opção de "roll back" é uma funcionalidade poderosa que evita ambientes inconsistentes, o que é uma das grandes vantagens do CloudFormation.

A documentação do processo no GitHub não apenas cumpriu o requisito do desafio, mas também serviu como uma ótima forma de fixar o aprendizado e criar um material de referência para futuros projetos.
