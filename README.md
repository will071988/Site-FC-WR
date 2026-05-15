# FC & WR Soluções em Softwares

Site institucional em HTML, CSS e JavaScript puro, com visual premium, responsivo e pronto para deploy no Firebase Hosting.

## Estrutura

```text
/
├── public/
│   └── index.html
├── index.html
├── README.md
├── firebase.json
├── .firebaserc
└── .gitignore
```

## Sobre o projeto

O site apresenta a empresa FC & WR Soluções em Softwares, os produtos atuais e um chatbot flutuante sem backend para captar leads comerciais.

### Seções incluídas

- Header com logo e menu
- Hero section
- Dashboard visual ilustrativo
- Empresa
- Nossas Soluções
- Detalhamento do Sistema de Gerenciamento de Igrejas
- Detalhamento do Sistema de Controle Financeiro
- Detalhamento de Solução Personalizada
- CTA final
- Footer
- Chatbot flutuante com envio por WhatsApp e e-mail

## Como executar localmente

Como o projeto é estático, você pode abrir diretamente o arquivo abaixo no navegador:

- `index.html`

Se preferir, também pode servir a pasta com uma extensão local server no VS Code ou com qualquer servidor HTTP estático.

## Chatbot

O chatbot funciona totalmente no front-end e segue este fluxo:

1. Cumprimenta o visitante
2. Pergunta o nome
3. Pergunta WhatsApp ou e-mail
4. Pergunta o produto de interesse
5. Pergunta a intenção comercial
6. Solicita uma breve descrição da necessidade
7. Gera o resumo do lead
8. Libera envio por WhatsApp e e-mail

### Configurações editáveis

No arquivo `index.html`, altere os valores do objeto `companyConfig`:

```js
const companyConfig = {
  whatsapp: "5500000000000",
  email: "contato@fcwrsoftwares.com.br"
};
```

## Publicação no Firebase Hosting

### Pré-requisitos

- Node.js instalado
- Firebase CLI instalado globalmente

```bash
npm install -g firebase-tools
```

### Login

```bash
firebase login
```

### Inicializar ou selecionar projeto

Atualize o arquivo `.firebaserc` com o ID real do projeto Firebase antes do deploy.

### Deploy

```bash
firebase deploy
```

## Observações

- O Firebase Hosting está configurado para publicar a pasta `public/`
- O `index.html` da raiz foi mantido para facilitar abertura direta no navegador
- A mesma versão final do site deve ser mantida em `public/index.html`
- A estrutura foi pensada para futura migração para React/Vite, se necessário
