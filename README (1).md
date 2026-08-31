# 🛡️ MVP — Unidade de Controle de Dados (UCD)
> **Projeto:** Pipeline de Governança, Qualidade de Dados e Predição de Risco de Saúde  
> **Base Piloto:** *Kaggle — Diabetes Risk Prediction* (15.000 registros | 19 variáveis)  
> **Status:** `MVP Concluído` | **Linguagem:** Python 3.10+

![Python](https://img.shields.io/badge/Python-3.10%2B-blue?style=flat-square&logo=python)
![LGPD](https://img.shields.io/badge/Conformidade-LGPD-green?style=flat-square)
![Dataset](https://img.shields.io/badge/Dataset-15k--Pacientes-orange?style=flat-square)
![Status](https://img.shields.io/badge/Status-Pronto%20para%20Produ%C3%A7%C3%A3o-brightgreen?style=flat-square)

---

## 📌 Visão Geral

Este repositório contém o **Minimum Viable Product (MVP)** para a criação de uma **Unidade de Controle de Dados (UCD)**. A UCD opera como o núcleo de governança, responsável por garantir que dados sensíveis de saúde sejam ingeridos com **segurança (LGPD)**, **qualidade auditada** e prontos para alimentar **modelos preditivos de apoio à decisão**.

O projeto utiliza um dataset real do Kaggle sobre risco de diabetes (`diabetes_risk.csv`), simulação que demonstra o ciclo de vida completo de um ativo de dados em uma empresa do setor de saúde.

---

## 🔄 Fluxo do Pipeline (O que o Notebook executa)

```text
[ Base de Dados Bruta ]
          │
          ▼
1. Ingestão & Inspeção ──────► Validação do tamanho e formato do dataset (15k x 19)
          │
          ▼
2. Adequação LGPD ───────────► Criptografia Hashing (SHA-256) na coluna `patient_id`
          │
          ▼
3. Qualidade & Limpeza ──────► Tratamento de dados ausentes (25% em consumo de álcool)
          │
          ▼
4. Análise Exploratória (EDA) ► Visualização gráfica de marcadores (Glicemia, Idade, IMC)
          │
          ▼
5. Machine Learning ─────────► Treinamento de Random Forest para classificação de risco
          │
          ▼
[ Saída Auditada & Modelo Preditivo ]
```

---

## 🚀 Como Executar o Projeto

### Opção 1: No Google Colab (Recomendado)
1. Baixe o arquivo [`UCD_Diabetes_Risk_MVP_v2.ipynb`](./UCD_Diabetes_Risk_MVP_v2.ipynb) deste repositório.
2. Acesse o [Google Colab](https://colab.research.google.com/) e faça o upload do notebook.
3. Envie o arquivo `diabetes_risk.csv` para a sessão do Colab.
4. Clique em **Ambiente de execução > Executar tudo** (`Ctrl + F9`).

### Opção 2: Localmente
```bash
# 1. Clone este repositório
git clone https://github.com/SeuUsuario/SeuRepositorio.git
cd SeuRepositorio

# 2. Instale as dependências
pip install pandas numpy matplotlib seaborn scikit-learn

# 3. Abra o Jupyter Notebook
jupyter notebook UCD_Diabetes_Risk_MVP_v2.ipynb
```

---

## 🛠️ Tecnologias e Bibliotecas Utilizadas

- **Python:** Linguagem base de processamento.
- **Pandas & NumPy:** Manipulação, limpeza e transformação estruturada de tabelas.
- **Hashlib:** Criptografia e pseudonimização de dados pessoais sensíveis (LGPD Art. 5º).
- **Seaborn & Matplotlib:** Visualização gráfica de dados e estatísticas descritivas.
- **Scikit-Learn:** Pré-processamento (`LabelEncoder`, `train_test_split`) e modelo de inteligência artificial (`RandomForestClassifier`).

---

## 📊 Resultados do Modelo Baseline

O algoritmo de **Random Forest** obteve alta capacidade preditiva na identificação dos níveis de risco de diabetes (*Low*, *Moderate*, *High*):

- **Métricas:** Relatório completo com Acurácia, Precision, Recall e F1-Score exibidos diretamente na execução.
- **Top Fatores de Risco:** A análise de *Feature Importance* destacou a **glicemia em jejum (`fasting_blood_sugar`)** e o **nível de HbA1c (`hba1c_level`)** como os principais determinantes do modelo.

---

## 📂 Estrutura do Repositório

```text
.
├── UCD_Diabetes_Risk_MVP_v2.ipynb   # Notebook Jupyter limpo e otimizado sem warnings
├── diabetes_risk.csv                # Dataset do Kaggle (15.000 pacientes)
└── README.md                        # Documentação executiva do projeto
```

---

<sub>Desenvolvido como protótipo para a Unidade de Controle de Dados (UCD).</sub>
