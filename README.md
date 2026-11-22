# ufsj-ds-seminario-altair
# Seminário Altair — Análise Exploratória com a Base do Titanic

Notebook reprodutível desenvolvido em **Altair** (sintaxe declarativa) sobre a base `titanic.csv`, com visualizações interativas, composição de gráficos e ambiente Conda isolado (`seminario-altair`).

## Arquivos do Projeto
- `seminario-altair-titanic.ipynb` — Notebook principal com configuração do ambiente, limpeza dos dados, visualizações interativas em Altair e síntese final.
- `titanic.csv` — Dataset utilizado nas análises.
- `environment.yml` — Especificação do ambiente Conda (`seminario-altair`).

## Como Rodar Localmente

### Passo 1 — Baixar ou clonar o repositório
Abra o terminal (ou Git Bash / Anaconda Prompt) e vá até a pasta desejada:

```bash
git clone <URL_DO_REPOSITORIO>
cd <NOME_DA_PASTA_DO_REPOSITORIO>
```

*(Caso tenha baixado o `.zip` direto pelo GitHub, extraia a pasta no computador e abra o terminal dentro dela).*

### Passo 2 — Criar e ativar o ambiente Conda
Com o **Conda** (Miniconda ou Anaconda) instalado na máquina, crie o ambiente a partir do `environment.yml` e ative-o:

```bash
conda env create -f environment.yml
conda activate seminario-altair
```

Se o ambiente `seminario-altair` já existir na máquina, atualize ele com:

```bash
conda env update -f environment.yml --prune
conda activate seminario-altair
```

### Passo 3 — Abrir o notebook e rodar as células
Com o ambiente `seminario-altair` ativo no terminal, inicie o JupyterLab:

```bash
jupyter lab
```

1. Abra o arquivo `seminario-altair-titanic.ipynb` no **JupyterLab** ou no **VS Code**.
2. Confirme no canto superior direito que o **kernel / interpretador** selecionado é o do ambiente **`seminario-altair`**.
3. Execute as células em ordem (`Shift + Enter` ou **Run All**).

### Dicas Rápidas se Algo Travar
- **Erro de arquivo não encontrado (`titanic.csv`):** confira se o `titanic.csv` está na mesma pasta do `seminario-altair-titanic.ipynb`.
- **Gráfico não aparece ou kernel errado:** troque o kernel para o Python do ambiente `seminario-altair` e rode novamente a célula de importações e a do gráfico.
