# Projeto final 

## Desenvolvimento de Plataforma para Entusiastas da Franquia Zelda

![image](https://github.com/SkiereszDiego/Java-Caldeira-Privado/blob/702086bc0550b78f3958f3d2a623a52cb7253f71/aula17-desafio-final/zelda1.gif)

### **Objetivo:** 
Criar uma plataforma inovadora que conecta entusiastas da renomada franquia Zelda. Este software será estruturado em três microserviços distintos, cada um desempenhando um papel fundamental na experiência do usuário.

### **Hey. Listen!**

![image](https://github.com/SkiereszDiego/Java-Caldeira-Privado/blob/702086bc0550b78f3958f3d2a623a52cb7253f71/aula17-desafio-final/zelda4.gif)

### **Instruções:**

1. Certifiquem-se de que cada grupo tenha alguem responsável em criar o repostório.

2. Cada membro do grupo deve clonar o repositório para sua máquina local.

3. Pelo menos um ou dois do grupo sejam responsáveis por controlar as reuniões e remover obstáculos que possam estar impedindo o progresso da equipe.

4. A equipe deve tomar decisões e ser autogerenciável com uma cultura de responsabilidade e auto-organização.

5. Certifiquem-se de que cada classe Java possui comentários explicativos para descrever suas funcionalidades.

6. Criem uma branch "dev" a partir da "main" e para todas as tarefas deve se criar uma branch a partir da "dev".

7. Padronizem a criação de branches, podem seguir esse exemplo de padronização: 

    Nomes de branches são compostos de 3 partes:
    
        1 — Categoria do branch. As categorias podem ser os seguintes:
        
        docs: apenas mudanças de documentação;
        feat: uma nova funcionalidade;
        fix: a correção de um bug;
        perf: mudança de código focada em melhorar performance;
        refactor: mudança de código que não adiciona uma funcionalidade e também não corrigi um bug;
        style: mudanças no código que não afetam seu significado (espaço em branco, formatação, ponto e vírgula, etc);
        test: adicionar ou corrigir testes.
   
        2 — o que o branch faz em si.
        
        3 — Código da tarefa no Trello ou Jira. Ex.: PF-123 *.
        
        Exemplos de alguns nomes de branches que podem existir em nossa aplicação:
        
        feat-cadastro-veiculos-PL-123
        refactor-edicao-colaboradores-PL-355
        fix-busca-checklists-PL-232

        *PF - Projeto Final

![image](https://github.com/SkiereszDiego/Java-Caldeira-Privado/blob/9fdf6f39282d1e694baabf7a1c7c08396910a477/aula17-desafio-final/commit%20semantico.png)

8. Nunca faça commit ou push diretamente na branch "main". A branch "main" deve ser considerada como a branch principal e estável do projeto.

9. Cada membro do grupo deve fazer o commit e o push para o repositório compartilhado. É importante adicionar uma mensagem de commit descritiva, de preferencia utilizar convençõs como [Commit semantico ](https://docs.zelda.fanapis.com/docs/games) .

10. Certifiquem-se de resolver qualquer conflito que possa ocorrer durante o processo de push.

11. Depois de todos os membros do grupo terem feito seus commits, verifiquem o repositório compartilhado para garantir que tudo esteja lá.

12. Organizem pacotes de forma lógica, criem classes com responsabilidades específicas, evitem acumular muitas funcionalidades em uma classe para uma estrutura de código clara e eficiente.

13. Gasrantam que os pacotes do projeto sejam organizados de maneira lógica e coesa.

14. Promovam revisões de código entre pares para garantir que a estrutura do código atenda aos padrões estabelecidos pelo time.

15. O README deve conter intruções de configuração, execução do projeto, estrutura do projeto e equipe de desenvolvedores.

# O Projeto final

![image](https://github.com/SkiereszDiego/Java-Caldeira-Privado/blob/702086bc0550b78f3958f3d2a623a52cb7253f71/aula17-desafio-final/zelda.gif)

## 1. API de Usuário (CRUD):
- Desenvolva uma API REST responsável por operações CRUD (Criar, Ler, Atualizar, Deletar) relacionadas aos perfis de usuário.
- Integre esta API com um Banco de Dados PostgreSQL para armazenamento seguro e eficiente das informações dos usuários. Cada usuário deve possuir id, nome e idade.

## 2. API de Consulta à API Pública Zelda:
- Crie uma API REST dedicada à consulta da API pública da franquia Zelda, disponível em [Zelda API](https://docs.zelda.fanapis.com/docs/games).
- Implemente lógicas para traduzir o corpo do JSON dos dois endpoints disponíveis dessa API externa.

## 3. API Gateway para Integração:
- Desenvolva um API Gateway que sirva como ponto de entrada unificado para os serviços anteriores.
- Integre de forma eficiente as APIs de Usuário e de Consulta à API Pública para criar uma experiência coesa para os usuários finais.

![image](https://github.com/SkiereszDiego/Java-Caldeira-Privado/blob/9fdf6f39282d1e694baabf7a1c7c08396910a477/aula17-desafio-final/gateway.png)

### Observações Importantes:

**Tecnologias Utilizadas:**
- Utilize Spring Boot para implementar os microserviços, aproveitando a robustez e a flexibilidade oferecidas por esse framework.
- O banco de dados PostgreSQL será a base de armazenamento para as informações dos usuários.
- A escolha entre Maven ou Gradle fica a critério do time.
- Utilize a biblioteca Log4J para imprimir logs de sucesso ou erros, uma prática comum no dia a dia de desenvolvedores.

**Testes e Qualidade de Código:**
- Implemente testes unitários para assegurar a robustez das funcionalidades de cada microserviço.
- Mantenha um código claro e bem-estruturado, aderindo às melhores práticas de desenvolvimento.

**Metodologia Ágil:**
- Assim como na amarelinha, vamos utilizar um quadro Kanban para organização das features.
- O quadro Kanban deve ser apresentado no final do projeto.

### Acordos para o Trabalho Final:

- **MVP (Mínimo Produto Viável):**
    - Compreende a API de Usuário e a API de consulta à API pública do Zelda, com os nomes "user-service" e "zelda-service", respectivamente.
    - O MVP também inclui testes unitários em ambas as APIs.

- **Primeira Versão da Aplicação (V1):**
    - Implementar a API Gateway, chamada "gateway-service", que terá TODOS os endpoints das outras APIs que ela vai chamar.
    - Para mais informações sobre o padrão gateway, consulte [https://microservices.io/patterns/apigateway.html](https://microservices.io/patterns/apigateway.html).
    - Opcionalmente, implementar um front-end com tecnologias de sua escolha, mas que deve chamar SOMENTE o "gateway-service".

- **Segunda Versão (V2):**
    - Implementar autenticação no "user-service".
    - Após autenticado, gerar um token que deve ser passado nos outros endpoints do sistema.

- **Final Versão (V3):**
    - Implementar um cache das informações da API externa.
    - Com essas informações, associar um usuário a VÁRIOS jogos, retornando os dados do usuário junto com seus jogos preferidos da franquia Zelda.

Este projeto proporcionará aos entusiastas da franquia Zelda uma plataforma envolvente e interativa, reunindo informações detalhadas e permitindo a interação social entre os usuários. Prepare-se para mergulhar no universo de Zelda e explorar o potencial da arquitetura de microserviços em Java com Spring!

![image](https://github.com/SkiereszDiego/Java-Caldeira-Privado/blob/702086bc0550b78f3958f3d2a623a52cb7253f71/aula17-desafio-final/zelda2.gif)



