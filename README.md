# CP02 - Generative AI Advanced Nets e Governança em IA e Business Analytics

## RAG Seguro com Proteção contra Prompt Injection

Projeto desenvolvido para a disciplina **Generative AI Advanced Net**, do curso de Tecnólogo em Inteligência Artificial da FIAP.

## Objetivo

O objetivo deste projeto é implementar um pipeline RAG (*Retrieval-Augmented Generation*) em Python, utilizando um banco vetorial FAISS para recuperar informações de um documento sensível simulado e gerar respostas com uma LLM.

Além da construção do RAG, o projeto também demonstra a vulnerabilidade da aplicação a ataques de Prompt Injection e compara o comportamento do sistema antes e depois da implementação de uma camada de proteção.

## Arquivo Principal

O notebook principal do projeto é:

```text
CP02_Gen_AI_e_Gov_em_IA.ipynb
```

## Tecnologias Utilizadas

- Python 3.10+
- Jupyter Notebook
- FAISS
- Sentence Transformers
- Hugging Face Transformers
- LangChain Text Splitters
- Pandas
- NumPy

## Estrutura do Projeto

```text
.
├── CP02 Gen AI e Gov em IA.ipynb
├── README.md
└── requirements.txt
```

## Como Executar o Notebook

### 1. Clonar o repositório

```bash
git clone https://github.com/fehonorato1107/CP02-Gen-AI-e-Gov-em-IA
```

### 2. Entrar na pasta do projeto

```bash
cd NOME-DO-REPOSITORIO
```

### 3. Instalar as dependências

Caso esteja executando localmente, instale as dependências com:

```bash
pip install -r requirements.txt
```

Caso prefira instalar manualmente, utilize:

```bash
pip install faiss-cpu langchain langchain-community langchain-text-splitters sentence-transformers transformers accelerate torch pandas numpy
```

### 4. Abrir o notebook

O notebook pode ser executado em:

- Google Colab;
- Jupyter Notebook;
- JupyterLab;
- Visual Studio Code.

Abra o arquivo:

```text
CP02 Gen AI e Gov em IA.ipynb
```

### 5. Executar as células

Caso tenha escolhido em executar no Google Colab, Altere o tipo de tempo de execução e coloque o acelerador de hardware em T4 GPU para ter uma experiência melhor para rodar as células. Depois de ter feito essa alteração, execute as células do notebook em ordem, do início ao fim.

O notebook contém as seguintes etapas:

1. Configuração do ambiente;
2. Importação das bibliotecas;
3. Definição dos modelos e parâmetros;
4. Criação do documento sensível fictício;
5. Divisão do documento em chunks;
6. Geração de embeddings;
7. Indexação no FAISS;
8. Recuperação de contexto;
9. Geração de respostas com LLM;
10. Execução do RAG sem proteção;
11. Testes com ataques de Prompt Injection;
12. Implementação de guardrails;
13. Execução do RAG com proteção;
14. Comparação dos resultados.

## Configuração dos Modelos

O notebook permite alterar os principais parâmetros na célula de configuração inicial, como:

- modelo de embeddings;
- modelo de LLM;
- tamanho dos chunks;
- overlap dos chunks;
- quantidade de documentos recuperados no top-k;
- ativação ou desativação da camada de proteção.

## Pipeline RAG

O pipeline implementado segue o seguinte fluxo:

```text
Documento sensível simulado
        ↓
Chunking
        ↓
Embeddings
        ↓
Indexação no FAISS
        ↓
Retriever
        ↓
LLM
        ↓
Resposta final
```

## Testes de Prompt Injection

Foram simuladas cinco estratégias de ataque:

1. Ignore Instructions;
2. Engenharia Social;
3. Roleplay / Jailbreak;
4. Exfiltração Disfarçada;
5. Encoding / Base64.

Esses testes foram usados para demonstrar como um sistema RAG sem proteção pode expor informações sensíveis recuperadas do banco vetorial.

## Camada de Proteção

A camada de proteção implementada inclui:

- detecção de padrões suspeitos na entrada do usuário;
- bloqueio de prompts maliciosos;
- sanitização do contexto recuperado;
- mascaramento de dados sensíveis;
- validação da resposta gerada pela LLM.

## Reprodutibilidade

Para garantir a reprodutibilidade, o projeto contém:

- notebook `.ipynb` com código e documentação;
- célula inicial de instalação de dependências;
- arquivo `requirements.txt`;
- instruções de execução neste README.

## Observação

Todos os dados sensíveis utilizados no projeto são fictícios e foram criados apenas para fins acadêmicos.

## Integrantes

- 562468 - Bernardo Braga Perobeli
- 563380 - Felipe Stefani Honorato
- 563726 - Igor Paixão Sarak
- 564121 - Lucca Phelipe Masini
- 562177 - Luiz Henrique Poss

## Instituição

FIAP - Faculdade de Informática e Administração Paulista  
Tecnólogo em Inteligência Artificial
