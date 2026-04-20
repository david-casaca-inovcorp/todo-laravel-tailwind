# Aplicação To-Do com Laravel e Tailwind CSS

## Sobre o projeto

Esta aplicação foi desenvolvida para gestão simples e intuitiva de tarefas do dia a dia.
O objetivo é permitir ao utilizador criar, visualizar, editar, concluir e remover tarefas de forma rápida, com uma interface limpa e responsiva.

A aplicação segue uma estrutura organizada com Laravel no backend e Tailwind CSS no frontend.

## Tecnologias utilizadas

- **Laravel**
- **Tailwind CSS**
- **MySQL**
- **JavaScript básico**
- **Pest** para testes

## Funcionalidades implementadas

- Criar novas tarefas
- Definir título obrigatório
- Adicionar descrição opcional
- Definir data de vencimento
- Definir prioridade: baixa, média ou alta
- Editar tarefas existentes
- Eliminar tarefas
- Marcar tarefas como concluídas ou pendentes

### Listagem e filtros
- Visualizar todas as tarefas
- Filtrar por estado:
  - pendente
  - concluída
  - todas
- Filtrar por prioridade
- Filtrar por data de vencimento
- Pesquisar tarefas por título
- Consultar os detalhes de cada tarefa

### Interface
- Layout responsivo para desktop, tablet e mobile
- Design simples e organizado com Tailwind CSS
- Estrutura visual consistente

## Estrutura principal do projeto

### Backend
A aplicação segue o padrão MVC do Laravel:

- **Model**: responsável pela lógica da entidade Task
- **Controller**: responsável pelo fluxo das operações
- **Migrations**: responsáveis pela estrutura da base de dados
- **Form Requests**: responsáveis pela validação dos dados

### Frontend
O frontend foi construído com Tailwind CSS, usando classes utilitárias para manter consistência visual e facilitar manutenção.

Também foi criado um formulário parcial reutilizável para criação e edição de tarefas.

## Estrutura da base de dados

A tabela principal é a tabela `tasks`, que guarda os seguintes dados:

- `id`
- `title`
- `description`
- `due_date`
- `priority`
- `status`
- `created_at`
- `updated_at`

Foram adicionados índices para melhorar o desempenho das pesquisas e filtros.

## Validação de dados

A validação é feita no backend através de **Form Requests**, garantindo integridade e consistência dos dados inseridos.

Exemplos de validação:
- título obrigatório
- prioridade limitada aos valores permitidos
- estado limitado aos valores permitidos
- datas validadas corretamente

## Requisitos

Antes de correr o projeto, confirma que tens instalado:

- PHP 8.2 ou superior
- Composer
- Node.js e npm
- MySQL

## Instalação do projeto

### 1. Clonar o repositório

```bash
git clone <url-do-repositorio>
cd tasks
```

### 2. Instalar dependências PHP

```bash
composer install
```

### 3. Instalar dependências frontend

```bash
npm install
```

### 4. Configurar o ficheiro `.env`

Criar o ficheiro `.env` com base no exemplo:

```bash
cp .env.example .env
```

Depois ajustar as credenciais da base de dados MySQL:

```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=tasks
DB_USERNAME=root
DB_PASSWORD=
```

### 5. Criar a chave da aplicação

```bash
php artisan key:generate
```

### 6. Executar as migrations

```bash
php artisan migrate
```

### 7. Compilar os assets

```bash
npm run dev
```

### 8. Iniciar o servidor local

```bash
php artisan serve
```

## Utilização

Depois de arrancar o projeto, a aplicação permite:

- adicionar tarefas
- editar tarefas
- ver detalhes
- aplicar filtros
- mudar estado das tarefas
- apagar tarefas

A página principal redireciona para a listagem de tarefas.

## Testes

Para executar os testes:

```bash
php artisan test
```

Ou, se preferires Pest diretamente:

```bash
./vendor/bin/pest
```

---

## Acessibilidade e usabilidade

Na construção da interface foram seguidos princípios de clareza visual, legibilidade e simplicidade de navegação.

Foram utilizados:
- labels nos formulários
- contrastes visuais adequados
- estrutura limpa e consistente
- layout adaptável a vários dispositivos

---

## Organização e versionamento

O projeto deve ser mantido com versionamento Git e commits organizados, com mensagens claras e objetivas.

Exemplos de commits:

```bash
git commit -m "feat: adicionar criação de tarefas"
git commit -m "feat: implementar filtros por estado e prioridade"
git commit -m "fix: corrigir validação da data de vencimento"
git commit -m "style: melhorar responsividade da listagem"
```

## Melhorias futuras

Algumas melhorias que podem ser adicionadas:

- autenticação de utilizadores
- paginação na listagem
- testes mais completos para todas as operações CRUD
- notificações de tarefas próximas do vencimento
- categorias ou etiquetas para tarefas

## Autor

Projeto desenvolvido no âmbito académico, com foco na aprendizagem de Laravel, Tailwind CSS e boas práticas de desenvolvimento web.
