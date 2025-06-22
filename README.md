# 🎬 Movie Chatbot Service

Um assistente de filmes inteligente que te ajuda a descobrir o próximo filme perfeito para assistir!

## 🌟 O que faz este chatbot?

Este microserviço é o cérebro por trás do assistente de filmes do website MoviePlanet. Ele consegue conversar de forma natural e te ajudar a encontrar recomendações personalizadas baseadas nos teus gostos e preferências.

### ✨ Funcionalidades

- **Conversas naturais** - Fala como se fosse um amigo que percebe muito de cinema
- **Recomendações inteligentes** - Sugere filmes baseados no que gostas
- **Conhecimento vasto** - Sabe sobre géneros, realizadores, atores e muito mais
- **Respostas rápidas** - Não te deixa à espera muito tempo
- **Links diretos** - Te leva diretamente aos filmes que recomenda

## 🚀 Como usar

### Pré-requisitos
- Node.js (versão 16 ou superior)
- Uma chave da API OpenRouter
- Ligação à internet (obvio, né? 😄)

### Instalação

```bash
# Clona ou faz o download do projeto
cd movie-chatbot-service

# Instala as dependências
npm install

# Configura as variáveis de ambiente
cp .env.example .env
# Edita o .env com a tua chave da API
```

### Configuração

Cria um ficheiro `.env` com as seguintes variáveis:

```env
# Chave da API OpenRouter (obrigatória)
OPENROUTER_API_KEY=key_aqui

# URL da API de filmes (opcional, tem um padrão)
MOVIE_API_URL=https://aoop-q9ib.onrender.com/api -- URL DA MINHA API PUBLICA

# Porta do servidor (opcional, padrão é 3001)
PORT=3001
```

### A correr!

```bash
# Desenvolvimento (reinicia automaticamente)
npm run dev

# Produção
npm start
```

O chatbot vai estar disponível em `http://localhost:3001`

## 🎯 Como funciona

O chatbot recebe a tua pergunta, analisa o contexto (se estás a ver um filme específico ou género), e usa inteligência artificial para te dar uma resposta personalizada e útil.

### Endpoint principal

```
POST /api/chatbot
```

**Envia:**
```json
{
  "message": "Recomenda-me um filme de ação",
  "context": {
    "title": "Top Gun: Maverick",
    "genre": "Ação"
  }
}
```

**Recebe:**
```json
{
  "response": "Com base no teu gosto por Top Gun: Maverick, recomendo Mission: Impossible...",
  "suggestions": ["Que tal algo mais antigo?", "Preferes comédia de ação?"]
}
```

## 🛠️ Tecnologias

- **Node.js & Express** - O servidor principal
- **OpenRouter API** - A inteligência artificial que faz a magia
- **Axios** - Para comunicar com outras APIs
- **CORS & Helmet** - Segurança e compatibilidade

## 🎨 Para desenvolvedores

O código está organizado de forma simples:

```
src/
├── app.js              # Servidor principal
├── config/             # Configurações
├── controllers/        # Lógica do chatbot
├── middleware/         # Validações e tratamento de erros
├── routes/            # Rotas da API
├── services/          # Integração com OpenRouter e filmes
└── utils/             # Utilitários e formatação
```

## 📝 Notas

- Este chatbot foi feito com ❤️ para o projeto MoviePlanet
- Funciona melhor quando tens uma boa ligação à internet
- As respostas são geradas por IA, por isso podem variar

---

**Feito por João Freitas** 🇵🇹
