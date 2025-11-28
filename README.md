# FIAP - Faculdade de Informática e Administração Paulista

![Logo FIAP](./assets/logo-fiap.png)

# Da Terra ao Código: Automatizando a Classificação de Grãos com Machine Learning

## Nome do grupo

## Integrantes:

* Ricardo Rodriguez Frugoni de Souza

## Professores:

### Coordenador(a)

* [Nome do Coordenador]

## Descrição

Em cooperativas agrícolas de pequeno porte, a classificação dos grãos é realizada manualmente por especialistas, o que pode ser demorado e sujeito a erros humanos. Com o avanço do aprendizado de máquina, é possível automatizar esse processo, aumentando a eficiência e a precisão da classificação.

O objetivo deste projeto é aplicar a metodologia CRISP-DM para desenvolver um modelo de aprendizado de máquina que classifique variedades de grãos de trigo com base em suas características físicas. Para isso, foram realizadas as seguintes etapas:

1. Análise e pré-processamento dos dados fornecidos
2. Implementação e comparação de diferentes algoritmos de classificação
3. Otimização dos modelos para melhorar o desempenho
4. Interpretação dos resultados e extração de insights relevantes

O projeto utiliza o "Seeds Dataset" disponível no UCI Machine Learning Repository, que contém medições de 210 amostras de grãos de trigo pertencentes a três variedades diferentes: Kama, Rosa e Canadian.

Foram implementados e comparados cinco algoritmos de classificação: K-Nearest Neighbors (KNN), Support Vector Machine (SVM), Random Forest, Naive Bayes e Logistic Regression. Todos os modelos foram otimizados utilizando Grid Search com validação cruzada, e o Random Forest otimizado apresentou o melhor desempenho geral, sendo recomendado para implantação em produção.

A solução pode ser implementada em cooperativas agrícolas para automatizar a classificação, reduzindo tempo e custos operacionais, além de aumentar a precisão e consistência do processo.

## Estrutura de pastas

Dentre os arquivos e pastas presentes na raiz do projeto, definem-se:

* **assets**: aqui estão os arquivos relacionados a elementos não-estruturados deste repositório, como imagens, diagramas e recursos visuais do projeto.
* **data**: Pasta contendo os dados do projeto:
  * **seeds_dataset.txt**: Dataset original do UCI Machine Learning Repository com 210 amostras de grãos de trigo
* **classificacao_graos_trigo.ipynb**: Notebook Jupyter principal com todo o desenvolvimento do projeto, incluindo análise exploratória, pré-processamento, modelagem, otimização e interpretação de resultados
* **README.md**: arquivo que serve como guia e explicação geral sobre o projeto (o mesmo que você está lendo agora).

## Como executar o código

### Pré-requisitos

* Python 3.7+ ([Download](https://python.org))
* Git ([Download](https://git-scm.com))
* IDE recomendada: Jupyter Notebook ou Google Colab

### Instalação

#### 1. Clonar o repositório

```bash
git clone [url-do-repositorio]
cd Cap3-ir-alem
```

#### 2. Configurar ambiente virtual Python

```bash
# Criar ambiente virtual
python -m venv venv

# Ativar ambiente virtual
# Windows:
venv\Scripts\activate
# Linux/Mac:
source venv/bin/activate
```

#### 3. Instalar dependências Python

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

### Execução

#### Opção 1: Jupyter Notebook (Local)

1. Iniciar o Jupyter Notebook:
```bash
jupyter notebook
```

2. Abrir o arquivo `classificacao_graos_trigo.ipynb`
3. Executar todas as células sequencialmente
4. Os resultados serão exibidos automaticamente

#### Opção 2: Google Colab (Nuvem)

1. Acessar o Google Colab: https://colab.research.google.com/
2. Fazer upload do arquivo `classificacao_graos_trigo.ipynb`
3. Fazer upload da pasta `data/` com o dataset
4. Executar todas as células sequencialmente

## Licença

MODELO GIT FIAP por Fiap está licenciado sobre Attribution 4.0 International.

## Tecnologias Utilizadas

### Análise de Dados e Machine Learning
* Python 3.7+
* Pandas 2.x
* NumPy 1.x
* Matplotlib 3.x
* Seaborn 0.12+
* Scikit-learn 1.x

### Ferramentas de Desenvolvimento
* Jupyter Notebook 7.x
* Git
* Visual Studio Code

## Resultados e Métricas

### Performance dos Modelos

Foram implementados e otimizados 5 algoritmos de classificação:

1. **K-Nearest Neighbors (KNN)**
2. **Support Vector Machine (SVM)**
3. **Random Forest**
4. **Naive Bayes**
5. **Logistic Regression**

### Modelo Selecionado

**Random Forest Otimizado** apresentou o melhor desempenho geral:
* Acurácia superior a 90%
* Excelente desempenho em todas as métricas (Precisão, Recall, F1-Score)
* Alta confiabilidade para classificação das três variedades de grãos

### Métricas de Avaliação

Todos os modelos foram avaliados utilizando:
* Acurácia (Accuracy)
* Precisão (Precision)
* Recall
* F1-Score
* Matriz de Confusão

### Características Mais Importantes

Análise de importância de features revelou que:
* **Área** do grão
* **Perímetro** do grão
* **Comprimento do Núcleo**

São as características mais discriminativas para classificação das variedades.

## Metodologia CRISP-DM

O projeto foi desenvolvido seguindo as etapas da metodologia CRISP-DM:

1. **Entendimento do Negócio**: Definição do problema e objetivos
2. **Entendimento dos Dados**: Análise exploratória e estatística descritiva
3. **Preparação dos Dados**: Tratamento de valores ausentes, normalização e divisão em treino/teste
4. **Modelagem**: Implementação e comparação de algoritmos de classificação
5. **Avaliação**: Otimização de hiperparâmetros e análise de desempenho
6. **Implantação**: Interpretação de resultados e recomendações

## Dataset

### Descrição

O **Seeds Dataset** contém medições de 210 amostras de grãos de trigo pertencentes a três variedades diferentes:

* **Kama** (Variedade 1)
* **Rosa** (Variedade 2)
* **Canadian** (Variedade 3)

### Atributos

1. **Área**: Medida da área do grão
2. **Perímetro**: Comprimento do contorno do grão
3. **Compacidade**: Calculada como (4π × área) / perímetro²
4. **Comprimento do Núcleo**: Comprimento do eixo principal da elipse equivalente ao grão
5. **Largura do Núcleo**: Comprimento do eixo secundário da elipse
6. **Coeficiente de Assimetria**: Medida da assimetria do grão
7. **Comprimento do Sulco do Núcleo**: Comprimento do sulco central do grão

### Fonte

* **Repositório**: UCI Machine Learning Repository
* **Link**: https://archive.ics.uci.edu/dataset/236/seeds

## Insights e Conclusões

### Principais Descobertas

1. **Desempenho dos Modelos**: Todos os modelos apresentaram excelente desempenho, com acurácias superiores a 90%. A otimização de hiperparâmetros trouxe melhorias significativas para a maioria dos modelos.

2. **Características Discriminativas**: As características físicas dos grãos são altamente discriminativas. O tamanho e formato dos grãos são os principais fatores de diferenciação entre as variedades.

3. **Aplicabilidade Prática**: O modelo pode ser implementado em cooperativas agrícolas para automatizar a classificação, garantindo alta confiabilidade e reduzindo tempo e custos operacionais.

### Limitações e Considerações

* O dataset é relativamente pequeno (210 amostras)
* Seria benéfico coletar mais dados para aumentar a robustez do modelo
* Validação em condições reais de campo seria necessária antes da implantação completa

### Próximos Passos

* Coleta de mais dados para aumentar a robustez do modelo
* Validação em condições reais de campo
* Desenvolvimento de interface para uso prático
* Monitoramento contínuo do desempenho do modelo

## Contato

Para dúvidas ou sugestões sobre o projeto, entre em contato através dos canais oficiais da FIAP ou abra uma issue no repositório do projeto.
