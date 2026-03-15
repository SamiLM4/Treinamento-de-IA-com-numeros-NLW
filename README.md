<h1 align="center">
  Implementação da LeNet-5 em PyTorch 🧠🖼️
</h1>

<p align="center">
  <img alt="Python" src="https://img.shields.io/badge/Python-3.13+-blue">
  <img alt="PyTorch" src="https://img.shields.io/badge/PyTorch-Deep%20Learning-EE4C2C">
  <img alt="License" src="https://img.shields.io/badge/License-MIT-green">
</p>

Este repositório contém o **Projeto 1** do evento da Rocketseat (NLW), onde implementamos e treinamos a clássica arquitetura de Inteligência Artificial **LeNet-5** utilizando o framework **PyTorch**, aplicada ao reconhecimentos de dígitos manuscritos (o famoso Dataset MNIST). 

---

## 🚀 Sobre o Projeto

A **LeNet-5** é uma das primeiras e mais influentes Redes Neurais Convolucionais (CNNs), criada na década de 1990 pelo pesquisador francês Yann LeCun. Originalmente focada em reconhecer caracteres de cheques bancários, ela pavimentou o caminho moderno da Visão Computacional.

O projeto foi construído em formato de Jupyter Notebook para tornar a matemática explícita e de fácil aprendizado. Durante a execução, você vai acompanhar o ciclo de vida completo de como uma máquina aprende:
1. Extração e pré-processamento de imagens.
2. Definição da arquitetura e blocos do modelo.
3. Treinamento utilizando aceleração via GPU (se dispoível).
4. Avaliação e análise visual dos erros cometidos (Loss e Accuracy).
5. Como exportar a rede inteligente final.

## 🛠 Tecnologias e Dependências

O ambiente de execução e as dependências são gerenciados utilizando o **[uv](https://github.com/astral-sh/uv)** (como observado no `pyproject.toml`). O ecossistema abrange:
- **[Python](https://www.python.org/)** `>= 3.13`
- **[PyTorch & Torchvision](https://pytorch.org/)** (Criação do modelo de IA, tensores corporais e manipulação de conjuntos de dados)
- **[Matplotlib](https://matplotlib.org/) & [NumPy](https://numpy.org/)** (Gráficos, plotagem de filtros Conv2d, cálculos matemáticos auxiliares)
- **[Jupyter Notebook](https://jupyter.org/)** (Ambiente interativo)

## 🗂 Estrutura do Repositório

- `lenet5.ipynb`: O coração do projeto — Notebook contendo código passo a passo, detalhadamente comentado, para treino da sua própria IA LeNet-5.
- `lenet5_pesos.pth`: Arquivo exportado da "memória" que armazena os pesos matemáticos treinados após o processamento. É ideal para utilizar o modelo em produção posteriormente sem precisar treiná-lo novamente!
- `main.py`: Ponto de entrada básico do projeto (`hello-world`).
- `pyproject.toml` / `uv.lock`: Arquivos de configuração de ambiente e as travas das versões de suas dependências em Python.
- `data/`: Base de dados baixada automaticamente, contendo as grandiosas 70.000 amostras (treino + teste) de dígitos da base clássica MNIST.

## 📦 Como Instalar e Rodar o Ambiente

Siga os passos abaixo, copiando para o terminal de sua máquina:

1. **Clone este repositório**:
   ```bash
   git clone <Sua_Url_Do_Repositorio_Aqui>
   cd "projeto 1"
   ```

2. **Crie e ative seu ambiente virtual** garantindo as dependências corretas instaladas.
   Utilize o ultra-rápido empacotador `uv` ou prossiga com ferramentas padrão (como o `pip`/`venv`):
   ```bash
   uv sync
   # -- (ou) instale apenas as libs referenciadas pelo requirements/TOML
   ```

3. **Execute o Jupyter Notebook**:
   Navegue com sua IDE favorita e execute `lenet5.ipynb`, ou pelo CLI:
   ```bash
   jupyter notebook lenet5.ipynb
   ```
   **Dica:** Repare na arquitetura da sua máquina! O código verificará se é possível aproveitar o poder da Placa de Vídeo. Ele identificará conexões via *CUDA* (Nvidia GPUs), bem como *MPS* para MacOS (Apple Silicon). Caso contrário, será executado lentamente pela *CPU*. 

## 🧪 Resultados Alcançados

O modelo provê uma precisão (Métrica de **Accuracy**) de aproximadamente **~98,79%** em apenas **5 Épocas** (5 repetições de aprendizado integral). Conta também com uma seção interativa para visualização dos filtros convolucionais natos da extração de *features*, além do feedback imagético exclusivo dos **erros** do modelo! 

---

> “Descomplicando a Inteligência Artificial, do primeiro Tensor até as Predições Reais com Deep Learning!”
