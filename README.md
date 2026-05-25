# EQS OrderTrack — PWA

**Gestão de Ordens de Serviço** para colaboradores da EQS Engenharia.

![EQS OrderTrack](./icons/icon-192.svg)

---

## 🚀 Como publicar no GitHub Pages

### 1. Criar repositório no GitHub
1. Acesse [github.com](https://github.com) e faça login
2. Clique em **"New repository"**
3. Nome sugerido: `eqs-ordertrack`
4. Deixe **Public** (necessário para GitHub Pages gratuito)
5. Clique em **"Create repository"**

### 2. Fazer upload dos arquivos
1. No repositório criado, clique em **"Add file" → "Upload files"**
2. Extraia o ZIP e arraste **o conteúdo de dentro da pasta**, não a pasta fechada:
   - `index.html`
   - `manifest.webmanifest`
   - `manifest.json`
   - `sw.js`
   - `icons/` (pasta com icon-192.png e icon-512.png)
   - `.nojekyll`
   - `README.md`
3. Clique em **"Commit changes"**

### 3. Ativar o GitHub Pages
1. No repositório, clique em **"Settings"**
2. No menu lateral, clique em **"Pages"**
3. Em **"Source"**, selecione **"Deploy from a branch"**
4. Em **"Branch"**, selecione **"main"** e pasta **"/ (root)"**
5. Clique em **"Save"**
6. Aguarde ~2 minutos e o link aparecerá no topo da página

### 4. Acessar o app
O app ficará disponível em:
```
https://SEU-USUARIO.github.io/eqs-ordertrack/
```

---

## 📱 Instalar como PWA (app no celular)

### Android (Chrome)
1. Abra o link no Chrome
2. Aguarde a página carregar. Ela pode recarregar sozinha uma vez para ativar o service worker.
3. Quando aparecer o botão **"Instalar app"** ou **"Instalar"**, toque nele e confirme.
4. Se o Chrome mostrar apenas **"Adicionar à tela inicial"**, limpe os dados do site e abra novamente o link HTTPS do GitHub Pages.

### iPhone/iPad (Safari)
1. Abra o link no Safari
2. Toque em **Compartilhar** (ícone de caixa com seta)
3. Toque em **"Adicionar à Tela de Início"**
4. Confirme

---

## 📂 Estrutura do projeto

```
eqs-ordertrack/
├── index.html        ← App principal (toda a lógica)
├── manifest.webmanifest ← Manifest PWA usado pelo navegador
├── manifest.json     ← Configurações PWA
├── sw.js             ← Service Worker (modo offline)
├── .nojekyll         ← Publicação direta no GitHub Pages
├── README.md         ← Este arquivo
└── icons/
    ├── icon-192.png  ← Ícone 192×192
    └── icon-512.png  ← Ícone 512×512
```

---

## ✅ Funcionalidades

| Recurso | Descrição |
|---|---|
| 🔐 Login | Identificação por nome, salva últimos 5 usuários |
| 📋 Gestão de OS | Criar, editar, excluir ordens de serviço |
| 🏢 Agência | Nome da agência vinculado ao chamado |
| 📊 Status | Em Aberto, Pendente, Vencido, Prioridade, Concluído |
| 🔔 Alertas | Notificações de OS vencendo hoje e amanhã |
| 📅 Filtro | Filtrar por período de datas (lançamento/vencimento) |
| 📎 PDF | Anexar e visualizar PDF por chamado |
| 📤 Excel | Exportar histórico em .xlsx |
| 📄 PDF | Exportar relatório para impressão |
| 🌐 Offline | Funciona sem internet após primeiro acesso |
| 📱 PWA | Instalável na tela inicial do celular |

---

## 🎨 Identidade Visual

- **Paleta:** Vermelho `#CC0000` · Preto `#080808` · Amarelo `#FFD700` · Branco
- **Tipografia:** Bebas Neue + Barlow Condensed + Barlow
- **Tema:** Dark mode industrial

---

## 💾 Armazenamento de Dados

- **OS:** `localStorage` do navegador (dados persistem no dispositivo)
- **PDFs:** `IndexedDB` do navegador (armazenamento local maior)
- **⚠️ Importante:** Os dados são locais por dispositivo. Para compartilhar entre usuários, seria necessário um backend.

---

*EQS Engenharia — EQS OrderTrack v2.0*
