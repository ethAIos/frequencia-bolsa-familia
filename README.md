# Frequencia por Turma

Converte uma planilha de frequencia detalhada (por aluno e por dia) em uma planilha agregada por turma, com nome, CPF, faltas e porcentagem de frequencia de cada mes.

## O que faz

Lê o relatório de Frequência Detalhado gerado pelo Conecta Educação que foi colocado na pasta `dados/`, processa todas as abas como meses de frequencia e gera `saida/frequencia_por_turma.xlsx` com uma aba por turma.

Apos o processamento, o arquivo de entrada e removido automaticamente para evitar reprocessamento e duplicacao de dados.

## Como usar

1. Coloque a planilha de origem dentro da pasta `dados/`.
2. Execute o script:

```bash
uv run processar_frequencia.py
```

3. O resultado sera salvo em `saida/frequencia_por_turma.xlsx`.

## Requisitos

- Python 3.14+
- uv
- Dependencias: pandas, openpyxl

Para instalar as dependencias:

```bash
uv venv
uv pip install pandas openpyxl
```

## Compilar o executavel

```bash
uv pip install pyinstaller pillow
uv run pyinstaller frequencia_por_turma.spec
```

## Aviso importante

As pastas `dados/` e `saida/` contem informacoes pessoais de alunos. Por isso, **seu conteudo nao e versionado** neste repositorio, conforme a LGPD. Mantenha esses arquivos apenas localmente e nao os publique.
