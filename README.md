# Análise de Sentimentos com **Language Studio** no Azure AI — Laboratório DIO

Este guia reúne todos os pontos, imagens e passos realizados durante o laboratório. Ele serve como um **passo a passo prático** para configurar e usar os serviços de **Processamento de Linguagem Natural (NLP)** do Azure.

---

## 📌 Visão geral — NLP no Azure

O **Azure AI Language (Language Service)** oferece:

- 🗣 **Detecção de idioma**
- 😀 **Análise de sentimento e opiniões**
- 📝 **Extração de frases-chave**
- 🏷 **Reconhecimento de entidades nomeadas (NER)**
- ❓ **Perguntas e Respostas prontas (QnA)**
- 💬 **Compreensão de linguagem conversacional (CLU)**
- ✂ **Sumarização de texto**
- 🩺 **Text Analytics for Health (saúde)**

> Tudo pode ser testado no **Language Studio** e depois consumido via API.

---

## 🔍 O que é o Language Studio?

O **Language Studio** é uma interface web que permite **testar e validar** os recursos do Azure AI Language sem escrever código.  
Com ele, é possível colar um texto, escolher o recurso (ex.: *Analyze sentiment and opinions*) e ver resultados como:
- Idioma detectado
- Sentimento geral e por sentença
- Entidades reconhecidas
- Frases-chave extraídas

---

## 🧩 Elementos comuns numa análise de texto

- **Idioma predominante** (ex.: `pt` para Português)  
- **Sentimento** (positivo, neutro, negativo)  
- **Frases-chave** (temas principais)  
- **Entidades** (pessoas, locais, organizações, datas...)

**Exemplo:**

- **Texto:** "A entrega atrasou dois dias, mas o suporte foi excelente."
- **Idioma:** pt
- **Sentimento:** misto (negativo sobre prazo, positivo sobre suporte)
- **Frases-chave:** entrega, suporte
- **Entidades:** (nenhuma específica)


---

## 🤖 Azure Bot Service (visão geral + integração com IA)

O **Azure Bot Service** hospeda bots criados com **Bot Framework** (C#, Node.js) ou **Bot Framework Composer**.

**Integrações comuns**:
- **Language Service (CLU)** para entender intenções e entidades
- **QnA (Language QnA)** para FAQ
- **Azure OpenAI** para respostas gerativas
- **Speech** para voz

**Fluxo básico**:
1. Criar o bot (Bot Channels Registration / Web App Bot)
2. Publicar o endpoint
3. Conectar canais (Web Chat, Teams, WhatsApp...)
4. Integrar com serviços de IA

---

## 🧠 CLU — Compreensão de linguagem coloquial

O **Conversational Language Understanding** serve para identificar:
- **Intenções** (o que o usuário quer fazer)
- **Entidades** (informações importantes no contexto)

---

## 🎙 Speech — Reconhecimento e Síntese de Fala

- **STT (Speech-to-Text)**: converte áudio para texto  
- **TTS (Text-to-Speech)**: converte texto em áudio  
- Ideal para criar assistentes de voz combinando com Language

---

## 📜 Passo a passo — Language Studio (Análise de Sentimento)

1. **Criar recurso**
   - Portal Azure → **Create a resource**
   - **AI + Machine Learning** → **Language Service**
   - Escolher **região**, **grupo de recursos** e nome

2. **Abrir Language Studio**
   - Acesse e associe ao recurso criado

3. **Rodar experimento**
   - Menu: **Classify text → Analyze sentiment and opinions**
   - Selecione o idioma
   - Cole o texto
   - Aceite termos e clique em **Run**
   - Veja resultados de sentimento, opiniões e confiança

---

## 📜 Passo a passo — Speech Studio (Fala → Texto em tempo real)

1. **Criar recurso de Speech**
   - Portal Azure → **Create a resource → Speech**

2. **No Speech Studio**
   - Associar recurso
   - Escolher **Real-time speech to text**
   - Selecionar idioma e áudio/microfone
   - Iniciar captura e acompanhar a transcrição

---

## 📌 Menu lateral útil no Portal Azure

- Create a resource  
- Resource groups  
- Azure AI services / Language  
- Azure Machine Learning  
- Virtual machines  
- SQL databases  
- Microsoft Defender for Cloud  
- Microsoft Entra ID  

---

## ✅ Checklist rápido — Language Studio

- [ ] Recurso **Language Service** criado  
- [ ] Associado ao **Language Studio**  
- [ ] Teste de **Analyze sentiment and opinions** feito  
- [ ] Testes opcionais: **Key phrase extraction**, **NER**, **Summarization**  
- [ ] (Opcional) Configuração do **QnA**

---

## 💡 Boas práticas

- Criar serviços na **mesma região** para reduzir latência  
- Usar **Free Tier** sempre que possível  
- Apagar recursos após o uso  
- Anonimizar dados sensíveis  
- Depois de validar no Studio, migrar para **SDK/API**  
- Em bots, separar intents (CLU) e FAQ (QnA)

---
