# Detecção de Bordas em Imagens de Dados

## Autores
- Itor Carlos Souza Queiroz
- Lanna Luara Novaes Silva

## Sobre o Projeto

Este projeto implementa um sistema de processamento de imagens utilizando técnicas de processamento de imagens para detectar os pontos das superfícieis dos dados. O trabalho aplica uma sequência de operações de processamento de imagens, incluindo conversão para escala de cinza, suavização, detecção de bordas através do filtro de Sobel, binarização e utilização da Transformada de Hough.

## Link do dataset utilizado
[Dataset de imagens de Dados no Roboflow](https://universe.roboflow.com/workspace-spezm/dice-0sexk)

## Link do vídeo explicativo - Youtube
[Vídeo no youtube](https://www.youtube.com/watch?v=s1H1HGc5XgI)

## Objetivos

O projeto tem como principais objetivos:

1. **Conversão de Imagens**: Transformar imagens coloridas em escala de cinza, removendo o canal alpha (transparência) quando presente
2. **Suavização**: Aplicar filtro Gaussiano para reduzir ruídos e preparar as imagens para detecção de bordas
3. **Detecção de Bordas**: Utilizar o filtro de Sobel para identificar e realçar as bordas dos dados nas imagens
4. **Binarização**: Aplicar um processo de limiarização para converter a imagem em escala de cinza em uma imagem binária,
5. **Visualização**: Apresentar os resultados de cada etapa do processamento de forma comparativa

## Tecnologias Utilizadas

- **Python 3.11+**
- **NumPy**: Manipulação de arrays e operações matemáticas
- **Matplotlib**: Visualização e plotagem de imagens
- **scikit-image**: Biblioteca principal para processamento de imagens
  - Conversão de cores
  - Filtros (Gaussiano, Sobel)
  - Detecção de características
  - Transformação de Hough para círculos
  - Limiarização

## Estrutura do Projeto

```
.
├── Trabalho_Final.ipynb    # Notebook principal com todo o código
├── dices/                       # Diretório com as imagens de dados (já incluído)
│   ├── imagem1.png
│   ├── imagem2.jpg
│   └── ...
└── README.md                    # Este arquivo
```

## Como Executar o Projeto

### Pré-requisitos

1. **Python 3.11 ou superior** instalado no sistema
2. **Jupyter Notebook** ou **JupyterLab** instalado
3. **Ambiente virtual** (recomendado)

### Instalação das Dependências

#### Opção 1: Usando pip diretamente

```bash
pip install numpy matplotlib scikit-image
```

#### Opção 2: Usando ambiente virtual (recomendado)

```bash
# Criar ambiente virtual
python -m venv .venv

# Ativar ambiente virtual
# No Windows:
.venv\Scripts\activate
# No Linux/Mac:
source .venv/bin/activate

# Instalar dependências
pip install -r requirements.txt
```

### Executando o Notebook

#### Via Jupyter Notebook

1. Inicie o Jupyter Notebook:
```bash
jupyter notebook
```

2. No navegador que abrir, navegue até o arquivo `Trabalho_Final.ipynb`

3. Execute as células sequencialmente:
   - Clique em uma célula e pressione `Shift + Enter` para executá-la
   - Ou use o menu `Cell > Run All` para executar todas as células

#### Via JupyterLab

1. Inicie o JupyterLab:
```bash
jupyter lab
```

2. Abra o arquivo `Trabalho_Final.ipynb` no explorador de arquivos

3. Execute as células na ordem, de cima para baixo

#### Via Google Colab

1. Acesse [Google Colab](https://colab.research.google.com/)
2. Faça upload do arquivo `Trabalho_Final.ipynb`
3. Faça upload da pasta "dices"
4. Execute as células sequencialmente

## Etapas do Processamento

O notebook está organizado nas seguintes etapas:

### 1. Importação de Bibliotecas
Carrega todas as dependências necessárias para o processamento de imagens.

### 2. Definição do Diretório
Configura o caminho para a pasta contendo as imagens dos dados.

### 3. Função de Visualização
Implementa uma função `exibe_grade()` que organiza múltiplas imagens em uma grade para comparação visual.

### 4. Conversão para Escala de Cinza
- Remove o canal alpha (transparência) se presente
- Converte imagens RGB para escala de cinza
- Exibe as imagens convertidas

### 5. Suavização
- Aplica filtro Gaussiano com sigma=1.5
- Reduz ruídos e prepara para detecção de bordas
- Visualiza o resultado da suavização

### 6. Detecção de Bordas
- Aplica o filtro de Sobel
- Identifica e realça as bordas dos dados
- Apresenta as imagens com bordas detectadas

## Resultados Esperados

Após executar todas as células, você verá:

1. **Imagens Originais**: Dataset completo de dados em cores
2. **Imagens em Cinza**: Mesmas imagens convertidas para escala de cinza
3. **Imagens Suavizadas**: Resultado após aplicação do filtro Gaussiano
4. **Bordas Detectadas**: Contornos dos dados realçados pelo filtro de Sobel

Cada etapa é apresentada em uma grade organizada, permitindo comparação visual entre as diferentes transformações.

**Desenvolvido como trabalho final de processamento de imagens**
