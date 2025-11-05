# Webhook Inspect

## Descrição

Webhook Inspect é uma aplicação completa para gerenciar e inspecionar webhooks. O projeto é dividido em duas partes principais:

- **API**: Responsável por capturar, armazenar e gerenciar os webhooks recebidos.
- **Interface Web**: Uma interface amigável para visualizar e interagir com os dados dos webhooks.

## Funcionalidades

### API

- Captura de webhooks em tempo real.
- Rotas para listar, criar, deletar e detalhar webhooks.
- Banco de dados gerenciado com Drizzle ORM.
- Suporte a migrações e seeds para inicialização do banco de dados.

### Interface Web

- Visualização de webhooks recebidos.
- Listagem detalhada com filtros e busca.
- Exibição de detalhes de cada webhook.
- Componentes reutilizáveis para uma experiência de usuário consistente.

## Tecnologias Utilizadas

### Backend (API)

- **Node.js**
- **TypeScript**
- **Drizzle ORM**
- **Docker** (para ambiente de desenvolvimento com `docker-compose`)

### Frontend (Web)

- **React**
- **TypeScript**
- **Vite** (para desenvolvimento e build)

## Estrutura do Projeto

```
webhook-inspect/
├── api/                # Código-fonte da API
│   ├── src/            # Código principal
│   ├── migrations/     # Migrações do banco de dados
│   ├── routes/         # Rotas da API
│   └── schema/         # Definição de esquemas do banco de dados
├── web/                # Código-fonte da interface web
│   ├── src/            # Código principal
│   ├── components/     # Componentes reutilizáveis
│   ├── routes/         # Rotas da aplicação
│   └── public/         # Arquivos estáticos
```

## Pré-requisitos

- **Node.js** (v18 ou superior)
- **PNPM** (para gerenciar pacotes)
- **Docker** (opcional, para rodar o banco de dados localmente)

## Instalação

### Clonando o Repositório

```bash
git clone https://github.com/marvieiradev/webhook-inspect.git
cd webhook-inspect
```

### Configurando a API

1. Navegue até o diretório da API:
   ```bash
   cd api
   ```
2. Instale as dependências:
   ```bash
   pnpm install
   ```
3. Configure as variáveis de ambiente no arquivo `.env` (baseado em `env.ts`).
4. Inicie o banco de dados com Docker:
   ```bash
   docker-compose up -d
   ```
5. Execute as migrações e seeds:
   ```bash
   pnpm run migrate
   pnpm run seed
   ```
6. Inicie o servidor:
   ```bash
   pnpm run dev
   ```

### Configurando a Interface Web

1. Navegue até o diretório da interface web:
   ```bash
   cd web
   ```
2. Instale as dependências:
   ```bash
   pnpm install
   ```
3. Inicie o servidor de desenvolvimento:
   ```bash
   pnpm run dev
   ```

## Uso

- Acesse a API em: `http://localhost:3000`
- Acesse a interface web em: `http://localhost:5173`

## Scripts Disponíveis

### API

- `pnpm run dev`: Inicia o servidor em modo de desenvolvimento.
- `pnpm run migrate`: Executa as migrações do banco de dados.
- `pnpm run seed`: Popula o banco de dados com dados iniciais.

### Web

- `pnpm run dev`: Inicia o servidor de desenvolvimento.
- `pnpm run build`: Gera a versão de produção.
- `pnpm run preview`: Visualiza a versão de produção localmente.

## Contribuição

Contribuições são bem-vindas! Sinta-se à vontade para abrir issues ou pull requests.

## Licença

Este projeto está licenciado sob a Licença MIT.

---

Desenvolvido por [marvieiradev](https://github.com/marvieiradev).
