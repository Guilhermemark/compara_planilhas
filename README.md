# 📊 Comparador de Alunos em Excel

Este script em Python permite comparar duas colunas de alunos dentro de uma planilha Excel e gerar um relatório detalhado em formato `.txt`.

Ele identifica:

- ✅ Alunos presentes em ambas as colunas  
- ❌ Alunos exclusivos da coluna 1  
- ❌ Alunos exclusivos da coluna 2  

---

## 🚀 Funcionalidades

- Leitura de arquivos Excel (`.xlsx`)
- Normalização dos dados (remove espaços, ignora maiúsculas/minúsculas)
- Comparação eficiente usando conjuntos (`set`)
- Geração de relatório automático com data e hora
- Tratamento de erros (arquivo não encontrado, colunas inválidas, etc.)

---

## 🧰 Requisitos

Antes de rodar o script, você precisa ter instalado:

- Python 3.7+
- Biblioteca `pandas`
- Biblioteca `openpyxl` (para leitura de Excel)

### Instalação das dependências:

```bash
pip install pandas openpyxl
```

---

## 📁 Estrutura esperada

```
seu_projeto/
│
├── data/
│   └── alunos.xlsx
│
├── compara_colunas_planilha_alunos.py
└── README.md
```

---

## 📄 Formato do arquivo Excel

O arquivo Excel deve conter duas colunas com os nomes definidos no script.

### Exemplo:

| alunos_a      | alunos_b      |
|--------------|--------------|
| João Silva   | Maria Souza  |
| Ana Lima     | João Silva   |
| Carlos Melo  | Pedro Santos |

---

## ⚙️ Como usar

### 1. Configure os parâmetros no script:

```python
arquivo = "data/alunos.xlsx"
coluna_a = "alunos_a"
coluna_b = "alunos_b"
```

### 2. Execute o script:

```bash
python compara_colunas_planilha_alunos.py
```

---

## 📤 Saída gerada

O script irá gerar um arquivo:

```
relatorio_alunos.txt
```

### Exemplo de conteúdo:

```
================================================================================
RELATÓRIO DE COMPARAÇÃO DE ALUNOS
================================================================================
Arquivo: data/alunos.xlsx
Data/Hora: 23/04/2026 10:00:00

TOTAL COLUNA 1 (alunos_a): 3
TOTAL COLUNA 2 (alunos_b): 3
--------------------------------------------------------------------------------

✓ ALUNOS PRESENTES EM AMBAS AS COLUNAS:
   Quantidade: 1
   - JOÃO SILVA

✗ ALUNOS APENAS NA COLUNA 1:
   Quantidade: 2
   - ANA LIMA
   - CARLOS MELO

✗ ALUNOS APENAS NA COLUNA 2:
   Quantidade: 2
   - MARIA SOUZA
   - PEDRO SANTOS
--------------------------------------------------------------------------------
FIM DO RELATÓRIO
```

---

## 🧠 Como funciona

O script utiliza:

- `pandas` para leitura da planilha
- `set` para comparação eficiente entre listas
- `datetime` para registrar o momento da execução

### Operações principais:

- Diferença:
  - `coluna1 - coluna2`
  - `coluna2 - coluna1`
- Interseção:
  - `coluna1 & coluna2`

---

## ⚠️ Tratamento de erros

O script já trata alguns problemas comuns:

- ❌ Arquivo não encontrado  
- ❌ Nome de coluna incorreto  
- ❌ Erros inesperados  

---

## 💡 Possíveis melhorias

- Exportar relatório em `.csv` ou `.xlsx`
- Interface gráfica (GUI)
- Upload automático de planilhas
- Integração com banco de dados
- Comparação de múltiplas colunas

---

## 👨‍💻 Autor

Desenvolvido para facilitar a análise de listas de alunos de forma rápida e confiável.

---

## 📜 Licença

Uso livre para estudos e projetos pessoais.

