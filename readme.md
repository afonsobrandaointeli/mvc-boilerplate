# MVC Boilerplate - Node.js com PostgreSQL

Uma aplicação completa seguindo o padrão MVC (Model-View-Controller) com Node.js, Express, PostgreSQL e interface web com EJS.

## 🚀 Funcionalidades

- **CRUD Completo de Usuários**: API REST para gerenciamento de usuários
- **Interface Web**: Frontend com EJS para visualização dos dados
- **Padrão MVC**: Arquitetura bem estruturada e organizada
- **Validação de Dados**: Validação usando Joi
- **Testes Automatizados**: Cobertura completa com Jest
- **PostgreSQL**: Banco de dados robusto com UUID como chave primária
- **Repository Pattern**: Separação clara entre camadas de dados

## 📋 Requisitos

- Node.js (versão 14 ou superior)
- PostgreSQL (versão 12 ou superior)

## 🛠️ Instalação

1. **Clone o repositório:**
```bash
git clone https://github.com/seu-usuario/mvc-boilerplate.git
cd mvc-boilerplate
```

2. **Instale as dependências:**
```bash
npm install
```

3. **Configure as variáveis de ambiente:**
Crie um arquivo `.env` na raiz do projeto com as configurações do banco:
```env
DB_HOST=localhost
DB_PORT=5432
DB_NAME=mvc_boilerplate
DB_USER=seu_usuario
DB_PASSWORD=sua_senha
PORT=3000
```

4. **Configure o banco de dados:**
```bash
npm run init-db
```

## 🎯 Como Usar

### Iniciar o servidor
```bash
# Desenvolvimento (com auto-reload)
npm run dev

# Produção
npm start
```

### Executar testes
```bash
# Todos os testes (usando mocks - não precisa de banco)
npm test

# Com cobertura de código
npm run test:coverage
```

Os testes são executados de forma **independente** e **rápida**, sem necessidade de configuração de banco de dados, tornando o desenvolvimento mais acessível para iniciantes.

### 📚 Vantagens dos Testes com Mocks

- **Facilidade de Aprendizado**: Ideal para estudantes de primeiro ano
- **Execução Rápida**: Testes executam em segundos 
- **Sem Dependências**: Não precisa de Docker, PostgreSQL ou configurações complexas
- **Foco no Código**: Aprenda lógica de negócio sem se preocupar com infraestrutura
- **Ambiente Controlado**: Dados previsíveis e cenários de teste claros

## 🌐 Endpoints da API

### Usuários
- `GET /users` - Lista todos os usuários
- `GET /users/:id` - Busca usuário por ID
- `POST /users` - Cria novo usuário
- `PUT /users/:id` - Atualiza usuário
- `DELETE /users/:id` - Remove usuário

### Interface Web
- `GET /` - Página inicial com lista de usuários
- `GET /about` - Página sobre

## 📁 Estrutura do Projeto

```
mvc-boilerplate/
├── config/
│   └── db.js                 # Configurações do banco de dados
├── controllers/
│   └── userController.js     # Controlador de usuários
├── models/
│   └── userModel.js         # Modelo de dados do usuário
├── repositories/
│   └── userRepository.js    # Camada de acesso aos dados
├── routes/
│   ├── userRoutes.js        # Rotas da API
│   └── frontRoutes.js       # Rotas do frontend
├── services/
│   └── userService.js       # Lógica de negócio
├── views/
│   ├── components/
│   │   └── header.ejs       # Componente de cabeçalho
│   ├── css/
│   │   └── style.css        # Estilos CSS
│   ├── layout/
│   │   └── main.ejs         # Layout principal
│   └── pages/
│       ├── page1.ejs        # Página de usuários
│       └── page2.ejs        # Página sobre
├── tests/
│   ├── fixtures/            # Dados de teste
│   ├── helpers/             # Utilitários de teste
│   └── *.test.js           # Arquivos de teste
├── scripts/
│   ├── init.sql            # Script de inicialização do BD
│   └── runSQLScript.js     # Executor de scripts SQL
└── server.js               # Servidor principal
```

## 🧪 Testes

O projeto inclui testes completos usando **mocks** para facilitar o aprendizado:

- **Testes de Unidade**: Controllers, Services, Models, Repositories com mocks
- **Testes de Rotas**: Endpoints da API usando SuperTest e mocks
- **Sem Dependências Externas**: Não requer configuração de banco de dados para testes
- **Cobertura**: Relatório detalhado de cobertura de código
- **Padrão AAA**: Arrange-Act-Assert para testes claros e organizados

## 🔧 Tecnologias Utilizadas

- **Backend**: Node.js, Express.js
- **Banco de Dados**: PostgreSQL
- **Template Engine**: EJS
- **Validação**: Joi
- **Testes**: Jest, Supertest
- **Desenvolvimento**: Nodemon
- **UUID**: Para chaves primárias

## 📊 Scripts Disponíveis

- `npm start` - Inicia o servidor em produção
- `npm run dev` - Inicia o servidor em desenvolvimento com auto-reload
- `npm test` - Executa todos os testes
- `npm run test:coverage` - Executa testes com relatório de cobertura
- `npm run init-db` - Inicializa o banco de dados

## 🤝 Contribuição

1. Fork o projeto
2. Crie uma branch para sua feature (`git checkout -b feature/nova-feature`)
3. Commit suas mudanças (`git commit -am 'Adiciona nova feature'`)
4. Push para a branch (`git push origin feature/nova-feature`)
5. Abra um Pull Request

## 📄 Licença

Este projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.