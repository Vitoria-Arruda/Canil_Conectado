# Canil Conectado

## Sobre o projeto
O **Canil Conectado** é uma plataforma web voltada à **adoção responsável de animais**, conectando futuros adotantes a cães e gatos que estão em busca de um lar. A proposta do sistema é facilitar a divulgação de animais para adoção por pessoas físicas, organizações e abrigos de todo o Brasil, tornando o processo mais acessível, organizado e intuitivo.

> **Aviso importante:** este repositório contém **apenas o front-end** do projeto.  
> O **back-end não está disponível**, pois foi desenvolvido separadamente por outra pessoa e eu não possuo esse código atualmente.

---

## Objetivo
Desenvolver uma plataforma que auxilie no processo de adoção responsável, permitindo que usuários realizem cadastro, divulguem animais para doação e encontrem animais por meio de pesquisas e filtros, facilitando a conexão entre doadores e adotantes.

---

Este repositório disponibiliza somente a camada de **interface e interação do front-end**, incluindo:

- estrutura das páginas
- layout e estilização da aplicação
- protótipos transformados em interface web
- validação e formatação de dados inseridos pelos usuários
- interações com formulários
- responsividade
- preparação para integração com API via `fetch`

Como o back-end não está presente, funcionalidades que dependem de banco de dados, autenticação real e persistência de informações podem não estar operacionais nesta versão.

---

## Funcionalidades previstas no sistema

### Cadastro de usuários
- cadastro de usuários no sistema
- suporte a cadastro por **pessoa física (CPF)** e **pessoa jurídica (CNPJ)**, como organizações
- possibilidade de alteração de alguns dados cadastrais

### Cadastro de animais
- cadastro de animais para doação com suas informações e imagem
- edição de dados de animais já cadastrados
- exclusão do animal do sistema após a adoção

### Adoção
- pesquisa de animais por atributos
- uso de filtros para facilitar a busca
- visualização das informações do animal
- demonstração de interesse em adoção
- acesso às informações de contato do doador
- exclusão de animais da lista de interesse

---

## Funcionalidades desenvolvidas no front-end
A parte de front-end foi desenvolvida com foco na usabilidade, validação de dados e experiência do usuário.

### Validação de dados
Realiza validação e formatação dos dados inseridos pelos usuários antes do envio ao servidor, como:

- senhas
- CPF
- CNPJ
- campos obrigatórios
- formatação de entradas em tempo real

### Integração com APIs
Uso de **JavaScript** e da função **`fetch`** para comunicação com a API, permitindo o envio e recebimento de dados do back-end no projeto original.

### Interatividade
Implementação de recursos interativos com JavaScript, como:

- validação de formulários
- atualização dinâmica de conteúdo
- exibição de listas de animais
- interações com botões e fluxos de navegação

### Responsividade e acessibilidade
A interface foi planejada para funcionar de forma adequada em diferentes dispositivos e tamanhos de tela, utilizando:

- Flexbox
- media queries
- organização visual intuitiva
- preocupação com boa experiência de uso

### Estrutura visual e design
As páginas foram desenvolvidas com **HTML**, **CSS** e **JavaScript**, com base em protótipos criados anteriormente, buscando uma interface clara, funcional e organizada.

---

## Regras de negócio
O sistema foi modelado com as seguintes regras de negócio:

- somente podem ser cadastrados animais das espécies **gato** e **cachorro**
- o usuário doador somente pode divulgar um animal se estiver logado em sua conta
- o usuário doador somente pode divulgar um animal se todas as informações forem preenchidas
- o animal passa a entrar na lista de **interesse** apenas quando o adotante clicar no botão **“Me Adote”**
- não é permitido divulgar animais para venda
- fotos de animais divulgados por abrigos devem conter **marca-d’água** com nome ou logo da organização

---

## Requisitos não funcionais
O sistema foi idealizado considerando os seguintes requisitos não funcionais:

- resposta rápida às requisições do usuário, com tempo máximo de até 5 segundos
- autenticação robusta e autorização baseada em permissões
- armazenamento seguro de dados, com proteção de senhas e medidas contra ataques
- interface responsiva, intuitiva e acessível
- facilidade de manutenção e atualização do código
- suporte a crescimento e evolução do sistema
- uso eficiente de recursos do servidor
- gerenciamento eficiente de conexões com banco de dados
- conformidade com a **LGPD**

---

## Modelagem do sistema
A modelagem apresentada no projeto inclui:

### Diagrama de classes
O sistema foi estruturado com três entidades principais:

- **Usuário**
- **Animal**
- **Interesse**

Essas classes representam os principais elementos da plataforma e suas relações dentro do fluxo de cadastro, divulgação e adoção.

### Modelagem de banco de dados
O projeto original também contou com:

- modelo entidade-relacionamento
- modelo lógico do banco de dados

A estrutura foi pensada para organizar os dados de usuários, animais cadastrados e interesses demonstrados pelos adotantes.

> A modelagem do banco e o back-end faziam parte do projeto completo, mas não estão incluídos neste repositório.

---

## Jornada do usuário
O fluxo principal do sistema foi pensado da seguinte forma:

1. usuário realiza cadastro ou login
2. acessa a página inicial
3. escolhe entre doar ou adotar
4. no caso de doação, cadastra um animal com suas informações
5. no caso de adoção, pesquisa animais por filtros
6. visualiza os dados do animal
7. clica em **“Me Adote”**
8. o sistema registra o interesse
9. o adotante acessa os dados de contato do doador para dar continuidade ao processo

---

## Protótipos
O projeto também contou com protótipos de interface elaborados previamente, incluindo páginas como:

- página de login
- página de cadastro de usuários
- página principal
- página de cadastro de animais

Esses protótipos serviram como base para a construção visual do front-end.

---

## Tecnologias utilizadas
No front-end, foram utilizadas tecnologias como:

- **HTML5**
- **CSS3**
- **JavaScript**
- **Fetch API**
- **Figma** para prototipação

No projeto original, também havia modelagem para integração com banco de dados relacional.

---

## Estrutura esperada do projeto
A organização pode variar conforme a versão publicada, mas o projeto segue a lógica de separação entre páginas, estilos, scripts e assets.

Exemplo:

```bash
Canil-Conectado/
├── assets/
│   ├── img/
│   └── icons/
├── css/
│   └── style.css
├── js/
│   └── script.js
├── pages/
│   ├── login.html
│   ├── cadastro.html
│   ├── index.html
│   └── cadastro-animal.html
└── README.md
