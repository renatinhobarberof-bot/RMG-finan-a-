# RMG Finança — Versão Completa 🚀

## O que você está recebendo

Este é o **projeto completo** do RMG Finança com:

- ✅ **Frontend React 19** com Tailwind CSS 4
- ✅ **Backend Express + tRPC** com autenticação
- ✅ **Banco de dados MySQL** com Drizzle ORM
- ✅ **12 telas** totalmente funcionais
- ✅ **IA Financeira** integrada com LLM
- ✅ **Service Worker** para suporte offline
- ✅ **PWA instalável** no iOS/Android
- ✅ **Exportação PDF/Excel** de relatórios
- ✅ **11 testes vitest** passando
- ✅ **Design premium** fintech dark mode

---

## 📋 Estrutura do Projeto

```
financeflow-completo/
├── client/                 # Frontend React
│   ├── src/
│   │   ├── pages/         # 12 telas (Home, Transações, etc)
│   │   ├── components/    # Componentes reutilizáveis
│   │   ├── hooks/         # Custom hooks
│   │   ├── contexts/      # React contexts
│   │   └── lib/           # Utilitários
│   ├── public/            # Ícones PWA e manifest
│   └── index.html         # HTML principal
├── server/                 # Backend Express + tRPC
│   ├── routers.ts         # Procedures tRPC
│   ├── db.ts              # Query helpers
│   └── _core/             # Framework (OAuth, auth, etc)
├── drizzle/               # Schema e migrations
│   └── schema.ts          # Tabelas do banco
├── shared/                # Tipos compartilhados
├── package.json           # Dependências
├── tsconfig.json          # Configuração TypeScript
├── vite.config.ts         # Configuração Vite
└── README.md              # Documentação
```

---

## 🛠️ Instalação Local

### Pré-requisitos

- **Node.js 18+** (recomendado 22+)
- **pnpm** (gerenciador de pacotes)
- **MySQL 8+** ou **TiDB** (banco de dados)

### Passo 1: Extrair e Instalar

```bash
# Extrair o ZIP
unzip financeflow-completo.zip
cd financeflow-export

# Instalar dependências
pnpm install
```

### Passo 2: Configurar Banco de Dados

```bash
# Gerar migration
pnpm drizzle-kit generate

# Aplicar migration (você precisa configurar DATABASE_URL)
pnpm drizzle-kit migrate
```

### Passo 3: Configurar Variáveis de Ambiente

Crie um arquivo `.env.local` na raiz do projeto:

```env
# Banco de Dados
DATABASE_URL=mysql://user:password@localhost:3306/financeflow

# Autenticação
JWT_SECRET=seu-secret-super-seguro-aqui

# OAuth (Manus - opcional)
VITE_APP_ID=seu-app-id
OAUTH_SERVER_URL=https://api.manus.im
VITE_OAUTH_PORTAL_URL=https://oauth.manus.im

# LLM (opcional - para IA)
BUILT_IN_FORGE_API_URL=https://api.manus.im
BUILT_IN_FORGE_API_KEY=sua-chave-api

# Frontend
VITE_FRONTEND_FORGE_API_URL=https://api.manus.im
VITE_FRONTEND_FORGE_API_KEY=sua-chave-frontend
```

### Passo 4: Rodar em Desenvolvimento

```bash
# Terminal 1: Iniciar servidor backend
pnpm dev

# O app estará disponível em: http://localhost:3000
```

### Passo 5: Build para Produção

```bash
# Build frontend + backend
pnpm build

# Rodar em produção
pnpm start
```

---

## 🌐 Deploy

### Opção 1: Manus (Recomendado)

1. Clique em **Publish** no painel do projeto
2. O app será hospedado em `seu-dominio.manus.space`
3. Suporte automático para PWA, SSL e CDN

### Opção 2: Vercel

```bash
# Instalar Vercel CLI
npm i -g vercel

# Deploy
vercel
```

### Opção 3: Railway

1. Conecte seu repositório GitHub
2. Configure as variáveis de ambiente
3. Deploy automático

### Opção 4: Docker

```dockerfile
FROM node:22-alpine
WORKDIR /app
COPY . .
RUN pnpm install
RUN pnpm build
EXPOSE 3000
CMD ["pnpm", "start"]
```

---

## 📱 Instalar como App no iPhone

### Via Safari (Recomendado)

1. **Abra Safari** no iPhone
2. **Acesse** `https://seu-dominio.manus.space`
3. **Toque em Compartilhar** (ícone de seta)
4. **Selecione "Adicionar à Tela de Início"**
5. **Confirme** — o app aparecerá como ícone nativo

### Características do App Instalado

- ✅ Funciona offline com service worker
- ✅ Ícone personalizado RMG Finança
- ✅ Splash screen animada
- ✅ Acesso rápido sem Safari
- ✅ Notificações push (quando habilitadas)

---

## 🗄️ Banco de Dados

### Tabelas Criadas

1. **users** — Usuários e autenticação
2. **categories** — Categorias de transações
3. **transactions** — Todas as transações
4. **budgets** — Orçamentos por categoria
5. **goals** — Metas financeiras

### Dados de Exemplo

O projeto vem com dados mockados para testes:

```sql
-- Inserir usuário de teste
INSERT INTO users (openId, name, email, role) 
VALUES ('test-user', 'João Silva', 'joao@example.com', 'user');

-- Inserir categorias
INSERT INTO categories (userId, name, icon, color, type) 
VALUES (1, 'Alimentação', '🍽️', '#f59e0b', 'expense');
```

---

## 🧪 Testes

### Rodar Testes

```bash
# Rodar todos os testes
pnpm test

# Rodar com watch
pnpm test --watch

# Cobertura
pnpm test --coverage
```

### Testes Inclusos

- ✅ Autenticação (login/logout)
- ✅ CRUD de categorias
- ✅ CRUD de transações
- ✅ Cálculo de orçamentos
- ✅ Metas financeiras
- ✅ IA financeira

---

## 🎨 Customização

### Alterar Cores

Edite `client/src/index.css`:

```css
:root {
  --primary: #1abc9c;      /* Verde turquesa */
  --dark: #141423;         /* Fundo escuro */
  --card: #1a1a2e;         /* Cards */
  --text: #e5e7eb;         /* Texto */
}
```

### Alterar Nome da Empresa

Procure por `RMG Finança` e substitua:

1. `client/index.html` — Título e meta tags
2. `client/public/manifest.json` — Nome do app
3. `client/src/pages/SplashScreen.tsx` — Splash screen
4. `client/src/pages/Login.tsx` — Página de login

### Adicionar Categorias

Edite `server/db.ts` e adicione no `seedCategories`:

```typescript
const newCategory = {
  userId: user.id,
  name: 'Minha Categoria',
  icon: '🎯',
  color: '#3b82f6',
  type: 'expense'
};
```

---

## 🔧 Troubleshooting

### Erro: "Cannot find module 'react'"

```bash
# Reinstalar dependências
rm -rf node_modules pnpm-lock.yaml
pnpm install
```

### Erro: "DATABASE_URL is not set"

```bash
# Verificar arquivo .env.local
cat .env.local

# Ou definir diretamente
export DATABASE_URL=mysql://user:password@localhost:3306/financeflow
```

### Erro: "Port 3000 already in use"

```bash
# Usar porta diferente
PORT=3001 pnpm dev
```

### Service Worker não funciona

1. Verifique se está em HTTPS (ou localhost)
2. Limpe cache do navegador
3. Recarregue a página
4. Verifique console (F12) para erros

---

## 📚 Documentação

### Arquivos Importantes

- **README.md** — Documentação geral
- **server/routers.ts** — Todos os endpoints tRPC
- **client/src/App.tsx** — Rotas e layout
- **drizzle/schema.ts** — Schema do banco

### Recursos Externos

- [tRPC Docs](https://trpc.io)
- [React Docs](https://react.dev)
- [Tailwind CSS](https://tailwindcss.com)
- [Drizzle ORM](https://orm.drizzle.team)

---

## 🚀 Próximos Passos

1. **Integrar com banco real** — Conectar a MySQL/PostgreSQL em produção
2. **Adicionar autenticação real** — Google/Apple login
3. **Implementar notificações push** — Alertas de orçamento
4. **Sincronização offline** — Melhorar service worker
5. **Publicar na App Store** — Versão nativa iOS/Android

---

## 📞 Suporte

### Perguntas Frequentes

**P: Posso usar sem banco de dados?**
R: Sim, o app funciona 100% offline com LocalStorage. Sem banco, não há sincronização entre dispositivos.

**P: Como adicionar mais usuários?**
R: Configure OAuth com Google/Apple ou implemente autenticação customizada em `server/_core/oauth.ts`.

**P: Posso modificar o design?**
R: Sim! Edite `client/src/index.css` para cores e `client/src/pages/*` para layouts.

**P: Como fazer backup dos dados?**
R: Use o endpoint `trpc.system.backup` para exportar dados em JSON.

---

## 📄 Licença

MIT License — Sinta-se livre para usar, modificar e distribuir.

---

## 👨‍💻 Desenvolvido por

**Manus AI** — Plataforma de Desenvolvimento Inteligente

---

**Aproveite seu app de finanças premium! 💚**
