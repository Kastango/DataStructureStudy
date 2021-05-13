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

**Lista Estática**
```C```

**Lista Dinâmica Simplesmente Encadeada**
```C
typedef struct node{
  struct node *next;
  void *data;
} node_t;

struct dynamic_list{
  int qtd;
  int size;
  node_t *head;
  node_t *tail;
};
```

**Fila Estática**
```C```

**Fila Simplesmente Encadeada**
```C
typedef struct node{
  struct node *next;
  void *data;
} node_t;

struct dynamic_list{
  int qtd;
  int size;
  node_t *head;
};

```


### 6. Ilustre o estado das tabelas de espalhamento (hash) abaixo após a inserção dos valores: 1, 4, 20, 13, 12, 10, 7, 33, 40, 15, 14, 30:
  * Tabela hash com 10 posições e colisão resolvida por encadeamento e função de hash h(k) = k%10
 
  | 0  | 1  |  2 |  3 |  4 |  5 |  6 |  7 |  8 |  9 |
  |----|----|----|----|----|----|----|----|----|----|
  |[20]| [1]|[12]|[13]|[4] |[15]|    |[7] |    |    |
  |[10]|    |    |[33]|[14]|    |    |    |    |    |
  |[40]|    |    |[33]|    |    |    |    |    |    |
  |[30]|    |    |    |    |    |    |    |    |    |

  * Tabela hash com 20 posições e colisão resolvida por sondagem linear e função de hash base g(k) = k%20
  * Tabela hash com 20 posições e colisão resolvida por sondagem quadrática e função de hash base g(k) = k%20
### 7. Explique os três tipos se sondagem para tabelas de espalhamento (hash).
 * **Linear** g(k, i) = (h(k) + i) % m
   * Nessa sondagem apos a primeira tentativa soma-se 1 no índice para a seguinte 
   * Primeiro tentamos T[h(k)], depois T[h(k) + 1], T[h(k) + 2], ...
   * É facil de implementar entretando gera clusters(longas sequencias ocupadas)
 * **Quadrática** g(k, i) = (h(k) + c₁i + c₂i²) % m
   * Depois da primeira tentativa os proximos valores dependem do número de sondagens que ocorreram
 * **Hash Duplo** g(k, i) = (h₁(k) + ih₂(k)) % m
   * Depois da primeira tentativa ele faz uso de outra função de hash para gerar a posição, os valores h₂ e m devem ser primos entre sí

### 8. Explique o algoritmo de heapsort, mergesort e quicksort.
 **Heapsort**
 
 
 ![image](https://lamfo-unb.github.io/img/Sorting-algorithms/Sorting_heapsort_anim.gif)
 
 **Mergesort** é um algorítmo de divisão e Conquista, ou seja, ele divide o problema em subproblemas e quando todas as pequenas partes tiverem sido solucionadas, o resultado é unido para dar a resposta do probleme inicial. Ou seja, primeramente o algorítmo irá dividir o Array na metade, em dois subarrays. Nesses dois subarrays há uma tentativa de ordenação, caso ainda não estejam em ordem, serão divididos novamentes e haverá uma nova tentativa de ordena-los. Quando o Algorítimo alcançar o caso ordenado, os subarrays são novamente combinados
 
  ![image](https://i.ibb.co/PW34M2v/merge-sort-gif-9.gif)
 
 **QuickSort** é um dos algorítimos de orneção mais eficientes de Divide and Conquer. Ele funciona selecionando um número pivo, que irá separar os números menores que ele à sua esquerda e os maiores a direita. Após essa partição, o pivot está em sua posição final. Isso é chamado de operação de partição. através de recursão a etapa é realizada novamente nos subarrays de elementos com valores menores separadamente ao sbuconjunto de velementos com valores maiores. O Seu pior caso tem complexidade de O(n²)
 
 ![image](https://upload.wikimedia.org/wikipedia/commons/6/6a/Sorting_quicksort_anim.gif)


### 9. Explique o que são Pilhas, Listas e Filas.
 Todas as estruturas são tipos de armazenar e relacionar conjuntos de informações de forma organizada e, na maioria das vezes, sequencial.
 **Conceito Pilha**
    * Estrutura de dados lineares que se pode inserir e remover somente em uma mesma extremidade, na qual o último elemento a entrar é o primeiro a sair
    * é uma lista linear em que todas as operações (inserção, retirada e consulta) são realizadas numa única extremidade da estrutura
 **Conceito Fila**
    * Estrutura de dados lineares que se pode inserir somente em uma extremidade e remover somente em uma outra extremidade, na qual o primeiro elemento a entrar é o primeiro a sair
    *  é uma lista linear em que as inserções de novos nodos na estrutura são realizadas em uma das extremidades e as retiradas ou consultas aos nodos são realizadas na outra extremidade da lista.
  **Conceito Lista**
    * Estrutura de dados lineares indexadas que se pode inserir e remover em qualquer posição
    * Lista é uma seqüência ordenada de elementos do mesmo tipo
