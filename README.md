# RAG Seguro com Proteção contra Prompt Injection

Projeto desenvolvido para as disciplinas:
- Generative AI Advanced Net
- Governança em IA & Business Analytics

## Objetivo

Desenvolver um pipeline RAG vulnerável a Prompt Injection e implementar mecanismos de mitigação para evitar vazamento de informações sensíveis.

## Tecnologias Utilizadas

- Python
- FAISS
- Hugging Face Transformers
- Sentence Transformers
- LangChain

## Funcionalidades

- Pipeline RAG completo
- Banco vetorial FAISS
- Recuperação de contexto
- Simulação de Prompt Injection
- Guardrails de entrada e saída
- Sanitização de dados sensíveis
- Mitigação de vazamento de informações

## Ataques Testados

- Ignore Instructions
- Engenharia Social
- Jailbreak
- Exfiltração Disfarçada
- Base64 / Encoding

## Como Executar

### Instalar dependências

```bash
pip install -r requirements.txt
```

### Executar notebook

Abrir o arquivo `.ipynb` no:
- Jupyter Notebook
- Google Colab
- VSCode

## Estrutura do Projeto

```text
.
├── CP02_Gen_AI_e_Gov_em_IA.ipynb
├── requirements.txt
├── README.md
```

## Integrantes do grupo:
Bernardo Braga Perobeli | RM 562468

Felipe Stefani Honorato | RM 563380

Igor Paixão Sarak | RM 563726

Lucca Phelipe Masini | RM 564121

Luiz Henrique Poss | RM 562177

FIAP - Tecnólogo em Inteligência Artificial
