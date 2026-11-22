# Seminário Altair — Análise Exploratória dos Dados do Titanic

Projeto desenvolvido para um seminário da disciplina de **Tecnologias para Data Science**, do DCOMP/UFSJ, com foco na biblioteca **Altair** para visualização de dados em Python.

O trabalho utiliza a base `titanic.csv` para demonstrar gráficos estatísticos declarativos, interatividade e composição de visualizações. A preparação dos dados é feita com **Pandas**, e os exemplos são apresentados em um **Jupyter Notebook**, executado diretamente no VS Code.

## Arquivos do projeto

- `seminario-altair-titanic.ipynb` — notebook principal, com explicações, código, gráficos e conclusão.
- `titanic.csv` — conjunto de dados usado nos exemplos.
- `environment.yml` — dependências para criar o ambiente Conda `seminario-altair`.
- `README.md` — instruções de execução do projeto.

## Requisitos

- **Miniconda ou Anaconda** instalado.
- **VS Code** com as extensões **Python** e **Jupyter** (da Microsoft).

## Como executar no VS Code

### 1 — Baixar ou clonar o repositório
Abra o terminal (ou Git Bash / Anaconda Prompt) e vá até a pasta desejada:

```bash
git clone https://github.com/bryan5719/ufsj-ds-seminario-altair.git
cd ufsj-ds-seminario-altair
```

### 2. Criar e ativar o ambiente Conda

```bash
conda env create -f environment.yml
conda activate seminario-altair
```

Se o ambiente `seminario-altair` já existir, atualize-o em vez de criá-lo novamente:

```bash
conda env update -f environment.yml --prune
conda activate seminario-altair
```

Para conferir se o ambiente foi ativado e as bibliotecas estão disponíveis:

```bash
python --version
python -c "import pandas, altair; print('Pandas:', pandas.__version__); print('Altair:', altair.__version__)"
```

### 3. Executar o notebook

1. Abra `seminario-altair-titanic.ipynb` no explorador do VS Code.
2. No canto superior direito do notebook, clique em **Select Kernel**.
3. Selecione o ambiente Python **`seminario-altair`**.
4. Clique em **Run All** para executar todas as células.
5. Confira os gráficos e salve o notebook com **Ctrl + S**, preservando as saídas.

**Não é necessário abrir o JupyterLab no navegador:** todo o processo pode ser feito pelo próprio VS Code.

## Demonstrações com Altair

O notebook apresenta quatro recursos da biblioteca usando os dados do Titanic:

1. **Dispersão interativa:** idade versus tarifa, com cores por sobrevivência, informações ao passar o mouse e zoom.
2. **Agregações e facetas:** contagem de passageiros por sobrevivência, separada por classe.
3. **Seleção cruzada (*brushing & linking*):** seleção de pontos em um gráfico que atualiza outro gráfico.
4. **Composição de gráficos:** pontos, linha de média e comparação de tarifas por classe, com seleção interativa.

Além dos exemplos, o notebook apresenta o propósito do Altair, compara a ferramenta com outras bibliotecas de visualização e discute vantagens, limitações e possíveis aplicações.

## Problemas comuns

- **`EnvironmentNameNotFound` ou ambiente inexistente:** execute `conda env create -f environment.yml` antes de ativá-lo.
- **Ambiente já existente:** execute `conda env update -f environment.yml --prune`.
- **`ModuleNotFoundError` para `altair` ou `pandas`:** confirme que o kernel do notebook é `seminario-altair` e que o ambiente foi criado a partir do arquivo YAML.
- **Erro ao ler `titanic.csv`:** mantenha o CSV na mesma pasta do notebook e abra essa pasta como projeto no VS Code.
- **Gráficos não aparecem:** confira o kernel selecionado e execute novamente as células, começando pela de importação e preparação dos dados.

## Entrega

O material do seminário inclui o notebook `.ipynb` com suas saídas salvas e os slides da apresentação exportados em PDF. O ambiente Conda e o CSV acompanham o notebook para permitir que os exemplos sejam reproduzidos em outro computador.
