# Projeto DataCamp - 3

Sistema multiagente** com [CrewAI], organizado em um _notebook_ (`agent.ipynb`) que define agentes com **role**, **goal**, **task** e **backstory**, e executa as tarefas em processo **sequential**.

## Roel
**Planejador de Viagem** → 
Goal: Planejar a viagens com roteiro com os passeios e atividades.

## Task
**Criar um roteiro de viagem para a Europa, considerando as cidades, atividades e transporte.** (agente: `planejador_de_viagem`) → Saída esperada: Um roteiro de viagem com a sequência de cidades a serem visitadas, as     principais atividades das cidades e o transporte a ser utilizado
**Calcule o orçamento total da viagem, incluindo transporte, hospedagem e atividades.** (agente: `orcamentista`) → Saída esperada: Um valor com os custos aproximados para cada um dos itens da viagem

## Basckstory
**Descreve a atividade.**
** Backstory** : Você é um planejador de viagens experiente, especializado em criar roteiros personalizados para diferentes destinos. Seu objetivo é ajudar os clientes a planejar  viagens, considerando atividades, transporte e hospedagem

## 📂 Arquivos
- `agent.ipynb` — código dos agentes e tarefas (Jupyter Notebook)
- `requirements.txt` — dependências do ambiente
- `.env` — variáveis de ambiente (**não**)
- `.venv/` — ambiente virtual local (**não**)

## ⚙️ Pré-requisitos
- Python 3.11+
- Chave de API válida (OpenAI, Groq ou Azure OpenAI)
- `pip` atualizado: `python -m pip install -U pip`

## 🛠️ Instalação
```bash
python -m venv .venv
# Windows
.\.venv\Scripts\activate
pip install -r requirements.txt
```

## Configuração (.env)
Crie um arquivo `.env` na raiz com suas variáveis (exemplo OpenAI):
```
OPENAI_API_KEY=sk-***
OPENAI_MODEL=gpt-4o-mini
LITELLM_MAX_RETRIES=6
LITELLM_RETRY_BACKOFF=2
LITELLM_TIMEOUT=120
```
> Se usar Azure OpenAI, configure `OPENAI_API_BASE`, `OPENAI_API_VERSION` e use o nome do *deployment* como modelo.

## Execução
Abra o notebook:
```bash
jupyter notebook agent.ipynb
```
Execute as células em ordem. Caso use script `.py`, adapte o comando:
```bash
python src/app.py
```

## 📦 Dependências (requirements.txt)
```
crewai
ipykernel
python-dotenv
```

---

> **Nota**: não suba `.env` nem `.venv/` para o repositório. Use `.gitignore`.
