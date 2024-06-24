# Projeto de Visão Computacional.

Esse projeto teve como objetivo treinar um modelo que identificasse menores de idade através de técnicas de visão computacional para ajudar os atendentes de uma rede de supermercados a não cometerem o erro de vender bebidas alcoólicas para menores de 18 anos.

Foram utilizadas imagens de faces e um CSV com os rótulos para as imagens. O projeto foi desenvolvido em cloud, utilizando uma VM com o Jupyter. As imagens e rótulos necessários para o treinamento do modelo foram providenciados, e o treinamento foi feito em uma máquina com GPU comunitária oferecida pela Tripleten para seus alunos. Criei uma classificação qualitativa de idoso, adulto e jovem para analisar a distribuição da amostra.

Em seguida, foi feita a transformação dos dados utilizando o ImageDataGenerator da biblioteca Keras. Com ele, é possível fazer todo o pré-processamento dos dados para o treinamento do modelo.

Foi utilizado o modelo Sequential com a arquitetura ResNet50 como pré-treinamento. Foi adicionada uma camada com o GlobalAveragePooling2D, uma camada densa com uma unidade e ReLU como função de ativação. A compilação foi feita com o otimizador Adam e MAE (Mean Absolute Error) como função de perda. O resultado foi um modelo com a taxa de erro de **6.6036 MAE.**