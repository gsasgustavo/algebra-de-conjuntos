
var:
> **Conjunto:**
    _vetor de inteiros_
    A: `vetor[2,3,5,6,8]` de inteiros
    B: `vetor[6,8]` de inteiros
    temp: `Uniao(A,B)` inteiros

    1. início
    2. função AdicionarElemento (conjunto[], elemento: inteiro): vetor de inteiro
    3.     se o tamanho do conjunto igual 0 então
    4.         conjunto na primeira posição recebe elemento.
    5.         retorne o conjunto
    6.     senão
    7.         vetor de inteiro a recebe tamanho do conjunto + 1
    8.         para i igual a 0 até i menor que tamanho de a faça
    9.             se i menor que tamanho do conjunto então
    10.                 a[i] recebe conjunto[i]
    11.             senão
    12.                 a[i] recebe elemento
    13.             fimse
    14.         fimpara
    15.         retorne a
    16.     fimse
    17. fim
    18. 
    19. inicio
    20. função RemoverElemento (conjunto[], elemento: inteiro): vetor de inteiro
    21.     vetor de inteiro a recebe tamanho conjunto - 1
    22.     lógico passou recebe false
    23.     para i igual a 0 até i menor que tamanho de a faça
    24.         se conjunto[i] diferente do elemento então
    25.             se passou diferente de falso então
    26.                 a[i] recebe conjunto[i]
    27.             senão
    28.                 a[i] recebe conjunto[i+1]
    29.             fimse
    30.         senão
    31.             a[i] recebe conjunto[i+1]
    32.             passou recebe true
    33.         fimse
    34.     fimpara
    35.     retorne a
    36. fim
    37. 
    38. inicio
    39. função Pertinencia (conjunto[],elemento: inteiro): lógico
    40.     para i igual a 0 até i menor que tamanho conjunto faça
    41.         se conjunto[i] igual elemento então
    42.             retorne verdadeiro
    43.         fimse
    44.     fimpara
    45.     retorne falso
    46. fim
	47.
    48. início
    49. função Continencia (conjuntoA,conjuntoB: vetor de inteiro): lógico
    50.     inteiro cont recebe 0
    51.     se tamanho do conjuntoA menor i tamanho do conjuntoB então
    52.         para i igual a 0 até i menor que tamanho conjuntoA faça
    53.             para j igual a 0 até j menor que tamanho conjuntoB faça
    54.                 se conjuntoB[j] igual a conjuntoA[i] então
    55.                     incrementa cont
    56.                 fimse
    57.             fimpara
    58.         fimpara
    59.     fimse
    60.     se cont igual a tamanho do conjuntoA então
    61.         retorne verdadeiro
    62.     senão
    63.         retorne falso
    64.     fimse
    65. fim
	66.
    67. início
    68. função Disjuncao (conjuntoA,conjuntoB: vetor de inteiro): lógico
    69.     inteiro cont recebe 0
    70.     se tamanho do conjuntoA menor ou igual a tamanho do conjuntoB então
    71.         para i igual a 0 até i menor que tamanho do conjuntoA faça
    72.             para j igual a 0 até j menor que tamanho do conjuntoB faça
    73.                 se conjuntoB[j] igual a conjuntoA[i] então
    74.                     incrementa cont
    75.                 fimse
    76.             fimpara
    77.         fimpara
    78.     fimse
    79.     se cont igual a 0 então
    80.         retorne verdadeiro
    81.     senão
    82.         retorne falso
    83.     fimse
    84. fim
	85.
    86. início
    87. função UniaoDisjunta (conjuntoA,conjuntoB: classe UniaoDisjunta): lista de caracter
    88.     c: lista de caracter
    89.     para i igual a 0 até i menor que tamanho do atributo Conjunto do conjuntoA faça
    90.         adiciona em c conjuntoA.Conjunto[i] + atributo nomeConjunto do conjuntoA
    91.     fimpara
    92.     para i igual a 0 até tamanho do atributo Conjunto do conjuntoB faça
    93.         adiciona em c conjuntoB.Conjunto[i] + atributo nomeConjunto do conjuntoB
    94.     fimpara
    95.     retorne c
    96. fim
	97.
    98. início
    99. função Uniao (conjuntoA,conjuntoB: vetor de inteiro): lista de inteiro
    100.     a: lista inteiro  
    101.     para i igual a 0 até i menor que tamanho do conjuntoA faça
    102.         adiciona em a conjuntoA[i]
    103.     fimpara
    104.     lógico temp recebe falso
    105.     para i igual a 0 até i menor que tamanho do conjuntoB faça
    106.         para j igual a 0 até j menor que contador de a faça
    107.             se conjuntoB[i] igual a a[j] então
    108.                 temp recebe verdadeiro
    109.                 pausa
    110.             fimse
    111.         fimpara
    112.         se diferença de temp então
    113.             adiciona em a conjuntoB[i]
    114.         fimse
    115.     fimpara
    116.     retorne a
    117. fim
	118.
    119. início
    120. função Diferenca (A,B: vetor de inteiro): lista de inteiro
    121.     listaTemp: lista inteiro
    122.     para i igual a 0 até i menor que tamanho de B faça
    123.         lógico temp recebe falso
    124.         para j igual a 0 até j menor que tamanho de A faça
    125.             se A[j] igual a B[i] então
    126.                 temp recebe verdadeiro
    127.             fimse
    128.         fimpara
    129.         se diferença temp então
    130.             adiciona em listaTemp B[i]
    131.         fimse
    132.     fimpara
    133.     para i igual a 0 até i menor que tamanho de A faça
    134.         lógico temp recebe falso
    135.         para j igual a 0 até j menor que tamanho de B faça
    136.             se A[i] igual a B[j] então
    137.                 temp recebe verdadeiro
    138.             fimse
    139.         fimpara
    140.         se diferença temp então
    141.             adiciona na listaTemp A[i]
    142.         fimse
    143.     fimpara
    144.     retorne listaTemp  
    145. fim  
	146.
    147. início  
    148. função ConjuntoDasPartes (A: vetor de inteiro): lista de vetor de inteiro  
    149.     listaTemp: lista de vetor de inteiro    
    150.     para i igual a 0 até i menor que tamanho de A faça  
    151.         adiciona na listaTemp A[i]  
    152.     fimpara  
    153.     para i igual a 0 até i menor que tamanho de A faça  
    154.         para j recebe tamanho A - 1 até j maior ou igual a 0 faça  
    155.             se A[i] diferente A[j] então  
    156.                 adiciona na listaTemp A[i], A[j]  
    157.             fimse  
    158.         fimpara  
    159.     fimpara  
    160.     retorne listaTemp  
    161. fim  
	162.
    163. início  
    164. função Complemento (A, B: vetor de inteiro): lista inteiro  
    165.     C: lista inteiro    
    166.     para i igual a 0 até i menor que tamanho de A faça  
    167.         adiciona em C A[i]  
    168.     fimpara  
    169.     lógico temp recebe falso  
    170.     para i igual a 0 até i menor que tamanho de B faça  
    171.         para j igual a 0 até j menor que contador C faça  
    172.             se B[i] igual a C[j] então  
    173.                 remove de C j  
    174.                 pausa  
    175.             senão  
    176.                 temp recebe verdadeiro  
    177.             fimse  
    178.         fimpara  
    179.         se diferença temp então  
    180.             adiciona em C B[i]  
    181.         fimse  
    182.     fimpara  
    183.     retorne C  
    184. fim
	185.
    186. início  
    187. classe UniaoDisjunta  
    188.     NomeConjunto: caracter  
    189.     Conjunto: vetor de inteiro  
    190.     construtor UniaoDisjunta (nomeConjunto: caracter, conjunto: vetor de inteiro)  
    191.         NomeConjunto recebe nomeConjunto  
    192.         Conjunto recebe conjunto  
    193. fim
	194.
