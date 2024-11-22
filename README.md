Descrição do Projeto:
Este projeto simula a propagação de uma doença em uma grade (lattice) bidimensional usando um modelo simples de infecção e recuperação. Além disso, o projeto realiza a otimização da razão entre a probabilidade de infecção e a probabilidade de recuperação, com o objetivo de identificar as condições em que a doença ainda se propaga para mais de 5000 células.

Funcionalidades:
Simulação de Propagação: O código simula a propagação de uma doença em uma grade quadrada, onde uma célula pode estar:

Saudável (0).
Infectada (1).
Recuperada (2).

A infecção ocorre nas células vizinhas de uma célula infectada com uma probabilidade definida. As células infectadas podem se recuperar após um número de dias, com uma probabilidade de recuperação.

Parâmetros da Simulação:

lado: Tamanho da grade (100x100 no exemplo).
dias: Duração da simulação em dias.
prob_infeccao: Probabilidade de uma célula saudável se infectar ao ter contato com uma célula infectada.
prob_recuperacao: Probabilidade de uma célula infectada se recuperar.
num_simulacoes: Número de simulações independentes para analisar a propagação.
Otimização das Probabilidades:

A função de otimização busca a razão mínima entre probabilidade de infecção e probabilidade de recuperação em que a doença ainda se propaga para mais de 5000 células.
A otimização é feita usando o método L-BFGS-B da biblioteca SciPy, que encontra os valores ótimos das probabilidades de infecção e recuperação.
Resultado da Otimização:

O projeto retorna a menor razão infecção/recuperação que permite a propagação da doença.
As probabilidades otimizadas de infecção e recuperação são impressas.

Tecnologias Utilizadas:
NumPy: Para cálculos e manipulação de arrays.
SciPy: Para otimização numérica.
Randomização: A simulação usa números aleatórios para determinar a propagação de infecção e recuperação das células.


Como o Código Funciona:
Simulação da Doença:

A doença começa no centro da grade e se propaga de acordo com as probabilidades definidas para infecção e recuperação.
Cada célula infectada tem 4 vizinhos (cima, baixo, esquerda, direita) e pode infectá-los com base em uma probabilidade.
As células infectadas podem se recuperar com uma determinada probabilidade, passando para o estado recuperado.

Otimização:

A função objetivo define uma métrica de desempenho com base na razão entre as probabilidades de infecção e recuperação.
A função minimize da biblioteca SciPy é usada para encontrar os valores de probabilidade que otimizam essa razão.


Resultados Esperados:
A otimização retornará uma razão mínima de infecção/recuperação onde a doença ainda se propaga significativamente.
Com isso, podemos entender como diferentes níveis de infecção e recuperação afetam a propagação da doença em um sistema discreto.

Exemplos de Saída:

A menor razão probabilidade de infecção / probabilidade de recuperação onde a doença ainda se propaga para mais de 5000 células é:

![image](https://github.com/user-attachments/assets/9be40868-c27e-4ba5-a0e8-35e85d06bc34)


