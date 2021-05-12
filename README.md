# Revisão
### 1. Qual a complexidade de tempo para inserção e remoção no pior caso, melhor caso e caso médio para as seguintes estruturas lineares: Pilha estática, Lista estática, Lista simplesmente encadeada e Lista duplamente encadeada
|              | inserção pior caso  | remocação pior caso | inserção melhor caso | remoção melhor caso | inserção caso médio | remoção caso medio | *pesquisa caso médio* | 
|--------------|---------------------|---------------------|----------------------|---------------------|---------------------|--------------------|-----------------------|
|Pilha Estática|   Θ(1)              |   Θ(1)              |   Θ(1)               |   Θ(1)              |   Θ(1)              |   Θ(1)             |   Θ(N)                |
|Lista Estática|   Θ(N)              |   Θ(N)              |   Θ(1)               |   Θ(1)              |   Θ(N)              |   Θ(N)             |   Θ(N)                |
|Lista Simplesmente Encadeada| Θ(N)  |   Θ(N)              |   Θ(1)               |   Θ(1)              |   Θ(N)              |   Θ(N)             |   Θ(N)                |
|Lista duplamente Encadeada| Θ(1)    |   Θ(1)              |   Θ(1)               |   Θ(1)              |   Θ(N)              |   Θ(N)             |   Θ(N)                |

### 2. Qual a complexidade de tempo no pior caso, melhor caso e caso médio para os seguintes algoritmos de ordenação: Heapsort, Mergesort, Quicksort, Insertsort, Selectionsort, Bubblesort
|              | Heapsort  | Mergesort | Quicksort | Insertsort | Selectionsort | Bubblesort |
|--------------|-----------|-----------|-----------|------------|---------------|------------|
|Melhor Caso   |Ω(n log(n))|Ω(n log(n))|Ω(n log(n))|Ω(n)        | Ω(n^2)        | Ω(n)       |
|Caso Medio    |Θ(n log(n))|Θ(n log(n))|Θ(n log(n))|Θ(n^2)      |    Θ(n^2)     | Θ(n^2)     |
|Pior caso     |O(n log(n))|O(n log(n))|O(n^2)     |O(n^2)      |O(n^2)         | O(n^2)     |
### 3. Defina: Árvore, Árvore binária, Árvore n-ária, Grau de uma árvore, nó raiz, nó folha
 **Árvores** são estruturas de dados não lineares e hierarquicas, tendo seus elementos "acima" ou "abaixo" de outros elementos da árvore nomeados "nós" (que possuem um campo de identificação e um de dados). 
 
 **Árvores Binárias** todos os graus da árvore são limitados a 2: Para todo nó n, grau(n) em {0, 1, 2}.
 
 **Árvore n-ária** árvores nas quais todos os nodos internos obrigatoriamente tem "n" filhos
 
 **Grau de uma árvore** é quantidade de filhos de um nó (subárvores)
 
 **Nó Raiz** É aquele que não possui pai, é o primeiro nó. Raiz possui nível 1, soma-se um cada vez que descer para um filho.
 
 **Nó Folha** Um nó de Grau zero é denominado nó folha.
 
 
### 4. Considere uma árvore binária de busca não balenciada, após a inserção dos seguintes valores nesta ordem: 10, 15, 5, 13, 20, 4, 8, 2, 14; qual o resultado (ordem de processamento) dos percursos: pré-ordem, em-ordem e pós-ordem?
[![image](https://user-images.githubusercontent.com/21091242/118016450-c7ae8100-b32b-11eb-9fa0-880b2465fd06.png)](https://visualgo.net/en/bst?slide=1)
**Pre-Order:** Começa da Raiz indo para esquerda primeiro e depois para a direita ``` 10, 5, 4, 2, 8, 15, 13, 14, 20 ```

**Post-Order:** Começa do Primeiro Node mais a esquerda ```2, 4, 8, 5, 14, 13, 20, 15, 10```

**In-Order:** É na Ordem
``` 2, 4, 5, 8, 10, 13, 14, 15, 20 ```

### 5. Descreva as struct dos descritores e dos nó (quando for o caso) para a implementação das seguintes estruturas de dados: lista estática, lista dinâmica simplesmente encadeada, fila estática, fila simplesmente encadeada. As estrutura devem ser tais que inserções e remoções nas extremidades (início e fim), quando for o caso, são realizadas em O(1).
### 6. Ilustre o estado das tabelas de espalhamento (hash) abaixo após a inserção dos valores: 1, 4, 20, 13, 12, 10, 7, 33, 40, 15, 14, 30:
  * Tabela hash com 10 posições e colisão resolvida por encadeamento e função de hash h(k) = k%10
  * Tabela hash com 20 posições e colisão resolvida por sondagem linear e função de hash base g(k) = k%20
  * Tabela hash com 20 posições e colisão resolvida por sondagem quadrática e função de hash base g(k) = k%20
### 7. Explique os três tipos se sondagem para tabelas de espalhamento (hash).
### 8. Explique o algoritmo de heapsort, mergesort e quicksort.
### 9. Explique o que são Pilhas, Listas e Filas.
