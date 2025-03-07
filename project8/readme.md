# PROJETO 8

Objetivo: Tentando reproduzir o material desse link:
https://github.com/lazyprogrammer/machine_learning_examples/blob/master/nlp_class2/tfidf_tsne.py

Nesse meu código estou lidando com um processo de pré-processamento de texto e visualização dos dados, mais especificamente usando técnicas de tokenização, representação vetorial e redução de dimensionalidade para analisar e visualizar texto de maneira mais eficiente. Vou explicar o que cada parte do seu código está fazendo em termos gerais:

1. Tokenização do texto:

A tokenização é o processo de dividir o texto em unidades menores, chamadas tokens (geralmente palavras ou sentenças). Isso é feito por meio da função tokenize_text_handmade e tokenize_text, que:

Divide o texto em sentenças: A função sent_tokenize do NLTK divide o texto em sentenças, ou seja, quebra o texto em blocos de frases.

Divide as sentenças em palavras: Após dividir em sentenças, a função word_tokenize é usada para dividir essas sentenças em palavras.

2. Criação de um vocabulário (Índices para palavras):

Depois de tokenizar o texto, o próximo passo é converter as palavras em índices numéricos para representar cada palavra de forma numérica, o que facilita o processamento computacional. Isso é feito com o dicionário word2idx e idx2word, onde cada palavra recebe um índice único.

3. Conversão de sentenças para índices:

Após criar o vocabulário (mapa de palavras para índices), o código converte cada palavra de cada sentença para o seu respectivo índice usando o mapeamento de word2idx. Isso permite que o texto seja manipulado em formato numérico para facilitar a análise ou o uso em modelos de aprendizado de máquina.

4. Redução de dimensionalidade com T-SNE:

Com as representações numéricas (índices), o código usa o T-SNE (t-Distributed Stochastic Neighbor Embedding), uma técnica de redução de dimensionalidade, para projetar os dados em um espaço 2D. Isso ajuda a visualizar a estrutura dos dados de uma maneira que facilita a identificação de padrões ou relações.

TSNE pega as representações vetoriais e as projeta em duas dimensões (ou mais, dependendo da configuração) para que você possa ver os dados em um gráfico 2D.

O código cria uma dispersão (scatter plot) no gráfico para mostrar onde cada palavra (representada por seu índice) está posicionada no espaço 2D resultante.

5. Anotações no gráfico:

No gráfico gerado pelo T-SNE, o código tenta anotar as palavras nos pontos correspondentes para que você possa ver quais palavras estão associadas a cada ponto no gráfico.

O código anota as palavras, mas limita o número de anotações para evitar sobrecarregar o gráfico.

Ele também remove palavras de pontuação, pois essas não são relevantes para o entendimento do texto.

6. Visualização:

O código usa a função plt.scatter para criar um gráfico de dispersão, onde os pontos representam as palavras em um espaço 2D. Ele também ajusta a aparência do gráfico para melhorar a legibilidade (como ajustando o tamanho da figura, a transparência dos pontos, o tamanho das fontes das anotações, etc.).

### Resumo do fluxo:

Tokenização: O texto é dividido em sentenças e palavras.

Conversão em índices: As palavras são mapeadas para índices numéricos.

T-SNE: A redução de dimensionalidade é realizada para projetar as palavras em um gráfico 2D.

Anotação: Algumas palavras são anotadas no gráfico para indicar onde elas se situam no espaço 2D.

Visualização: O gráfico de dispersão é gerado e ajustado para facilitar a visualização.


### Objetivo do código:

O objetivo do seu código é analisar a estrutura semântica de um corpus de texto, representando palavras em um espaço vetorial de alta dimensão, e em seguida, projetando essas palavras em um espaço 2D para entender como elas se agrupam ou se relacionam. Isso é útil para tarefas como:

Análise semântica (entender como as palavras se agrupam em um espaço semântico).

Visualização de dados textuais.

Exploração de padrões em dados de texto.
