# RMG Finança 💰

**Gestão Financeira Inteligente com IA**

Um aplicativo PWA moderno, responsivo e totalmente funcional para controle de finanças pessoais. Instalável como app nativo no iPhone, Android e desktop.

---

## 🎯 Características Principais

### 📊 Dashboard Premium
- **Saldo Total** com visualização clara
- **Resumo Mensal** com receitas, despesas e economia
- **Últimas Transações** com categorias e datas
- **Gráficos Interativos** de gastos por categoria

### 💳 Gestão de Transações
- Adicionar receitas e despesas
- Editar e deletar transações
- Categorias personalizadas
- Upload de comprovantes
- Busca e filtros por data/categoria

### 📈 Orçamentos e Metas
- Definir limite mensal por categoria
- Barras de progresso visuais
- Alertas automáticos de gastos
- Metas financeiras personalizadas

### 🤖 IA Financeira
- Sugestões automáticas de economia
- Insights personalizados
- Detecção de gastos excessivos
- Recomendações inteligentes

### ⚙️ Configurações Completas
- Tema claro/escuro
- Perfil do usuário
- Segurança da conta
- Backup de dados
- Gerenciamento de notificações

---

## 📱 Instalação no iPhone (PWA)

### Via Safari (Recomendado)

1. **Abra o Safari** no seu iPhone
2. **Acesse** a URL do app
3. **Toque em Compartilhar** (ícone de seta)
4. **Selecione "Adicionar à Tela de Início"**
5. **Confirme** — o app aparecerá como ícone nativo

### Características do App Instalado
- ✅ Funciona offline com service worker
- ✅ Ícone personalizado na tela inicial
- ✅ Splash screen animada ao abrir
- ✅ Acesso rápido sem abrir Safari
- ✅ Notificações push (quando habilitadas)

---

## 🖥️ Instalação no Desktop

### Windows / Mac / Linux

1. **Clone o repositório**
   ```bash
   git clone https://github.com/renatinhobarberof-bot/RMG-finan-a-.git
   cd RMG-finan-a-
   ```

2. **Abra o arquivo**
   - Clique duplo em `index.html` ou
   - Arraste para o navegador

3. **Ou inicie um servidor local**
   ```bash
   # Python 3
   python -m http.server 8000
   
   # Node.js
   npx http-server
   ```

4. **Acesse** `http://localhost:8000`

---

## 📲 Instalação no Android

1. **Abra o Chrome** no seu Android
2. **Acesse** a URL do app
3. **Toque no menu** (⋮) → "Instalar app"
4. **Confirme** — o app será instalado

---

## 🎨 Design & Tecnologia

### Visual
- **Paleta**: Verde turquesa premium (#1abc9c) com fundo escuro elegante
- **Tipografia**: Plus Jakarta Sans (moderna e legível)
- **Animações**: Fluidas e responsivas com transições suaves
- **Responsividade**: Otimizado para iPhone, Android e desktop

### Tecnologia
- **HTML5** com semântica moderna
- **CSS3** com Grid, Flexbox e animações
- **JavaScript Vanilla** (sem dependências externas)
- **Service Worker** para suporte offline
- **LocalStorage** para persistência de dados
- **PWA** totalmente funcional

---

## 💾 Dados & Persistência

### Armazenamento Local
- Todos os dados são salvos no navegador (LocalStorage)
- Nenhum dado é enviado para servidor
- Funciona 100% offline após primeira carga
- Sincronização automática quando online

### Dados de Exemplo
O app vem com dados de demonstração:
- **Saldo**: R$ 12.450,00
- **Receitas**: R$ 8.500
- **Despesas**: R$ 3.200
- **3 Transações** de exemplo
- **3 Orçamentos** configurados
- **3 Insights** de IA

---

## 🔒 Segurança & Privacidade

- ✅ Sem login obrigatório
- ✅ Dados armazenados localmente (não enviados)
- ✅ HTTPS recomendado em produção
- ✅ Sem rastreamento ou cookies de terceiros
- ✅ Compatível com RGPD

---

## 📊 Funcionalidades Detalhadas

### Home (Dashboard)
- Saldo total em destaque
- Resumo do mês (receita, despesa, economia)
- Últimas 3 transações
- Acesso rápido a todas as seções

### Transações
- Lista completa de todas as transações
- Botão flutuante para adicionar nova
- Filtros por data e categoria
- Busca por descrição
- Edição e exclusão de registros

### Orçamento
- Visualizar limites por categoria
- Barras de progresso de consumo
- Alertas visuais quando próximo do limite
- Adicionar/editar/deletar orçamentos

### IA Financeira
- Análise automática de gastos
- Sugestões de economia
- Alertas de anomalias
- Recomendações personalizadas
- Chat com IA (versão premium)

### Configurações
- Editar perfil
- Alternar tema
- Gerenciar notificações
- Fazer backup
- Restaurar dados
- Informações do app

---

## 🚀 Roadmap Futuro

- [ ] Sincronização com banco de dados (Firebase/Supabase)
- [ ] Autenticação com Google/Apple
- [ ] Cartões de crédito integrados
- [ ] Transações recorrentes automáticas
- [ ] Relatórios em PDF/Excel
- [ ] Gráficos avançados com Chart.js
- [ ] Notificações push reais
- [ ] Modo colaborativo (compartilhar orçamento)
- [ ] Integração com APIs bancárias
- [ ] App nativo iOS/Android

---

## 📝 Como Usar

### Primeira Vez
1. Abra o app
2. Veja a splash screen animada
3. Explore o dashboard
4. Adicione suas primeiras transações
5. Configure seus orçamentos

### Adicionar Transação
1. Toque no botão **"+ Adicionar"** na aba Transações
2. Preencha os dados (descrição, valor, categoria, data)
3. Confirme
4. A transação aparecerá na lista e no dashboard

### Configurar Orçamento
1. Vá para a aba **Orçamento**
2. Toque em **"+ Novo Orçamento"**
3. Selecione a categoria
4. Defina o limite mensal
5. Salve

### Consultar IA
1. Vá para a aba **IA Financeira**
2. Veja os insights automáticos
3. Leia as recomendações
4. Implemente as sugestões

---

## 🛠️ Desenvolvimento

### Estrutura do Projeto
```
RMG-finan-a-/
├── index.html          # App completo em um arquivo
├── README.md           # Este arquivo
└── config.json         # Configurações (futuro)
```

### Customização

#### Alterar Cores
Procure no `index.html` por:
```css
--primary: #1abc9c;    /* Verde turquesa */
--dark: #141423;       /* Fundo escuro */
--card: #1a1a2e;       /* Cards */
```

#### Alterar Nome da Empresa
Procure por `RMG Finança` e substitua por seu nome.

#### Adicionar Categorias
Procure por `const categories` e adicione novas categorias.

---

## 📞 Suporte

### Problemas Comuns

**O app não funciona offline?**
- Certifique-se de que o service worker foi registrado
- Recarregue a página uma vez
- Verifique o console (F12) para erros

**Os dados não salvam?**
- Verifique se o LocalStorage está habilitado
- Tente limpar cache e recarregar
- Verifique o espaço disponível no navegador

**Não consegue instalar no iPhone?**
- Use Safari (não funciona em Chrome/Firefox no iOS)
- Toque em Compartilhar (ícone de seta)
- Procure por "Adicionar à Tela de Início"

---

## 📄 Licença

MIT License - Sinta-se livre para usar, modificar e distribuir.

---

## 👨‍💻 Desenvolvido por

**Manus AI** - Plataforma de Desenvolvimento Inteligente

---

## 🌟 Contribuições

Sugestões e melhorias são bem-vindas! Abra uma issue ou faça um pull request.

---

## 📈 Versão

**v1.0.0** - Lançamento Inicial

---

**Aproveite seu app de finanças! 💚**
