# Algoritmo de Karatsuba

Implementação em Java do algoritmo de Karatsuba para multiplicação eficiente de números grandes.

## 📖 Sobre

Este projeto implementa o **Algoritmo de Karatsuba**, um método de multiplicação rápida que usa a técnica de divisão e conquista. Desenvolvido por Anatoly Karatsuba em 1960, este algoritmo reduz a complexidade da multiplicação de números grandes de O(n²) para aproximadamente O(n^1.585).

## 🚀 Como Usar

### Pré-requisitos

- Java JDK instalado (versão 8 ou superior)

### Compilação

```bash
javac App.java
```

### Execução

```bash
java App "numero1" "numero2"
```

### Exemplo

```bash
java App "12432134341245674745675476" "7054920058988836008343024"
```

O programa irá calcular e exibir o resultado da multiplicação dos dois números fornecidos.

## 🔧 Funcionamento

O algoritmo divide os números em partes menores e realiza multiplicações recursivas, reduzindo o número total de operações necessárias.

### Principais Componentes

- **karatsuba()**: Implementação principal do algoritmo recursivo
- **soma()**: Realiza a adição de dois números grandes representados como strings
- **sub()**: Realiza a subtração de dois números grandes
- **shift()**: Desloca um número multiplicando-o por potências de 10
- **zeros()**: Normaliza os números adicionando zeros à esquerda quando necessário
- **tiraZeros()**: Remove zeros à esquerda do resultado final

## 📊 Complexidade

- **Tradicional**: O(n²)
- **Karatsuba**: O(n^log₂3) ≈ O(n^1.585)

Essa melhoria é especialmente significativa ao trabalhar com números muito grandes.

## 💡 Exemplo de Uso

```bash
# Multiplicação de números grandes
java App "12432134341245674745675476" "7054920058988836008343024"

# O programa aceita exatamente 2 argumentos
# Se não forem fornecidos 2 números, o programa será encerrado
```

## ⚙️ Detalhes Técnicos

- Linguagem: Java
- Método: Divisão e Conquista
- Representa números como Strings para suportar valores maiores que os tipos primitivos do Java
- Implementação iterativa das operações de soma e subtração para evitar overflow
