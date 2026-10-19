# Dicionário de Python

Dicionário com os comandos, estruturas, operadores e funções vistos nas aulas, com a descrição de cada um e exemplos testados.

## 1. Entrada e saída de dados

### `print()`
Mostra uma mensagem ou um valor na tela.

```python
print("Olá, mundo!")
print("Python", "é legal")
```

Saída:
```text
Olá, mundo!
Python é legal
```

### `input()`
Permite que a pessoa digite uma informação. O que é digitado fica como texto.

```python
nome = input("Digite seu nome: ")
print("Olá,", nome)
```

Exemplo de saída:
```text
Digite seu nome: Ana
Olá, Ana
```

## 2. Variáveis e tipos de dados

### Variáveis
Servem para guardar valores e usar depois no programa.

```python
nome = "Carlos"
idade = 16
altura = 1.75
print(nome, idade, altura)
```

Saída:
```text
Carlos 16 1.75
```

### Tipos de dados
Os tipos mais comuns são:

| Tipo | Para que serve | Exemplo |
|---|---|---|
| `int` | Número inteiro | `10` |
| `float` | Número com casas decimais | `3.14` |
| `str` | Texto | `"Python"` |
| `bool` | Verdadeiro ou falso | `True` |

### `type()`
Mostra o tipo de um valor.

```python
print(type(10))
print(type(3.14))
print(type("texto"))
print(type(True))
```

Saída:
```text
<class 'int'>
<class 'float'>
<class 'str'>
<class 'bool'>
```

### Conversão de tipos: `int()`, `float()`, `str()` e `bool()`
Essas funções ajudam a converter valores de um tipo para outro.

```python
numero = int("42")
print(numero + 8)

preco = float("3.5")
print(preco)

print(str(100) + " reais")
print(bool(1))
```

Saída:
```text
50
3.5
100 reais
True
```

## 3. Operadores

### Operadores aritméticos
São usados para fazer contas.

| Operador | O que faz | Exemplo |
|---|---|---|
| `+` | Soma | `7 + 2` resulta em `9` |
| `-` | Subtração | `7 - 2` resulta em `5` |
| `*` | Multiplicação | `7 * 2` resulta em `14` |
| `/` | Divisão | `7 / 2` resulta em `3.5` |
| `//` | Divisão inteira | `7 // 2` resulta em `3` |
| `%` | Resto da divisão | `7 % 2` resulta em `1` |
| `**` | Potência | `7 ** 2` resulta em `49` |

```python
a = 7
b = 2
print(a + b)
print(a / b)
print(a % b)
```

Saída:
```text
9
3.5
1
```

### Operadores relacionais
Comparam valores e retornam `True` ou `False`.

| Operador | Significado |
|---|---|
| `==` | Igual |
| `!=` | Diferente |
| `>` | Maior |
| `<` | Menor |
| `>=` | Maior ou igual |
| `<=` | Menor ou igual |

```python
x = 10
y = 5
print(x == y)
print(x != y)
print(x > y)
```

Saída:
```text
False
True
True
```

### Operadores lógicos
Servem para combinar condições. `and` exige que as duas sejam verdadeiras; `or` aceita pelo menos uma verdadeira; `not` inverte o resultado.

```python
idade = 20
tem_cnh = True
print(idade >= 18 and tem_cnh)
print(idade < 18 or tem_cnh)
print(not tem_cnh)
```

Saída:
```text
True
True
False
```

### Operadores de atribuição
O `=` guarda um valor. Os operadores como `+=` e `*=` atualizam o valor da variável.

```python
x = 10
x += 5
print(x)

x *= 2
print(x)
```

Saída:
```text
15
30
```

Outros exemplos são `-=`, `/=`, `//=`, `%=` e `**=`.

### Operadores de pertencimento: `in` e `not in`
Verificam se um item está ou não em uma lista ou texto.

```python
frutas = ["maçã", "banana", "uva"]
print("banana" in frutas)
print("pera" not in frutas)
```

Saída:
```text
True
True
```

## 4. Estruturas condicionais

### `if`
Executa o código quando a condição é verdadeira.

```python
idade = 18

if idade >= 18:
    print("Maior de idade")
```

Saída:
```text
Maior de idade
```

### `else`
É usado quando a condição do `if` não é verdadeira.

```python
numero = 7

if numero % 2 == 0:
    print("Par")
else:
    print("Ímpar")
```

Saída:
```text
Ímpar
```

### `elif`
Permite verificar outra condição antes de chegar ao `else`.

```python
nota = 7.5

if nota >= 9:
    print("Conceito A")
elif nota >= 7:
    print("Conceito B")
else:
    print("Conceito C")
```

Saída:
```text
Conceito B
```

## 5. Estruturas de repetição

### `range()`
Gera uma sequência de números. O número final não é incluído.

```python
print(list(range(5)))
print(list(range(2, 6)))
print(list(range(0, 10, 2)))
```

Saída:
```text
[0, 1, 2, 3, 4]
[2, 3, 4, 5]
[0, 2, 4, 6, 8]
```

### `for`
Repete o código para cada item de uma sequência.

```python
for i in range(1, 4):
    print("Número:", i)
```

Saída:
```text
Número: 1
Número: 2
Número: 3
```

### `while`
Repete o código enquanto a condição for verdadeira.

```python
contador = 1

while contador <= 3:
    print("Contador:", contador)
    contador += 1
```

Saída:
```text
Contador: 1
Contador: 2
Contador: 3
```

### `break`
Encerra a repetição antes de ela terminar normalmente.

```python
for i in range(1, 10):
    if i == 4:
        break
    print(i)
```

Saída:
```text
1
2
3
```

### `continue`
Pula para a próxima repetição.

```python
for i in range(1, 6):
    if i == 3:
        continue
    print(i)
```

Saída:
```text
1
2
4
5
```

## 6. Funções para números

### `abs()`
Retorna o valor absoluto de um número.

```python
print(abs(-15))
```

Saída: `15`

### `round()`
Arredonda um número.

```python
print(round(3.14159, 2))
print(round(7.8))
```

Saída:
```text
3.14
8
```

### `pow()`
Calcula uma potência.

```python
print(pow(2, 5))
```

Saída: `32`

### `min()` e `max()`
`min()` mostra o menor valor e `max()` mostra o maior.

```python
print(min(4, 9, 1))
print(max(4, 9, 1))
```

Saída:
```text
1
9
```

## 7. Funções e métodos para strings

### `upper()` e `lower()`
`upper()` transforma as letras em maiúsculas e `lower()` em minúsculas.

```python
print("python".upper())
print("PYTHON".lower())
```

Saída:
```text
PYTHON
python
```

### `strip()`
Remove os espaços do começo e do fim do texto.

```python
print("   olá   ".strip())
```

Saída: `olá`

### `replace()`
Troca uma parte do texto por outra.

```python
frase = "Eu gosto de Java"
print(frase.replace("Java", "Python"))
```

Saída: `Eu gosto de Python`

### `split()`
Divide um texto e coloca as partes em uma lista.

```python
print("maçã,banana,uva".split(","))
```

Saída:
```text
['maçã', 'banana', 'uva']
```

### `find()`
Mostra a posição em que um trecho aparece. Se não encontrar, retorna `-1`.

```python
texto = "programação"
print(texto.find("gra"))
print(texto.find("x"))
```

Saída:
```text
3
-1
```

## 8. Funções e métodos para listas

### Criar uma lista
Uma lista guarda vários valores. A primeira posição é a de número `0`.

```python
numeros = [10, 20, 30]
print(numeros)
print(numeros[0])
```

Saída:
```text
[10, 20, 30]
10
```

### `append()`
Adiciona um item no final da lista.

```python
frutas = ["maçã", "banana"]
frutas.append("uva")
print(frutas)
```

Saída:
```text
['maçã', 'banana', 'uva']
```

### `insert()`
Adiciona um item em uma posição escolhida.

```python
frutas = ["maçã", "uva"]
frutas.insert(1, "banana")
print(frutas)
```

Saída:
```text
['maçã', 'banana', 'uva']
```

### `remove()`
Remove um item pelo valor.

```python
frutas = ["maçã", "banana", "uva"]
frutas.remove("banana")
print(frutas)
```

Saída:
```text
['maçã', 'uva']
```

### `pop()`
Remove um item e o retorna. Se não indicar uma posição, remove o último.

```python
numeros = [1, 2, 3, 4]
numeros.pop()
print(numeros)

numeros.pop(0)
print(numeros)
```

Saída:
```text
[1, 2, 3]
[2, 3]
```

### `sort()`
Coloca os itens em ordem crescente. Com `reverse=True`, coloca em ordem decrescente.

```python
numeros = [5, 2, 9, 1]
numeros.sort()
print(numeros)

numeros.sort(reverse=True)
print(numeros)
```

Saída:
```text
[1, 2, 5, 9]
[9, 5, 2, 1]
```

### `reverse()`
Inverte a ordem atual dos itens.

```python
letras = ["a", "b", "c"]
letras.reverse()
print(letras)
```

Saída: `['c', 'b', 'a']`

### `len()`
Mostra quantos itens existem na lista. Também pode contar os caracteres de um texto.

```python
print(len([10, 20, 30]))
print(len("Python"))
```

Saída:
```text
3
6
```

## 9. Manipulação de arquivos

### `open()`
Abre um arquivo. Os modos mais usados são `"r"` para ler, `"w"` para escrever e `"a"` para acrescentar conteúdo ao final.

### `write()` e `close()`
`write()` escreve no arquivo e `close()` fecha o arquivo.

```python
arquivo = open("exemplo.txt", "w", encoding="utf-8")
arquivo.write("Primeira linha\n")
arquivo.write("Segunda linha\n")
arquivo.close()
```

### `read()`
Lê todo o conteúdo do arquivo.

```python
arquivo = open("exemplo.txt", "r", encoding="utf-8")
print(arquivo.read())
arquivo.close()
```

Saída:
```text
Primeira linha
Segunda linha
```

### `readline()`
Lê uma linha do arquivo por vez.

```python
arquivo = open("exemplo.txt", "r", encoding="utf-8")
print(arquivo.readline().strip())
print(arquivo.readline().strip())
arquivo.close()
```

Saída:
```text
Primeira linha
Segunda linha
```

### `with`
Abre o arquivo e fecha automaticamente ao terminar o bloco.

```python
with open("exemplo.txt", "w", encoding="utf-8") as arquivo:
    arquivo.write("Linha A\n")
    arquivo.write("Linha B\n")

with open("exemplo.txt", "r", encoding="utf-8") as arquivo:
    print(arquivo.read())
```

Saída:
```text
Linha A
Linha B
```
