# Projeto Integrador - Gerencia.Ai

Um modelo para o desenvolvimento do Projeto Integrador do Curso de Técnico em Desenvolvimento de Sistemas para a Internet Integrado ao Ensino Médio do IFC - Campus Araquari.

Alunos: [Carlos Eduardo](https://github.com/FaDoAdamSandler), [Gustavo de Paula](https://github.com/GustavodePaulaGorges) e [João Felipi](https://github.com/snow-sr)

Professores: [Marco André Mendes](github.com/marcoandre) e [Alann Perini](https://github.com/AlannKPerini).

Links do projeto:

-   [Documentação](github.com/FaDoAdamSandler/pi-modelo)
-   [Backend]()
-   [Frontend-Mockup](https://www.figma.com/file/XHktzx8KwSCYFRFMbHjZec/F%C3%A1brica-Build?node-id=0%3A1&t=sLv59h9FqwW3CUKk-1)

<!-- # Como usar esse modelo para o Projeto Integrador

1. Faça um fork desse repositório para a sua conta do GitHub.
2. Clone o repositório para o seu computador.
3. Abra o arquivo README.md no seu editor de texto favorito (recomendamos o [Visual Studio Code](https://code.visualstudio.com/)).
4. Tenha instalada a extensão [Markdown All in One](https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one) no seu editor de texto.
5. Edite o arquivo README.md com as informações do seu projeto. -->

<!-- # Desenvolvimento

-   As equipes serão avaliadas por cada etapa da documentação e entregas realizadas.
-   Cada equipe deverá escolher um sistema para o desenvolvimento das atividades, a partir dos modelos apresentados. -->

# Modelo de Sistema

<!-- **Nessa parte a equipe deve escolher um dos modelos de sistemas para desenvolver o projeto. Ao escolher, escreva uma breve descrição do sistema e o motivo da escolha e pode apagar os outros modelos.** -->

## 3 - Ordem de Serviço (O.S.)

**Gerenciamento de Projetos**

Um sistema para o gerenciamento de projetos desenvolvidos. Com meios de comunicação entre o coordenador do projeto e os empregaos alocados. Ordem de serviço foi o modelo mais compatível com o tipo de sistema que queremos desenvolver, um sistema para o gerenciamento de um ambiente de trabalho.


# Introdução: 

Muitas empresas tem problemas de gerenciamento, geralmente, o principal motivo é a falta de organização ou falta de feedbacks sobre o desempenho, individual e em equipe, de seus empregados. A proposta do software Gerencia.Ai é resolver esses problemas entregando uma interface que possibilita uma organização simples e funcional para seus usuários, e além disso, entregar relatórios para seus coordenadores.
 
# Situação-problema: 
O coordenador responsável por algum projeto, precisa fazer o gerenciamento, organização das tarefas, acompanhamento dos empregados, tudo sem uma plataforma  específica (em planilhas e anotações por exemplo), gerando um transtorno por conta do déficit na eficiência na comunicação da coordenação com os empregados.

# Conclusão: 
Com base nos problemas analisados, o software iria auxiliar com a falta de organização do gerenciamento dos projetos, manter os registros de forma organizada, controle dos empregados e facilitar o contato e o desenvolvimento entre equipes.

# Descrição da proposta

Baseado em todas as informações adquiridas com o cliente e a identificação dos problemas apresentados, buscamos apresentar uma proposta de desenvolvimento do software para sanar as dificultades de gerenciamento.

Para o controle e gerenciamento dos projetos cadastrados no sistema, visando padronizar e melhorar a comunicação entre as equipes e o coordenador, além disso facilitar o cadastro dos novos empregados, integrando-o com o gerenciamento dos projetos, assim obtendo maior eficiência e poupando tempo do coordenador

**Alguns pontos importantes a se destacar são:**

-   **Qual o foco de ação do software?** Permitir que os coordenadores possam ter uma interface padronizada para gerenciar seus atuais projetos, também podendo se comunicar com os empregados envolvidos, sobre o projeto, via um mural. 

-   **Os níveis de usuário do sistema**. Todos os funcionários possuem acesso ao sistema, exceto o PO (Product Owner). O sistema possui uma hierarquia de permissões que é composta por três níveis:

    -   **O primeiro nível é o administrador do sistema**, que possui permissões para remover, travar e alterar qualquer projeto no sistema, pode remover empregados inativos, adicionar novos empregados, definir reuniões gerais, notificar atrasos de entregas e aplicar punições aos empregados inadimplentes.

    -   **O segundo nível é o gerente de projetos**, que tem a permissão de criar (no máximo 2), travar, remover e alterar projetos. Além disso, ele pode assimilar empregados aos seus projetos, marcar reuniões com suas equipes, notificar empregados de seu próprio grupo e remover empregados das equipes.

    -   **O terceiro nível é o usuário comum**, também conhecido como empregado. Esse usuário possui permissões para editar os projetos em que está inscrito, enviar notas pelo "notes" e concluir tarefas.

# Regras de Negócio
 
* RN001 - Publicação de Projetos: Apenas usuários de nível gerente de projeto ou maior podem fazer a publicação dos projetos.

* RN002 - Criação de projetos: Os usuários com nível gerente ou maior podem criar projetos.

* RN003 - Expulsão de Empregados: Apenas usuários com nível administrador podem expulsar/banir/privar empregados.

* RN004 - Cadastro de Empregados: Apenas usuários com nível administrador podem  cadastrar novos empregados no sistema.
* 
* RN005 - Exclusão de projetos: apenas o responsável pelo projeto pode excluir os projetos de sua responsabilidade.

* RN006 - Avisos no mural: só um gerente de projetos ou maior pode postar um aviso no mural.
   
# Requisitos Funcionais
**Entrada**
* **RF001 - Cadastro de projetos:** O sistema deve permitir o cadastro de projetos para o gerenciamento. 
**Dados necessários:** nome do projeto, descrição, equipe responsável e prazo de entrega. 
**Nível de usuário:** gerente do projeto.


* **RF002 - Cadastro de empregados:** - O sistema deve permitir que o administrador adicione e remova empregados. 
**Dados necessários:** nome, email, cpf e senha.
**Nível de usuário:** administrador.

* **RF003 - Login:** - O sistema deve permitir que os usuários cadastrados realizem login. 
**Dados necessários:** Email e Senha
**Nível de usuário:** administrador.


* RF004 - Mural - O sistema deve permitir manter postagens criadas por gerentes dos projetos, que podem ser visualizadas pelos usuários comuns via um mural do projeto.
**Dados necessários:** Título, tipo do post(prazo, comunicado ou pergunta) e o descrição do post.
**Nível de usuário:** gerente do projeto.

* RF005 - Comunicação - O sistema deve permitir manter comentários nos posts criados pelos gerentes dos projetos.
**Dados necessários:** descrição do comentário.
**Nível de usuário:** usuário comum, gerente do projeto.

**Processo**

* RF006 - Controle de tarefas - O sistema deve permitir que os gerentes de projeto monitorem o progresso individual de cada empregado, via uma lista de tarefas individual para cada empregado.
**Dados necessários:** descrição da tarefa, lista dos empregados, cargo dos empregados no projeto.
**Nível de usuário:** gerente do projeto.

* RF007 - Apontamento de tarefas - O sistema deve permitir que os membros da equipe visualizem as tarefas atribuídas a eles e as concluam quando estiverem prontas.
**Dados necessários:** descrição da tarefa, cargo individual no projeto.
**Nível de usuário:** usuário comum.

* RF008 - Visualização do projeto - Os posts gerados pelos Gerentes do projetos poderão ser visualizados pelos usuários comuns, via um mural específico para cada projeto
**Dados necessários:** Título, tipo do post(prazo, comunicado ou pergunta) e o descrição do post.
**Nível de usuário:** usuário comum.


* RF009 - Controle de Projeto - Os posts que estiverem marcados como prazo poderão ser marcados como concluídos no prazo, com atraso ou não concluídos
**Dados necessários:** Título, estado de conclusão do prazo, e o descrição do post.
**Nível de usuário:** gerente do projeto.

* RF010 - Alocação de empregados em projetos - O sistema deve permitir que o gerente de projeto aloque empregados nos seus projetos e remova os empregados das equipes.
**Dados necessários:** lista dos alunos, cargo dos empregados no projeto
**Nível de usuário:** gerente do projeto.

* RF011 - Notificações - O sistema deve enviar notificações para o usuário comum em situações importantes ex:(prazo acabando, novos posts etc.)
**Dados necessários:** Titulo do novo post ou dias faltando para o fim do prazo, descrição da nova tarefa
**Nível de usuário:** usuário comum, gerente do projeto.

**Saída**
* RF012 - Relatórios - O sistema deve permitir que os gerentes de projeto gerem relatórios sobre o progresso do projeto, o desempenho da equipe e o tempo gasto em cada tarefa. Esses relatórios podem ser usados para avaliar o desempenho da equipe e fazer melhorias no processo de gerenciamento do projeto.
**Dados necessários:** tabela de conclusão de metas individuais de cada empregado(quando concluiu suas tarefas, quantas tarefas foram concluídas, etc), estado dos prazos do projeto(quantos foram concluídos, dentro do prazo etc.) estado de conclusão do projeto(incompleto, completo, arquivado, travado.)
**Nível de usuário:** gerente do projeto.

# Requisitos Não Funcionais

* RNF001 - Segurança - o sistema deve ser protegido contra acesso não autorizado 
* RNF002 - Manuseabilidade - o sistema deve ser capaz de aumentar ou diminuir conforme necessário 
* RNF003 - Manuseablilidade - o sistema deve ser fácil de manter e atualizar 
* RNF004 - Segurança - o sistema deve ser confiável e atender aos requisitos do usuário 
* RNF005 - Compatibilidade - o sistema deve ser compatível com outros sistemas(como o Github)
* RNF006 - Compatibilidade - o sistema deve ser compatível com Linux e Windows 
* RNF007 - Atuação - o sistema deve ser capaz de lidar com múltiplos usuários simultâneos
* RNF008 - Manutenção - o sistema deve receber manutenções recorrentes
* RNF009 - Disponibilidade - o sistema deve ficar disponível 24 horas
* RNF010 - Banco de Dados - o sistema deve ter o banco de dados em django


