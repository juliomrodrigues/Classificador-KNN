# Classificador-KNN
### Descrição
Treinando um modelo de classificação a e aplicando em uma base de dados para classificar registros(Censo de 1994 - EUA).

O objetivo é prever se uma pessoa possui renda anual <= ou > 50 mil dólares por ano.

**Percentual Mínimo** -> Base Line Classifier = 0.7559 (ZeroR).

### Resultados - Validação Cruzada - StratifiedKFold
**Precisão** | **Pré-Processamentos** | **Desvio Padrão**
| :------: | :------: | :------: |
0.7778 | LabelEncoder | 0.0079
0.7764 | OneHotEncoder | 0.0075
**0.8281** | **LabelEncoder + StandardScaler** | **0.0075**
0.8238 | OneHotEncoder + StandardScaler | 0.0061
0.8238 | LabelEnconder + OneHotEncoder + StandardScaler | 0.0061

### Matriz de Confusão(Média de todas as 10 execuções):
### Matriz de Confusão (Média):
x | **0** | **1**
| :------: | :------: | :------: |
0 | **2236.9** | 235.1
1 | 324.6 | **459.5**

A Matriz na tabela acima é formada pela média de todas as matrizes geradas ao longo de 10 execuções usando pré-processamentos LabelEncoder + StandardScaler .

A diagonal principal (em negrito) destaca os registros classificados corretamente.

### Bibliotecas usadas:
- Pandas
- Sklearn
- Numpy

### Técnicas de Pré-Processamento e Tratamento dos dados usada:
- LabelEnconder;
- OneHotEncoder;
- StandardScaler;

### Ferramentas Usadas:
- Anaconda
- Spyder

### Linguagem:
- Python

### Fonte da Base de Dados: 
- Dua, D. and Graff, C. (2019). UCI Machine Learning Repository [http://archive.ics.uci.edu/ml]. Irvine, CA: University of California, School of Information and Computer Science.

### Como usar:
1. Faça o download do classificador já treinado dispoível neste mesmo repositório [aqui](https://github.com/juliomrodrigues/Classificador-KNN/blob/main/classificador_knn.sav).
2. Abra o arquivo.py que deseja usar o classificador ou então crie um novo.
3. Execute o código abaixo para fazer a importação:
~~~~python
import pickle
classificador_knn = pickle.load(open('classificador_knn.sav', 'rb'))
~~~~~
4. Pronto, agora o classficador está pronto para ser usado.

#### Outros Classificadores:
- [Naive Bayes](https://github.com/juliomrodrigues/Classificador-Naive-Bayes)
- [Árvore de Decisão](https://github.com/juliomrodrigues/Arvore-de-Decisao)
- [Random Forest](https://github.com/juliomrodrigues/Random-Forest-Classificador)
- [Regras](https://github.com/juliomrodrigues/Classificador-Regras)
- [Regressão Logística](https://github.com/juliomrodrigues/Regressao-Logistica-Classificador)
- [SVM](https://github.com/juliomrodrigues/Classificador-SVM)
- [Rede Neural](https://github.com/juliomrodrigues/Classificador-Rede-Neural)
