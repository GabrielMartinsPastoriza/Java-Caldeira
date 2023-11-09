# Conceito inicial

A arquitetura de um sistema de software é a organização ou a estrutura dos componentes significativos do sistema que interagem através das interfaces, com os componentes compostos de componentes sucessivamente menores e de interfaces.

Uma das funções mais importantes e desafiadoras de um arquiteto de software é a definição da arquitetura para o sistema a ser desenvolvido. Com base nisso podemos falar sobre dois tipos de arquitetura:

## Arquitetura Monolitica: ##

Sistemas construídos sobre o padrão arquitetural monolítico são compostos basicamente por módulos ou funcionalidades agrupadas que, juntas, compõem o software. Como exemplos de aplicações que fazem uso do modelo monolítico, podemos citar os sistemas ERP (Enterprise Resource Planning), como o SAP ou Protheus. Estes possuem, normalmente, módulos para controle do setor financeiro, contábil, compras, entre outros, agrupados numa única solução que acessa o banco de dados.

Na arquitetura monolítica há uma dependência entre os serviços de uma mesma aplicação. De forma “grosseira” isso é um ‘monolito’.

Com a ascensão do desenvolvimento ágil, o modelo de arquitetura monolítica passou a não ser mais visto como melhor opção para aplicações robustas, uma vez que a alteração de um único serviço pode mexer com o funcionamento de outras features dependentes.

Por ser muito mais antiga, a arquitetura monolítica ainda é usada por uma maior fatia do mercado de desenvolvimento de software. Cenário este, que está mudando exponencialmente.

### Características da Arquitetura Monolitica

- Implantar a aplicação é relativamente simples, uma vez que basta fazer o deploy de um único WAR ou EAR no servidor de aplicação;
- Simples de monitorar e manter;
- Ambiente de desenvolvimento mais simples, onde uma tecnologia core é utilizada em todo o projeto.

### Quando usar Arquitetura Monolitica:

- Quando o desenvolvimento é simples, principalmente quando ainda não são claros os domínios da aplicação.
- Quando existe apenas um sistema para subir e nenhuma preocupação se este pode quebrar outros sistemas que consomem dele, simplesmente por não existir outros. É apenas um.


## Arquitetura Microserviços: ##

Arquitetura de microserviços consiste no desenvolvimento de uma aplicação como um conjunto de pequenos serviços, cada um executando em seu próprio processo. Os serviços podem ser construídos de forma modular, com base na capacidade de negócio da organização em questão.

Pelo fato dos serviços serem construídos de forma independente, a implantação e a escalabilidade podem ser tratadas de acordo com a demanda. Essa independência também permite que os serviços sejam escritos em diferentes linguagens de programação e diferentes tecnologias, visando atender a necessidades específicas da melhor maneira. Outro ponto importante é que cada serviço pode ser gerenciado por diferentes times de desenvolvimento, possibilitando a formação de equipes especializadas.


### Características da Arquitetura Microserviços:

- Fácil entendimento e desenvolvimento do projeto;
- Fácil e rápida implantação (build e deploy);
- Redução do tempo de startup, pois os microservices são menores que aplicações monolíticas em termos de código;
- Possibilidade de aplicar a melhor ferramenta para um determinado trabalho.


### Quando usar Arquitetura Microserviços:

Quando quebramos uma aplicação monolítica e grande em várias pequenas, possivelmente conseguimos escalá-las de forma separada.

Supondo que um serviço de autenticação seja chamado várias vezes durante a sessão de um usuário, com certeza o stress sobre ele é maior.

Com microsserviços, podemos escalar apenas uma parte, ao invés de ter que escalar a aplicação como um todo, como ocorre em uma arquitetura monolítica.





### Exemplos

***Arquitetura Monolitica vs Microserviços***

<img src="https://github.com/SkiereszDiego/Java-Caldeira-Privado/blob/main/aula15/monolithic_vs_microservice.png?raw=true">

A ilustração mostra a arquitetura de microserviços de um lado e a arquitetura monolitica do outro.

A seção Arquitetura de Microsserviços mostra a IU que se conecta a seis microsserviços. Dois dos microsserviços se conectam uns aos outros e quatro microsserviços se conectam a apenas um armazenamento de dados.

A seção Arquitetura Monolítica mostra os componentes UI, Lógica de Negócios e Camada de Acesso a Dados, que se conectam a um armazenamento de dados.

***Arquitetura Microserviços***

<img src="https://github.com/SkiereszDiego/Java-Caldeira-Privado/blob/main/aula15/microservice_architecture.png?raw=true">

A ilustração mostra as camadas da arquitetura de microsserviços.

A primeira camada é a camada do cliente, que contém: os computadores, laptops e dispositivos móveis.

A segunda camada é a camada do gateway de API, que redireciona as solicitações do cliente para os microsserviços apropriados.

A terceira camada é a camada de orquestração de contêineres, com todos os microsserviços agrupados dentro de uma orquestração de contêineres. Cada um dos microsserviços está em contêiner. Eles se comunicam com os clientes por meio do gateway de API.

A quarta camada é a camada de armazenamento de dados. Cada um dos microsserviços em contêiner que implementam persistência se comunica a apenas um armazenamento de dados. Os armazenamentos de dados exibidos são NoSQL e SQL.


### Conclusões

Como vemos, ambas as arquiteturas têm suas vantagens. É importante entender como você consegue o melhor de cada uma e, de certa forma, diversificar a composição dos seus serviços.

Se não for necessário ser exclusivamente microsserviço, então que não seja.

Se for interessante ter uma arquitetura monolítica por inteiro, pois o processo é consolidado e não gera falta de recursos no servidor, ou má produtividade da equipe, então continue deste jeito.



