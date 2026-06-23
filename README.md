# Frequência por Turma

Converte uma planilha de frequência detalhada (por aluno e por dia) em uma planilha agregada por turma, com nome, CPF, faltas e porcentagem de frequência de cada mês.

## O que faz

Lê qualquer arquivo `.xlsx` colocado na pasta `dados/`, processa todas as abas como meses de frequência e gera `saida/frequencia_por_turma.xlsx` com uma aba por turma.

Após o processamento, o arquivo de entrada é removido automaticamente para evitar reprocessamento e duplicação de dados.

## Como usar

1. Coloque a planilha de origem dentro da pasta `dados/`.
2. Execute o script:

```bash
uv run processar_frequencia.py
```

3. O resultado será salvo em `saida/frequencia_por_turma.xlsx`.

## Requisitos

- Python 3.14+
- uv
- Dependências: pandas, openpyxl

Para instalar as dependências:

```bash
uv venv
uv pip install pandas openpyxl
```

## Compilar o executável

```bash
uv pip install pyinstaller pillow
uv run pyinstaller frequencia_por_turma.spec
```

## Aviso importante

As pastas `dados/` e `saida/` contêm informações pessoais de alunos. Por isso, **seu conteúdo não é versionado** neste repositório, conforme a LGPD. Mantenha esses arquivos apenas localmente e não os publique.
