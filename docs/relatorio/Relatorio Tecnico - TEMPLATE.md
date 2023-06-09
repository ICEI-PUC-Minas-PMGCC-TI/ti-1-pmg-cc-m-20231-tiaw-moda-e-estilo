# Informações do Projeto
`TÍTULO DO PROJETO`  

Trendy - The Look Book

`CURSO` 

Ciência da Computação-Puc Minas

## Participantes

- Vitor Lucio de Oliveira
- Vitor Dias de Britto Militão
- Júlio César Gonzaga Ferreira Silva
- Pedro Henriques Guimarães da Silveira
- Julia Gabriela dos Santos Ramalho Aleluia

# Estrutura do Documento

- [Informações do Projeto](#informações-do-projeto)
  - [Participantes](#participantes)
- [Estrutura do Documento](#estrutura-do-documento)
- [Introdução](#introdução)
  - [Problema](#problema)
  - [Objetivos](#objetivos)
  - [Justificativa](#justificativa)
  - [Público-Alvo](#público-alvo)
- [Especificações do Projeto](#especificações-do-projeto)
  - [Personas, Empatia e Proposta de Valor](#personas-empatia-e-proposta-de-valor)
  - [Histórias de Usuários](#histórias-de-usuários)
  - [Requisitos](#requisitos)
    - [Requisitos Funcionais](#requisitos-funcionais)
    - [Requisitos não Funcionais](#requisitos-não-funcionais)
  - [Restrições](#restrições)
- [Projeto de Interface](#projeto-de-interface)
  - [User Flow](#user-flow)
  - [Wireframes](#wireframes)
- [Metodologia](#metodologia)
  - [Divisão de Papéis](#divisão-de-papéis)
  - [Ferramentas](#ferramentas)
  - [Controle de Versão](#controle-de-versão)
- [**############## SPRINT 1 ACABA AQUI #############**](#-sprint-1-acaba-aqui-)
- [Projeto da Solução](#projeto-da-solução)
  - [Tecnologias Utilizadas](#tecnologias-utilizadas)
  - [Arquitetura da solução](#arquitetura-da-solução)
- [Avaliação da Aplicação](#avaliação-da-aplicação)
  - [Plano de Testes](#plano-de-testes)
  - [Ferramentas de Testes (Opcional)](#ferramentas-de-testes-opcional)
  - [Registros de Testes](#registros-de-testes)
- [Referências](#referências)


# Introdução

## Problema
  
  Junto com a passagem do tempo as pessoas tendem a mudar seus gostos, e isso interfere diretamente com a moda. Tentar se manter "estiloso" ou "dentro da moda", sempre foi um desafio para alguns, tanto por falta de tempo para aprender quanto dinheiro para seguir. Mas infelizmente, no mundo atual, a imagem que você apresenta para os outros é fundamental para sua vivência social, tornando saber se vestir algo essencial. 

  Desta forma, muitos buscam se guiar através de símbolos da moda, “influencers” ou simplesmente o que outros ao redor usam. Entretendo tais métodos tão grandes chances de falhas por dois motivos: não ter acesso as roupas recomendadas e se as roupas combinaram com a pessoa. Isso causa frustação, baixa autoestima e desestimula a busca pelo estilo próprio. 

  Sendo assim, criando uma necessidade de canais confiáveis e personalizados de guia de vestimentas, sem a parcialidade de grandes empresas que querem vender seus produtos, e assim permitindo as pessoas explorarem o próprio estilo, mas mantendo uma boa estética social. 

## Objetivos

O objetivo geral deste trabalho é a criação de um guia virtual de moda que apresente ferramentas de fácil uso e tenha conteúdo personalizado para atender todas as características de uma pessoa. 

 
Como objetivos específicos, temos: 

*Fornecer funcionalidades que permitam interagir com conjuntos de roupas criadas por usuários, e conjuntos criados pela própria plataforma; 

*Permitir a criação de vários estilos e conjuntos com o aconselhamento da plataforma, para atender gostos individuais, mas se mantendo “bem-vestida”;

*Tornar o conhecimento de moda pessoal mais acessível, independente de genero ou condição social. 

## Justificativa

 A moda e a sua relação com o indivíduo e a sociedade, trata-se de uma relação que existe para além da necessidade básica de cobrir e proteger o corpo, mas de explora o mundo visual e identidade do ser humano.
 Além disso, com o advento da internet e das redes sociais, tornou-se mais fácil para as pessoas pesquisarem e acessarem informações sobre moda, seja por meio de blogs, fóruns, sites especializados ou influenciadores digitais. Dessa forma, é seguro afirmar que há um grande número de pessoas que pesquisam sobre moda e que esse número tende a crescer cada vez mais. 

## Público-Alvo

Embora todas as pessoas possam se beneficiar de um guia para se adequar a moda, que muda constantemente, o foco deste trabalho está no público que não consegue achar um estilo que encaixe em seu corpo e personalidade, e pessoas que precisam de roupas especificas para eventos específicos (entrevistas de empregos, festas, festivais, etc...) 

Portanto, como público-alvo temos homens e as mulheres entre 14 e 30 anos que se encontram na necessidade de se reinventar e tentar “looks” novos, mas não tem conhecimento de como começar. 

# Especificações do Projeto

A definição do problema neste projeto foi fundamentada por entrevistas e pesquisas de necessidades do mundo da moda realizadas pelos membros da equipe. Sendo representada por meio de personas criadas para atender as diferentes necessidades de usuários. 

## Personas, Empatia e Proposta de Valor

As personas e suas necessidades, criadas para maior entendeminto do problema, estão representadas nas imagens a seguir: 


> **Persona 1: Enzo**

![Persona 1](images/enzo1.png)


![Proposta de Valor 1](images/enzo2.png)

> **Persona 2: Carlos**

![Persona 2](images/carlos1.png)


![Proposta de Valor 2](images/carlos2.png)




> **Persona 3: Aninha**

![Persona 3](images/aninha1.png)


![Proposta de Valor 3](images/aninha2.png)



> **Persona 4: Felipe**

![Persona 4](images/felipe1.png)


![Proposta de Valor 4](images/felipe2.png)



## Histórias de Usuários

Com base na análise das personas forma identificadas as seguintes histórias de usuários:

|EU COMO... `PERSONA`| QUERO/PRECISO ... `FUNCIONALIDADE` |PARA ... `MOTIVO/VALOR`                 |
|--------------------|------------------------------------|----------------------------------------|
|Enzo                | Saber vestir para festas casuais           | Conseguir atrair pessoas e me sentir bonito                 |
|Carlos              | Saber vestir para encontros romanticos     | Ter mais confiança e chances de me relacionar romanticamente|
|Aninha              | Saber vestir para entrevistas profissionais| Ter maiores chances em vagas de emprego                     |
|Felipe              | Ferramenta acessivel para meus clientes    | Economizar tempo e satisfação de consumidor                 |

## Requisitos

As tabelas que se seguem apresentam os requisitos funcionais e não funcionais que detalham o escopo do projeto.

### Requisitos Funcionais

|ID    | Descrição do Requisito  | Prioridade |
|------|-----------------------------------------|----|
|RF-001| Permitir que o usuário cadastre seus dados (caracteristicas) | ALTA | 
|RF-002| Relacionar o banco de dados de roupas com os dados do usúario| ALTA |
|RF-003| Permitir o usúario a criar conjuntos guiados com o banco de roupas personalizado | ALTA |
|RF-004| Opção de publicar ou privar conjuntos para outros usúarios    | MÉDIA |
|RF-005| Possuir conjuntos exemplos para facilitar o aprendizado       | MÉDIA |
|RF-006| Opção de curtir/favoritar conjuntos publicos                  | BAIXA |


### Requisitos não Funcionais

|ID     | Descrição do Requisito  |Prioridade |
|-------|-------------------------|----|
|RNF-001| O sistema deve ser responsivo para rodar em um dispositivos móvel | MÉDIA | 
|RNF-002| Deve processar dados do usuário em no máximo 3s |  BAIXA | 
|RNF-003| Deve Atualizar dados de usúario a cada 10s |  BAIXA |
|RNF-004| O site deve ter dominio acessível (Repl.it, etc) | MEDIA |  
|RNF-004| O site deve ser compativel com principais navegadores (Opera, Chrome, FireFox) |ALTA |  

## Restrições

O projeto está restrito pelos itens apresentados na tabela a seguir.

|ID| Restrição                                             |
|--|-------------------------------------------------------|
|01| O projeto deverá ser entregue até o final do semestre |
|02| Não pode ser desenvolvido um módulo de backend        |


# Projeto de Interface

Entre as prioridades para a montagem da interface do sistema, foi criado uma maior atenção na praticidade, acessibilidade e usabilidade. Sendo assim, o projeto tem o seu visual padronizado o para funcionamento em desktops e dispositivos móveis. Resultando em um ritimo único de uso em qualquer plataforma ou navegador. Mantendo a experiencia fácil e prática para todos os usuários.


## User Flow


![userFlow ](images/UserFlow.png)


## Wireframes


> **Wireframe 1: Pagina Inicial**

![Wireframe 1](images/mp.jpeg)

> **Wireframe 2: Login**

![Wireframe 2](images/Login.jpeg)

> **Wireframe 3: Seu Perfil**

![Wireframe 3](images/sp.jpeg)

> **Wireframe 4: Barra de Pesquisa**

![Wireframe 4](images/pesquisar.jpeg)

> **Persona 5: Seus Looks**

![Wireframe 5](images/looks.jpeg)

> **Wireframe 6: Criação de  Perfil**

![Wireframe 6](images/lista.jpeg)

> **Wireframe 7: Lojas Afiliadas**

![Wireframe 7](images/lojas.jpeg)

> **Wireframe 8: Mais informções**

![Wireframe 8](images/info.jpeg)


# Metodologia

A metodologia contempla os meios utilizado pela equipe tanto para a manutenção dos códigos quanto os demais artefatos para a organização do time na execução das tarefas do projeto.


## Divisão de Papéis

A equipe utiliza metodologias ágeis, sendo o Scrum a base para definição do processo de desenvolvimento.

Divisão:

- Scrum Master: Vitor Lucio;

- Product Owner: Vitor Lucio;

Equipe de Desenvolvimento:

- Vitor Dias;
- Julio Cesar Silva;
- Pedro Henriques Guimarães;
- Julia Gabriela;


## Ferramentas

Os artefatos do projeto são desenvolvidos a partir de diversas plataformas que são apresentadas na tabela a seguir:


| Ambiente  | Plataforma              |Link de Acesso |Motivo|
|-----------|-------------------------|---------------|---------------|
|Processo de Design Thinkgin  | Miro |  https://miro.com/XXXXXXX | Para melhor organização de ideias virtualmente  |
|Repositório de código | GitHub | https://github.com/XXXXXXX |  Ferramenta mais utilizada pelos membros do grupo  posteriormente |
|Hospedagem do site | Heroku |  https://XXXXXXX.herokuapp.com | Ferramenta mais utilizada pelos membros do grupo  posteriormente        |
|Protótipo Interativo | Figma | https://figma.com/XXXXXXX |  Ferramenta gratuita e simples de se usar |


## Controle de Versão

Para gestão do software desenvolvido pelo time, nossa equipe utiliza um processo baseado no Git Feature Branch Workflow, mostrado na Figura a seguir. Onde todas as alterações/manutenções do código são realizadas em branches separados, mantendo aberto as versões feitas por todos do grupo individualmente.

 ![Exemplo de Wireframe](images/Github-Workflow.png)


# Projeto da Solução
No projeto de solução foi decidido tomar foco na funcionalidade principal do projeto: a recomendação de combinações e estilos de roupas para o usuário de forma a guia-lo na escolha de algo que se encaixe no que ele procura.

## Tecnologias Utilizadas

Para resolver o problema no qual o projeto foca, foi criada uma aplicação web utilizando HTML (para a estruturação da página), CSS e Bootstrap(para a estilização), JavaScript com o LocalStorage (para tornar o site dinâmico e guardar dados localmente). Além disso foram utilizadas outras tecnologias: o Figma, para criar o Wireframe do projeto; o Chat GPT, para auxiliar o desenvolvimento; o Looka para a criação da logo e, por fim, o Replit foi o principal ambiente de desnvolvimento do projeto.
![Tecnologias](images/DiagramaTecnologias.png)

Como é mostrado no User Flow, o usuario terá acesso a uma página de Login ou Cadastro, que o levará para a página principal de looks, com uma barra lateral onde estarão as páginas de carcteristicas e preferências, perfil, Lojas afiliadas e Mais Informações.
![userFlow ](images/UserFlow.png)

## Arquitetura da solução

Na arquitetura da solução temos o projeto web utilizando HTML, CSS, JavaScript (para a estruturação, estilização e tornar a página dinâmica e responsiva) e LocalStorage (para salvar os dados localmente), o projeto foi disponibilizado na internet por meio do Replit.
![Arquitetura](images/Arquitetura.png)


# Avaliação da Aplicação

Os cenários de testes utilizados foram dividos seguindo as funcionalidades aplicadas no projeto: o primeiro cenário sendo o cadastro e login de um usuário, o segundo a navegação pela barra lateral da página, o terceiro o acesso a tela de perfil e edição de informações do usuário, o terceiro o acesso as telas informativas, e o quarto, e ultimo, a possibilidade de pesquisa de looks e sugestões de combinações para o usuário, com a opção de salvar essas sugestões no site. Dessa forma, cada um dessas funcionalidades foi testadas e os resultados foram satisfatórios; algumas funcionalidades que incialmente estavam no projeto foram descartadas a partir dos testes ao serem consideradas incompatíveis com a ideia principal do projeto ou por problemos no desenvolvimento.

## Plano de Testes

Para realizar os testes foi reunido um grupo de dez pessoas, onde os testes foram divididos em fases de acordo com as funcionalidades aplicadas no site, unindo assim os testes de unidade, integração e usabilidade.

### Requisitos Funcionais

|ID    | Funcionalidades testadas|
|------|---------------------------------------------|
|RF-001| Feito e testado com sucesso| 
|RF-002| Feito e testado com sucesso|
|RF-003| Feito e testado com sucesso|
|RF-004| Descartado|
|RF-005| Feito e testado com sucesso|
|RF-006| Descartado|


### Requisitos não Funcionais

|ID     | Funcionaliades testadas|
|-------|-----------------------------|
|RNF-001| Feito e testado com sucesso| 
|RNF-002| Feito e testado com sucesso| 
|RNF-003| Feito e testado com sucesso |
|RNF-004| Feito e testado com sucesso |  
|RNF-004| Feito e testado com sucesso |  


## Registros de Testes

Dessa forma, a partir dos testes realizados a equipe tomou a decisão de manter certas funcionalidades e elementos que forma pensados nas fases iniciais do projeto, porém, foi tomada a decisão de alterar alguns dos elementos e funcionalidades pensadas inicialmente ao ocorrer a identificação de pontos fracos no desenvolvimento, assim, as opções de favoritar, seguir e dar like em roupas e outros perfis forma eliminadas. O ponto forte do projeto acabou sendo a funcionalidade principal centrada na problema tratado pela aplicação web: a recomendação de combinações e peças de roupa para o usuário de acordo com o gosto de cada indivíduo.

# Referências

LAZARINI, Jader. Varejo de moda: o desafio do mercado brasileiro de R$ 115 bilhões. 2022. Disponível em: https://trademap.com.br/agencia/analises-e-relatorios/varejo-de-moda-mercado-brasileiro-lojas-renner-lren3-arezzo-arzz3. Acesso em: 10 de abril de 2023.

