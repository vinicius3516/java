# ☕ Java — Anotações de Estudo

> Repositório de consulta pessoal com a teoria de Java organizada, explicada com analogias e acompanhada de exemplos de código. Serve como material de referência rápida para revisar conceitos sempre que necessário.

---

## 📑 Sumário

1. [Introdução sobre Programação](#1-introdução-sobre-programação)
   - [1.1 Algoritmo, Automação e Programa de Computador](#11-algoritmo-automação-e-programa-de-computador)
   - [1.2 O que é preciso para fazer um programa de computador](#12-o-que-é-preciso-para-fazer-um-programa-de-computador)
   - [1.3 Compilação, Interpretação e Máquina Virtual](#13-compilação-interpretação-e-máquina-virtual)
2. [Introdução à Linguagem Java](#2-introdução-à-linguagem-java)
   - [2.1 Versões do Java e LTS](#21-versões-do-java-e-lts)
   - [2.2 O que é o Java](#22-o-que-é-o-java)
   - [2.3 Edições do Java](#23-edições-do-java)
3. [Estrutura Sequencial](#3-estrutura-sequencial)
   - [3.1 Anatomia de um programa Java](#31-anatomia-de-um-programa-java)
   - [3.2 Variáveis e tipos primitivos](#32-variáveis-e-tipos-primitivos)
   - [3.3 Expressões aritméticas e operadores](#33-expressões-aritméticas-e-operadores)
   - [3.4 As três operações básicas: Entrada, Processamento e Saída](#34-as-três-operações-básicas-entrada-processamento-e-saída)
   - [3.5 Saída de dados (`System.out`)](#35-saída-de-dados-systemout)
   - [3.6 Processamento de dados e Casting](#36-processamento-de-dados-e-casting)
   - [3.7 Entrada de dados (`Scanner`)](#37-entrada-de-dados-scanner)
   - [3.8 Funções matemáticas (`Math`)](#38-funções-matemáticas-math)
4. [Estruturas Condicionais](#4-estruturas-condicionais)
   - [4.1 Expressões comparativas](#41-expressões-comparativas)
   - [4.2 Expressões lógicas](#42-expressões-lógicas)
   - [4.3 Estruturas condicionais (if / else / else if)](#43-estruturas-condicionais-if--else--else-if)
   - [4.4 Operadores de atribuição cumulativa](#44-operadores-de-atribuição-cumulativa)
   - [4.5 Estrutura switch-case](#45-estrutura-switch-case)
   - [4.6 Expressão condicional ternária](#46-expressão-condicional-ternária)
   - [4.7 Escopo e inicialização de variáveis](#47-escopo-e-inicialização-de-variáveis)
5. [Estruturas de Repetição](#5-estruturas-de-repetição)
   - [5.1 Estrutura de repetição `while`](#51-estrutura-de-repetição-while)
   - [5.2 Estrutura de repetição `for`](#52-estrutura-de-repetição-for)
   - [5.3 Estrutura de repetição `do-while`](#53-estrutura-de-repetição-do-while)
6. [Outros Tópicos Básicos em Java](#6-outros-tópicos-básicos-em-java)
   - [6.1 Funções interessantes para String](#61-funções-interessantes-para-string)
   - [6.2 Funções](#62-funções)
7. [Exercícios Resolvidos](#7-exercícios-resolvidos)

---

## 1. Introdução sobre Programação

### 1.1 Algoritmo, Automação e Programa de Computador

**Algoritmo** é uma sequência finita de instruções, bem definidas e ordenadas, que resolve um problema. Não é exclusivo da computação — uma receita de bolo é um algoritmo: passos finitos, em ordem, que levam a um resultado.

**Automação** é o uso de máquina(s) para executar esse procedimento de forma automática ou semiautomática, sem depender integralmente da ação humana a cada passo.

**Programa de computador** é um algoritmo escrito de forma que o computador consiga executá-lo. O computador, por sua vez, é a máquina que automatiza a execução de algoritmos — mas **não qualquer algoritmo**, apenas os *algoritmos computacionais*, ou seja, aqueles resolvíveis por:
- Processamento de dados
- Cálculos

> 💡 **Analogia:** pense no algoritmo como a *receita* e no programa como a receita *traduzida para uma língua que o forno (computador) entende e consegue seguir sozinho*.

### 1.2 O que é preciso para fazer um programa de computador

Para transformar um algoritmo em um programa funcional, quatro peças entram em jogo:

| Peça | Função |
|---|---|
| **Linguagem de programação** | Conjunto de regras léxicas e sintáticas para escrever o código (o "idioma"). |
| **IDE** | Software para editar e testar o programa (o "ambiente de trabalho"). |
| **Compilador** | Software que transforma código-fonte em código objeto (o "tradutor"). |
| **Gerador de código / Máquina Virtual** | Software que efetivamente executa o programa (o "motor"). |

### 1.3 Compilação, Interpretação e Máquina Virtual

- **Código-fonte**: o código exatamente como o programador escreve, em uma linguagem de programação (ex.: `.java`).
- **Compilação**: o código-fonte inteiro é traduzido de uma vez para código de máquina (ou bytecode) *antes* da execução. É como traduzir um livro inteiro antes de entregá-lo ao leitor.
- **Interpretação**: o código é lido e executado linha a linha, em tempo real, por um interpretador. É como um intérprete simultâneo traduzindo uma fala ao vivo.
- **Abordagem híbrida**: combina as duas — o código-fonte é primeiro **compilado** para um formato intermediário (bytecode) e depois esse bytecode é **interpretado/executado** por uma máquina virtual. **É exatamente o modelo do Java** (veja a seção 2.2).

> 💡 **Analogia:** a abordagem híbrida é como traduzir um livro para um "idioma universal simplificado" (bytecode) uma única vez, e depois qualquer pessoa em qualquer país (qualquer sistema operacional com JVM instalada) consegue interpretar esse idioma universal sem precisar de uma nova tradução completa.

---

## 2. Introdução à Linguagem Java

### 2.1 Versões do Java e LTS

Java lança novas versões periodicamente, mas nem todas são recomendadas para projetos reais. As versões **LTS (Long Term Support)** são as que recebem suporte e atualizações de segurança por um longo período, e são **sempre a escolha correta** ao iniciar um projeto novo.

> Resumo de cada versão: [devsuperior/curso-java — 04-versoes-do-java.md](https://github.com/devsuperior/curso-java/blob/main/04-versoes-do-java.md)

Entre as versões LTS existem **versões intermediárias** (não-LTS), lançadas apenas para que a comunidade teste e valide novas funcionalidades. Assim que a próxima LTS é lançada, essas versões intermediárias deixam de receber suporte. Por isso, **nunca se deve basear um projeto em uma versão não-LTS**.

> 💡 **Analogia:** LTS é como a edição de um software "estável" que recebe correções por anos; as versões intermediárias são como *betas* — ótimas para experimentar, arriscadas para colocar em produção.

### 2.2 O que é o Java

O Java é, ao mesmo tempo:
- **Uma linguagem de programação**: um conjunto de regras sintáticas.
- **Uma plataforma de desenvolvimento e execução**: dá acesso a um ecossistema de bibliotecas e a um ambiente de execução próprio (a JVM).

**Aspectos notáveis:**
- O código-fonte (`.java`) é **compilado para bytecode** (`.class`) e executado pela **JVM (Java Virtual Machine)** — o modelo híbrido descrito na seção 1.3.
- É **portável**: o mesmo bytecode roda em qualquer sistema operacional que tenha uma JVM ("*Write Once, Run Anywhere*").
- É **seguro e robusto** (tipagem forte, gerenciamento automático de memória via Garbage Collector).
- Roda em diversos tipos de dispositivo — de servidores corporativos a dispositivos embarcados.
- Domina o mercado corporativo desde o fim do século 20, sendo hoje uma das linguagens mais usadas no mundo.

```
Código-fonte (.java) --[compilador javac]--> Bytecode (.class) --[JVM]--> Execução
```

### 2.3 Edições do Java

| Edição | Sigla | Indicada para |
|---|---|---|
| **Java Micro Edition** | Java ME | Dispositivos embarcados e móveis (IoT) |
| **Java Standard Edition** | Java SE | *Core* da linguagem — desktop e servidores. **É a base estudada neste repositório.** |
| **Java Enterprise Edition** | Java EE (hoje Jakarta EE) | Aplicações corporativas de grande porte |

---

## 3. Estrutura Sequencial

A **estrutura sequencial** é o tipo de algoritmo mais simples: as instruções são executadas *uma após a outra*, na ordem em que aparecem, sem desvios (sem decisões ou repetições — isso vem depois, com estruturas condicionais e de repetição).

### 3.1 Anatomia de um programa Java

```java
public class Main {
    public static void main(String[] args) {
        // Todo programa Java começa a ser executado aqui
        System.out.println("Olá, mundo!");
    }
}
```

- `public class Main`: toda lógica em Java mora dentro de uma **classe**. O nome do arquivo (`Main.java`) deve ser igual ao nome da classe pública.
- `public static void main(String[] args)`: é o **método principal** — o ponto de entrada que a JVM procura e executa primeiro.
- `System.out.println(...)`: instrução de saída, imprime uma linha no console.

### 3.2 Variáveis e tipos primitivos

Uma **variável** é uma porção de memória RAM usada para armazenar um dado durante a execução do programa.

> 💡 **Analogia:** uma variável é uma **caixa com etiqueta** (o nome) guardada em uma prateleira (a memória). O **tipo** da variável define o tamanho e o formato dessa caixa — uma caixa de `int` não guarda o mesmo tipo de conteúdo que uma caixa de `String`.

| Tipo | Armazena | Exemplo |
|---|---|---|
| `int` | Número inteiro | `int idade = 30;` |
| `double` | Número decimal (ponto flutuante, precisão dupla) | `double preco = 19.90;` |
| `float` | Número decimal (precisão simples) | `float peso = 72.5f;` |
| `char` | Um único caractere | `char genero = 'F';` |
| `boolean` | Verdadeiro ou falso | `boolean ativo = true;` |
| `String` | Cadeia de caracteres (texto) | `String nome = "Vinicius";` |
| `long` | Número inteiro (faixa maior que `int`) | `long populacao = 8000000000L;` |

```java
String nome = "Vinicius";
int idade = 31;
double renda = 4000.0;

System.out.println("Bom dia! - " + nome);
System.out.printf("%s tem %d anos e ganha R$ %.2f reais%n", nome, idade, renda);
```

> ⚠️ **Cuidado com o separador decimal:** por padrão, a JVM pode usar a vírgula (`,`) como separador decimal dependendo do `Locale` do sistema operacional. Para garantir o padrão internacional com ponto (`.`), define-se o `Locale` logo no início do `main`:
> ```java
> Locale.setDefault(Locale.US); // Mantém o separador decimal como ponto '.'
> ```

### 3.3 Expressões aritméticas e operadores

Uma **expressão aritmética** é uma combinação de números unidos por operadores matemáticos, resolvida seguindo uma ordem específica de prioridade (a mesma da matemática básica: parênteses → multiplicação/divisão → soma/subtração).

| Operador | Significado | Exemplo | Resultado |
|---|---|---|---|
| `+` | Adição | `5 + 2` | `7` |
| `-` | Subtração | `5 - 2` | `3` |
| `*` | Multiplicação | `5 * 2` | `10` |
| `/` | Divisão | `5 / 2` | `2` (divisão inteira!) |
| `%` | Módulo (resto da divisão) | `5 % 2` | `1` |

> ⚠️ **Divisão entre inteiros trunca o resultado.** `5 / 2` em Java resulta em `2`, não `2.5`, porque os dois operandos são `int`. Para obter o resultado decimal, é necessário *casting* (seção 3.6).

### 3.4 As três operações básicas: Entrada, Processamento e Saída

Todo programa sequencial pode ser resumido em três operações fundamentais:

```
ENTRADA  ──▶  PROCESSAMENTO  ──▶  SAÍDA
(ler dado)    (calcular/transformar)   (exibir resultado)
```

> 💡 **Analogia:** pense em uma **fábrica**: a *entrada* é a matéria-prima que chega, o *processamento* é a linha de produção que transforma essa matéria-prima, e a *saída* é o produto final que sai pela porta.

Essas três operações aparecem em praticamente todo exercício de lógica de programação — inclusive nos [exercícios resolvidos](#5-exercícios-resolvidos) deste repositório.

### 3.5 Saída de dados (`System.out`)

Java oferece três formas principais de exibir dados no console:

| Método | Comportamento |
|---|---|
| `System.out.print(x)` | Imprime sem quebrar linha ao final |
| `System.out.println(x)` | Imprime e quebra a linha ao final |
| `System.out.printf(formato, args...)` | Imprime com **formatação controlada** (como um "molde" para o texto) |

Principais especificadores de formatação usados com `printf`/`String.format`:

| Especificador | Uso | Exemplo |
|---|---|---|
| `%d` | Número inteiro | `printf("%d", 10)` → `10` |
| `%f` | Número decimal | `printf("%.2f", 3.14159)` → `3.14` |
| `%s` | Texto (String) | `printf("%s", "Vinicius")` → `Vinicius` |
| `%c` | Caractere | `printf("%c", 'A')` → `A` |
| `%n` | Quebra de linha (portável entre SOs) | — |

```java
String product1 = "Computer";
double price1 = 2100.0;
double measure = 53.234567;

System.out.printf("Produto: %s, preço: $ %.2f%n", product1, price1);
System.out.printf("Medida com 8 casas decimais: %.8f%n", measure);
System.out.printf("Medida arredondada (3 casas): %.3f%n", measure);
```

### 3.6 Processamento de dados e Casting

**Processar dados**, em sua forma mais simples, é o ato de **atribuir o resultado de uma expressão a uma variável**.

```java
int w, y;
w = 5;
y = 2 * w; // processamento: calcula e atribui
```

#### Casting

**Casting** é a **conversão explícita** de um tipo de dado para outro. É necessário sempre que o compilador não consegue "adivinhar" sozinho que o resultado de uma expressão deveria ser de um tipo diferente do esperado pelos operandos.

> 💡 **Analogia:** é como despejar o conteúdo de um copo pequeno (`int`) dentro de um copo maior (`double`) — fisicamente cabe, mas você precisa **avisar explicitamente** ao Java que está fazendo essa conversão, senão ele assume o tipo mais "estreito" dos operandos envolvidos.

```java
// ❌ Exemplo com erro de raciocínio:
int a, b;
double resultado;
a = 5;
b = 2;
resultado = a / b; // a divisão inteira acontece ANTES da atribuição!
System.out.println(resultado); // imprime 2.0, e não 2.5

// ✅ Exemplo corrigido com casting:
int a, b;
double resultado;
a = 5;
b = 2;
resultado = (double) a / b; // converte 'a' para double ANTES da divisão
System.out.println(resultado); // imprime 2.5
```

O ponto-chave: `(double) a / b` converte apenas `a` para `double` **antes** da divisão ser realizada — e como um dos operandos já é `double`, o Java promove a divisão inteira para uma divisão de ponto flutuante.

### 3.7 Entrada de dados (`Scanner`)

A classe `Scanner` (pacote `java.util`) é a forma padrão de ler dados digitados pelo usuário no console.

```java
Scanner sc = new Scanner(System.in);

int h = sc.nextInt();       // lê um número inteiro
double d = sc.nextDouble(); // lê um número decimal
char c = sc.next().charAt(0); // lê a primeira letra de uma palavra
String linha = sc.nextLine(); // lê uma linha inteira de texto

sc.close(); // libera o recurso ao final
```

| Método | Lê |
|---|---|
| `sc.nextInt()` | Um valor `int` |
| `sc.nextDouble()` | Um valor `double` |
| `sc.next().charAt(0)` | O primeiro caractere de uma palavra |
| `sc.nextLine()` | Uma linha inteira de texto |

> ⚠️ **A pegadinha clássica do buffer:** quando se usa `sc.nextInt()` (ou `nextDouble()`) e, na sequência, `sc.nextLine()`, o `nextLine()` "captura" apenas a quebra de linha (`\n`) que ficou pendente no buffer de entrada — pulando a leitura real de texto. Isso é conhecido como **"limpar o buffer de leitura"**.
>
> ```java
> int h = sc.nextInt();
> sc.nextLine(); // consome a quebra de linha deixada pelo Enter do nextInt()
> String descricao = sc.nextLine(); // agora lê a linha corretamente
> ```
> 💡 **Analogia:** é como apertar Enter duas vezes sem perceber — o primeiro Enter "sobra" na fila e é consumido silenciosamente pela próxima leitura, a não ser que você o descarte de propósito antes.

### 3.8 Funções matemáticas (`Math`)

A classe `Math` (pacote `java.lang`, não precisa de `import`) concentra as funções matemáticas prontas da linguagem.

| Método | Faz | Exemplo |
|---|---|---|
| `Math.sqrt(x)` | Raiz quadrada | `Math.sqrt(25.0)` → `5.0` |
| `Math.pow(x, y)` | `x` elevado a `y` | `Math.pow(2.0, 3.0)` → `8.0` |
| `Math.abs(x)` | Valor absoluto | `Math.abs(-5.0)` → `5.0` |

```java
double x = 3.0, y = 4.0, z = -5.0;

System.out.println("Raiz quadrada de " + x + " = " + Math.sqrt(x));
System.out.println(x + " elevado a " + y + " = " + Math.pow(x, y));
System.out.println("Valor absoluto de " + z + " = " + Math.abs(z));
```

---

## 4. Estruturas Condicionais

Estruturas condicionais permitem que o programa **desvie** o fluxo de execução com base em uma condição — deixando de lado a execução puramente sequencial da seção 3 para tomar decisões.

### 4.1 Expressões comparativas

Uma **expressão comparativa** é uma expressão que compara dois valores e produz um resultado **booleano** (`true` ou `false`), em vez de um número.

```java
5 > 10   // resultado: false
```

> 💡 **Analogia:** uma expressão comparativa é uma **pergunta de sim/não** feita ao programa — "esse valor é maior que aquele?" — e a resposta (`true`/`false`) é o que as estruturas condicionais (próximo tópico) usam para decidir qual caminho seguir.

| Operador | Significado |
|---|---|
| `>` | Maior que |
| `<` | Menor que |
| `>=` | Maior ou igual a |
| `<=` | Menor ou igual a |
| `==` | Igual a |
| `!=` | Diferente de |

```java
int a = 5;
int b = 10;

System.out.println(a > b);  // false
System.out.println(a < b);  // true
System.out.println(a == 5); // true
System.out.println(a != b); // true
```

> ⚠️ **Não confunda `==` com `=`.** O operador `=` **atribui** um valor a uma variável; o operador `==` **compara** dois valores. Trocar um pelo outro é um dos erros mais comuns de quem está começando.

### 4.2 Expressões lógicas

Assim como as expressões comparativas, uma **expressão lógica** também resulta em `true` ou `false` — mas, em vez de comparar dois valores diretamente, ela **combina o resultado de outras expressões** (geralmente comparativas) usando os operadores lógicos.

| Operador | Nome | Ideia |
|---|---|---|
| `&&` | E (AND) | **Todas** as comparações precisam ser verdadeiras |
| \|\| | OU (OR) | **Pelo menos uma** das comparações precisa ser verdadeira |
| `!` | Não (NOT) | **Inverte** o resultado da expressão |

> 💡 **Analogia:** pense em `&&` como uma dupla exigência — "preciso do CPF **e** do endereço para liberar o cadastro" (falta um, já não libera). `||` é uma exigência flexível — "aceito CPF **ou** RG" (qualquer um dos dois já resolve). E `!` é simplesmente virar a resposta ao contrário — se a resposta era "sim", `!` faz virar "não".

#### `&&` (E) — todas precisam ser verdadeiras

```java
int x = 5;

x <= 20 && x == 10   // false -> a segunda comparação (x == 10) é falsa, então tudo vira false
x > 0   && x != 3    // true  -> as duas comparações são verdadeiras
```

**Tabela-verdade do `&&`:**

| A | B | A `&&` B |
|---|---|---|
| F | F | F |
| F | V | F |
| V | F | F |
| V | V | V |

#### `||` (OU) — basta uma ser verdadeira

```java
int x = 5;

x == 10 || x <= 20   // true  -> a segunda comparação (x <= 20) já é verdadeira, então tudo vira true
x >= 10 || x != 5    // false -> as duas comparações são falsas
```

**Tabela-verdade do `||`:**

| A | B | A \|\| B |
|---|---|---|
| F | F | F |
| F | V | V |
| V | F | V |
| V | V | V |

#### `!` (NÃO) — inverte o resultado

```java
int x = 5;

!(x == 10)              // true  -> "x == 10" é false, o '!' inverte para true
!(x <= 20 && x == 10)   // true  -> "x <= 20 && x == 10" é false, o '!' inverte para true
```

> 💡 **Analogia:** `!(x == 10)` é como perguntar **"5 não é igual a 10, né?"** — e a resposta é **"sim, é verdade, 5 não é igual a 10"** (`true`). O `!` transforma a pergunta em sua negativa e avalia se essa negativa é verdadeira.

**Tabela-verdade do `!`:**

| A | `!`A |
|---|---|
| F | V |
| V | F |

### 4.3 Estruturas condicionais (if / else / else if)

Uma **estrutura condicional** é uma estrutura de controle que permite definir que um determinado bloco de comandos só será executado dependendo do resultado de uma condição (uma expressão comparativa e/ou lógica, como as vistas em [4.1](#41-expressões-comparativas) e [4.2](#42-expressões-lógicas)).

#### `if` simples

```java
if (condicao) {
    comando1;
    comando2;
}
```

Os comandos dentro das chaves só são executados caso `condicao` seja `true`. Caso contrário, o bloco inteiro é simplesmente ignorado e a execução segue em frente.

#### `if` / `else` — estrutura composta

```java
if (condicao) {
    comando1;
    comando2;
} else {
    comando3;
    comando4;
}
```

Aqui a lógica muda um pouco: se `condicao` for falsa, o bloco executado é exatamente o que está dentro do `else`. É como dizer **"se tal condição for verdadeira, execute X; caso contrário, execute Y"** — sempre um dos dois blocos roda, nunca os dois nem nenhum.

> 💡 **Analogia:** pense num guarda-chuva — "se estiver chovendo, eu levo o guarda-chuva; senão, eu deixo em casa". Não existe meio-termo: uma das duas ações sempre acontece.

#### E quando há mais de duas possibilidades?

Uma forma (pouco elegante) de resolver seria aninhar um `if`/`else` dentro do `else`:

```java
if (condicao) {
    comando1;
    comando2;
} else {
    if (condicao) {
        comando3;
    } else {
        comando4;
    }
}
```

Isso funciona, mas cada nova possibilidade cria mais um nível de aninhamento, o que deixa o código cada vez mais difícil de ler. Na prática, o dia a dia usa uma forma mais simples e organizada para o mesmo caso: o `else if`.

#### `if` / `else if` / `else`

```java
if (condicao) {
    comando1;
    comando2;
} else if (condicao) {
    comando3;
} else {
    comando4;
}
```

Continuamos lidando com mais de duas condições, só que agora de forma linear e mais legível — cada `else if` é testado em sequência, na ordem em que aparece, até que uma condição seja verdadeira (ou até cair no `else` final, se nenhuma for).

### 4.4 Operadores de atribuição cumulativa

Repare no trecho abaixo, que calcula o valor de uma conta cobrando R$ 2,00 por minuto excedente após os 100 minutos:

```java
Scanner sc = new Scanner(System.in);

System.out.println("Informe o numero de minutos:");
int minutes = sc.nextInt();

double accountValue = 50.0;

if (minutes > 100) {
    accountValue = accountValue + (minutes - 100) * 2;
    System.out.printf("O valor da sua conta fechou em: R$ %.2f%n", accountValue);
} else {
    System.out.printf("O valor da sua conta fechou em: R$ %.2f%n", accountValue);
}

sc.close();
```

No cálculo do novo valor da conta, foi preciso pegar a própria variável `accountValue` e somá-la ao resultado de uma operação:

```java
accountValue = accountValue + (minutes - 100) * 2;
```

Esse padrão — "pega a variável, aplica uma operação nela mesma, e guarda o resultado de volta nela" — é tão comum que Java oferece uma forma mais curta para escrevê-lo: o **operador de atribuição cumulativa**. Em vez de `accountValue = accountValue + ...`, basta escrever:

```java
accountValue += (minutes - 100) * 2; // "accountValue passa a valer ele mesmo + (minutes - 100) * 2"
```

> 💡 **Analogia:** é como dizer "acrescenta isso ao que eu já tinha", em vez de "pega o que eu já tinha, soma com isso, e guarda de novo no mesmo lugar" — o resultado é idêntico, só que mais direto.

Existe um operador cumulativo para cada operador aritmético:

| Forma cumulativa | Equivale a |
|---|---|
| `a += b` | `a = a + b` |
| `a -= b` | `a = a - b` |
| `a *= b` | `a = a * b` |
| `a /= b` | `a = a / b` |
| `a %= b` | `a = a % b` |

O mesmo programa, agora usando o operador cumulativo:

```java
Scanner sc = new Scanner(System.in);

System.out.println("Informe o numero de minutos:");
int minutes = sc.nextInt();

double accountValue = 50.0;

if (minutes > 100) {
    accountValue += (minutes - 100) * 2;
    System.out.printf("O valor da sua conta fechou em: R$ %.2f%n", accountValue);
} else {
    System.out.printf("O valor da sua conta fechou em: R$ %.2f%n", accountValue);
}

sc.close();
```

### 4.5 Estrutura switch-case

Quando existem várias opções de fluxo diferentes a serem tratadas com base no valor de **uma única variável**, encadear vários `if`/`else if` pode deixar o código repetitivo. Nesses casos, uma alternativa é a estrutura `switch-case`:

```java
switch (expressao) {
    case valor1:
        comando1;
        comando2;
        break;
    case valor2:
        comando3;
        comando4;
        break;
    default:
        comando5;
        comando6;
        break;
}
```

`expressao` é avaliada uma única vez, e o Java compara o resultado com cada `case`, executando o bloco correspondente ao valor que bater. Se nenhum `case` corresponder, o bloco `default` é executado (funciona como o `else` final de uma cadeia de `if`/`else if`).

> 💡 **Analogia:** pense num `switch` como um recepcionista com uma lista de senhas — ele olha a sua senha (`expressao`) e te encaminha direto para o guichê (`case`) correspondente, sem precisar perguntar "é a senha 1? não? é a 2? não?..." uma por uma como um `if`/`else if` faria.

> ⚠️ **Atenção ao `break`:** cada `case` deve terminar com `break`, senão a execução "cai" para o próximo `case` (comportamento chamado de *fall-through*) e continua executando os comandos seguintes, mesmo que o valor não bata.

**Exemplo — convertendo um número em dia da semana:**

```java
Scanner sc = new Scanner(System.in);
int x = sc.nextInt();
String dia;

switch (x) {
    case 1:
        dia = "domingo";
        break;
    case 2:
        dia = "segunda";
        break;
    case 3:
        dia = "terca";
        break;
    case 4:
        dia = "quarta";
        break;
    case 5:
        dia = "quinta";
        break;
    case 6:
        dia = "sexta";
        break;
    case 7:
        dia = "sabado";
        break;
    default:
        dia = "valor invalido";
        break;
}

System.out.println("Dia da semana: " + dia);
sc.close();
```

### 4.6 Expressão condicional ternária

É uma alternativa mais compacta ao `if`/`else` para os casos em que o único objetivo é **decidir o valor de uma variável** com base em uma condição.

**Sintaxe:**

```java
(condicao) ? valor_se_true : valor_se_false;
```

Se `condicao` for `true`, a expressão inteira "vira" `valor_se_true`; se for `false`, "vira" `valor_se_false`. É a mesma decisão de um `if`/`else`, só que expressa como um valor único, direto na linha.

> 💡 **Analogia:** pense nela como uma pergunta de sim/não seguida de duas respostas prontas, separadas por `:` — "está chovendo? leva o guarda-chuva : deixa em casa" — só que tudo isso "vira" o valor de uma variável de uma vez, sem precisar de blocos `{ }`.

**Exemplo — calculando desconto sem a ternária:**

```java
double preco = 34.5;
double desconto;

if (preco < 20.0) {
    desconto = preco * 0.1;
} else {
    desconto = preco * 0.05;
}
```

**O mesmo exemplo, agora com a condicional ternária:**

```java
double preco = 34.5;
double desconto = (preco < 20.0) ? preco * 0.1 : preco * 0.05;
```

O resultado é exatamente o mesmo, mas em uma única linha — ideal quando a única coisa que o `if`/`else` faz é atribuir um valor a uma variável.

### 4.7 Escopo e inicialização de variáveis

O **escopo** de uma variável é a região do programa onde ela é válida — ou seja, onde ela pode ser referenciada. Em Java, esse limite é sempre um bloco `{ }`: uma variável declarada dentro de um bloco só existe (e só pode ser usada) dentro dele; fora disso, ela simplesmente não é enxergada.

> 💡 **Analogia:** pense no escopo como o cômodo de uma casa — o que você guarda dentro do quarto só está acessível enquanto você está naquele quarto. Saindo dele (fechando a chave `}`), o que estava lá dentro deixa de existir para o resto da casa.

**Exemplo com erro de escopo:**

```java
double preco = 400.0;

if (preco < 200) {
    double desconto = preco * 0.05;
}

System.out.println(desconto); // ERRO de compilação: 'desconto' não existe aqui
```

Esse código não compila porque `desconto` foi declarada **dentro** do bloco do `if` — seu escopo termina na chave `}` que fecha o `if`. O `System.out.println`, estando fora desse bloco, simplesmente não tem acesso a ela.

**Correção — declarar (e inicializar) a variável antes do `if`:**

```java
double preco = 400.0;
double desconto = 0;

if (preco < 200) {
    desconto = preco * 0.05;
}

System.out.println(desconto);
```

Agora `desconto` é declarada num escopo mais amplo (fora do `if`), e o bloco do `if` apenas **atribui** um novo valor a ela — sem redeclará-la. Assim ela continua acessível no `System.out.println`, valendo `0` caso a condição do `if` seja falsa, ou o valor calculado caso seja verdadeira.

> ⚠️ **Por que inicializar com `0`?** o compilador não sabe, em tempo de compilação, se a condição do `if` vai ser verdadeira ou falsa em tempo de execução. Se `desconto` fosse apenas declarada (`double desconto;`, sem valor) e o `if` não fosse executado, a variável chegaria "vazia" até o `println` — e o Java não permite usar uma variável local que pode não ter sido inicializada. Dar um valor inicial (mesmo que `0`) garante que ela sempre tenha algo válido, independente do caminho que o programa seguir.

Esse mesmo princípio vale de forma geral: **uma variável não pode ser usada — nem mesmo impressa — antes de ser inicializada.** Referenciá-la em qualquer expressão sem antes atribuir um valor é erro de compilação em Java.

---

## 5. Estruturas de Repetição

### 5.1 Estrutura de repetição `while`

O `while` é uma estrutura de controle que **repete a execução de um bloco de código enquanto uma condição for verdadeira**. Assim que a condição avaliar `false`, o laço para e a execução segue para o que vem depois do bloco.

**Sintaxe:**

```java
while (condicao) {
    comando1;
    comando2;
}
```

A regra é simples: se `condicao` for `true`, executa o bloco e volta a testar a condição de novo; se for `false`, pula o bloco inteiro e segue em frente.

O uso mais comum do `while` é justamente quando **não se sabe de antemão quantas repetições serão necessárias** — diferente de, por exemplo, percorrer um intervalo fixo de números.

> 💡 **Analogia:** pense no `while` como alguém servindo café enquanto a xícara não estiver cheia — ninguém sabe de antemão quantos "goles" de café serão necessários; a única regra é continuar servindo enquanto a condição ("xícara não está cheia") for verdadeira.

**Exemplo — somando números até o usuário digitar 0:**

O cenário: o programa deve receber números inteiros do usuário até que o valor digitado seja `0`. Quando isso acontecer, deve exibir a soma de todos os números diferentes de zero informados. Como não se sabe quantos números o usuário vai digitar, esse é exatamente o tipo de caso que pede um `while`:

```java
import java.util.Locale;
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Locale.setDefault(Locale.US);
        Scanner sc = new Scanner(System.in);

        int x = sc.nextInt();
        int soma = 0;

        while (x != 0) {
            soma += x;
            x = sc.nextInt();
        }

        System.out.println("A soma dos valores informados é: " + soma);

        sc.close();
    }
}
```

A cada volta do laço, o valor lido é somado a `soma`, e um novo número é lido em seguida. Quando o usuário finalmente digitar `0`, a condição `x != 0` se torna `false` e o `while` é encerrado.

### 5.2 Estrutura de repetição `for`

O `for` é uma estrutura de controle que repete um bloco de comandos para um determinado intervalo de valores. Ao contrário do [`while`](#51-estrutura-de-repetição-while), ele é a escolha natural **quando já se sabe de antemão a quantidade de repetições** (ou o intervalo de valores a percorrer).

**Sintaxe:**

```java
for (inicio; condicao; incremento) {
    comando1;
    comando2;
}
```

O `for` é dividido em três partes, separadas por `;`:

- **`inicio`** — executado **uma única vez**, logo no começo, geralmente criando a variável de controle do laço (a mesma usada na condição e no incremento).
- **`condicao`** — testada a cada volta, igual ao `while`: se `true`, o bloco executa e o laço continua; se `false`, o `for` é encerrado.
- **`incremento`** — executado **ao final de cada volta**, depois do bloco rodar, e é o responsável por "andar" em direção à condição de parada.

> 💡 **Analogia:** pense no `for` como configurar um contador regressivo de forno — você define o ponto de partida (`inicio`), até onde ele deve contar (`condicao`), e de quanto em quanto ele avança a cada segundo (`incremento`). Tudo isso já fica combinado de uma vez, na própria "cabeça" do loop.

**Exemplo — somando N números lidos do usuário:**

O cenário: ler um valor inteiro `N` e, em seguida, ler `N` números inteiros, exibindo ao final a soma de todos eles. Como a quantidade de repetições (`N`) é conhecida antes do laço começar, esse é um caso perfeito para o `for`:

```java
import java.util.Locale;
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Locale.setDefault(Locale.US);
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();
        int soma = 0;

        for (int i = 0; i < n; i++) {
            int x = sc.nextInt();
            soma += x;
        }

        System.out.println("A soma dos numeros é: " + soma);

        sc.close();
    }
}
```

Aqui, `int i = 0` é o `inicio` (criado só na primeira vez), `i < n` é a `condicao` (testada a cada volta) e `i++` é o `incremento` (executado ao final de cada volta, somando 1 a `i`). Esse `i++` também poderia ser escrito como `i += 1` — o efeito é o mesmo.

**Contando para cima:**

```java
for (int i = 5; i <= 10; i++) {
    System.out.println("I vale: " + i);
}
```

**Contando para baixo (decrementando):**

Basta inverter a lógica: começar de um valor maior, testar até um valor menor, e decrementar em vez de incrementar (`i--`, equivalente a `i -= 1`):

```java
for (int i = 5; i >= 0; i--) {
    System.out.println("I vale: " + i);
}
```

### 5.3 Estrutura de repetição `do-while`

É uma variação menos usada que o [`while`](#51-estrutura-de-repetição-while) e o [`for`](#52-estrutura-de-repetição-for), mas que se encaixa melhor em alguns cenários específicos.

A diferença está em **quando** a condição é verificada: no `while` e no `for`, a condição é testada **antes** de cada execução do bloco — se ela já começar `false`, o bloco pode nunca rodar. No `do-while`, a condição só é verificada **ao final** do loop, o que garante que o bloco **sempre executa pelo menos uma vez**, independente do resultado da condição.

**Sintaxe:**

```java
do {
    comando1;
    comando2;
} while (condicao);
```

> 💡 **Analogia:** pense no `do-while` como provar um prato antes de decidir se repete — você primeiro come (executa o bloco), e só depois pergunta "quero mais?" (testa a condição). No `while`/`for` é o contrário: primeiro se pergunta "tem mais no prato?" para então decidir se come.

**Exemplo — conversor de Celsius para Fahrenheit com repetição controlada pelo usuário:**

```java
import java.util.Locale;
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Locale.setDefault(Locale.US);
        Scanner sc = new Scanner(System.in);

        char resp;

        do {
            System.out.print("Digite a temperatura em Celsius: ");
            double c = sc.nextDouble();
            double f = 9 * c / 5 + 32;
            System.out.printf("Equivalente em Fahrenheit: %.1f%n", f);
            System.out.print("Deseja repetir (s/n)? ");
            resp = sc.next().charAt(0);
        } while (resp != 'n');

        sc.close();
    }
}
```

Tudo dentro do `do { ... }` é executado pelo menos uma vez — o programa sempre pede ao menos uma temperatura antes mesmo de perguntar se o usuário quer repetir. O loop só volta a executar caso a condição do `while` final (`resp != 'n'`) seja `true`; assim que o usuário digitar `n`, a condição vira `false` e o laço termina.

---

## 6. Outros Tópicos Básicos em Java

### 6.1 Funções interessantes para String

`String` é uma classe do Java (não um tipo primitivo) e, como tal, oferece vários **métodos prontos** para manipular texto sem precisar reimplementar essas operações na mão. Algumas das mais úteis no dia a dia:

| Categoria | Método | O que faz |
|---|---|---|
| Formatar | `toLowerCase()` | Converte todos os caracteres para minúsculo |
| Formatar | `toUpperCase()` | Converte todos os caracteres para maiúsculo |
| Formatar | `trim()` | Remove espaços em branco do início e do fim da string |
| Recortar | `substring(inicio)` | Retorna a substring a partir da posição `inicio` até o fim |
| Recortar | `substring(inicio, fim)` | Retorna a substring entre as posições `inicio` (incluso) e `fim` (exclusivo) |
| Substituir | `replace(char, char)` | Troca todas as ocorrências de um caractere por outro |
| Substituir | `replace(String, String)` | Troca todas as ocorrências de uma substring por outra |
| Buscar | `indexOf(String)` | Retorna a posição da **primeira** ocorrência de uma substring (ou `-1` se não encontrar) |
| Buscar | `lastIndexOf(String)` | Retorna a posição da **última** ocorrência de uma substring (ou `-1` se não encontrar) |
| Dividir | `split(String)` | Quebra a string em pedaços, usando o argumento como separador |

> 💡 **Analogia:** pense numa `String` como uma fita de texto: `substring` recorta um pedaço da fita, `replace` troca trechos por outros, `indexOf`/`lastIndexOf` procuram em que ponto da fita algo aparece, e `split` corta a fita inteira em vários pedaços menores, um para cada palavra.

**Exemplo — testando cada método:**

```java
String original = "abcde FGHIJ ABC abc DEFG ";

String s01 = original.toLowerCase();
String s02 = original.toUpperCase();
String s03 = original.trim();
String s04 = original.substring(2);
String s05 = original.substring(2, 9);
String s06 = original.replace('a', 'x');
String s07 = original.replace("abc", "xy");
int i = original.indexOf("bc");
int j = original.lastIndexOf("bc");

System.out.println("Original: -" + original + "-");
System.out.println("toLowerCase: -" + s01 + "-");
System.out.println("toUpperCase: -" + s02 + "-");
System.out.println("trim: -" + s03 + "-");
System.out.println("substring(2): -" + s04 + "-");
System.out.println("substring(2, 9): -" + s05 + "-");
System.out.println("replace('a', 'x'): -" + s06 + "-");
System.out.println("replace(\"abc\", \"xy\"): -" + s07 + "-");
System.out.println("Index of 'bc': " + i);
System.out.println("Last index of 'bc': " + j);
```

> ⚠️ **Strings são imutáveis:** nenhum desses métodos altera `original` — todos retornam uma **nova** string com o resultado. É por isso que cada exemplo guarda o retorno numa variável nova (`s01`, `s02`, ...) em vez de reatribuir `original`.

**A operação `split`:**

```java
String s = "potato apple lemon";
String[] vect = s.split(" ");

String word1 = vect[0];
String word2 = vect[1];
String word3 = vect[2];
```

Quando a declaração é `String[]` (com colchetes), o resultado é um **vetor** (array) — um conjunto de valores indexados, ainda não estudado em detalhe até aqui. No caso do `split`, o vetor resultante é a frase original dividida em partes, uma palavra por posição: `vect[0]` é `"potato"`, `vect[1]` é `"apple"`, e assim por diante.

---

### 6.2 Funções

Uma **função** representa um processamento que tem um significado próprio — um pedaço de lógica com nome, que pode ser chamado sempre que aquele processamento for necessário. Exemplos de funções que já vínhamos usando sem chamar assim: `Math.sqrt(double)` e `System.out.println(string)`.

**Principais vantagens de usar funções:**

- **Modularização** — divide um programa grande em pedaços menores e mais fáceis de entender.
- **Delegação** — quem chama a função não precisa saber *como* ela resolve o problema, só *o que* ela faz.
- **Reaproveitamento** — a mesma lógica pode ser chamada várias vezes, em vários pontos do programa, sem duplicar código.

**Entrada e saída de dados:**

- Uma função pode **receber dados de entrada**, chamados de **parâmetros** (na definição da função) ou **argumentos** (quando ela é chamada com valores concretos).
- Uma função pode **ou não retornar uma saída** — algumas apenas executam uma ação (como `showResult`, abaixo) e outras devolvem um valor para quem as chamou (como `max`, abaixo).

> 💡 **Nota:** em orientação a objetos, funções definidas dentro de uma classe recebem o nome de **métodos** — é o mesmo conceito, apenas um nome mais específico para o contexto.

**Exemplo — encontrando o maior entre três números:**

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter three numbers:");

        int a = sc.nextInt();
        int b = sc.nextInt();
        int c = sc.nextInt();

        int higher = max(a, b, c);
        showResult(higher);

        sc.close();
    }

    public static int max(int x, int y, int z) {
        int aux;
        if (x > y && x > z) {
            aux = x;
        } else if (y > z) {
            aux = y;
        } else {
            aux = z;
        }
        return aux;
    }

    public static void showResult(int value) {
        System.out.println("Higher = " + value);
    }
}
```

```
Enter three numbers:
5
8
3
Higher = 8
```

Aqui, `max` é uma função que **recebe três parâmetros** (`x`, `y`, `z`) e **retorna** (`return`) o maior deles como `int`. Já `showResult` **recebe um parâmetro** (`value`) mas **não retorna nada** (`void`) — sua única função é imprimir o resultado na tela. Repare também no reaproveitamento: toda a lógica de "achar o maior" fica isolada em `max`, podendo ser chamada de qualquer lugar do programa sem reescrever o `if`/`else if`/`else`.

> 💬 Os modificadores `public` e `static` que aparecem antes de cada função ainda serão vistos em mais detalhe adiante no curso.

---

## 7. Exercícios Resolvidos

Exercícios práticos de fixação da **estrutura sequencial**, escritos no repositório de prática `java-estudos` (código-fonte à parte deste material teórico):

<details>
<summary><strong>Exercício — Soma de dois valores inteiros</strong></summary>

```java
int value1 = sc.nextInt();
int value2 = sc.nextInt();
int soma = value1 + value2;
System.out.printf("SOMA = %d", soma);
```
</details>

<details>
<summary><strong>Exercício — Área do círculo</strong></summary>

```java
double raio = sc.nextDouble();
double pi = 3.14159;
double area = pi * Math.pow(raio, 2.0);
System.out.printf("Value = %.4f", area);
```
</details>

<details>
<summary><strong>Exercício — Diferença entre produtos de pares</strong></summary>

```java
int value1 = sc.nextInt();
int value2 = sc.nextInt();
int value3 = sc.nextInt();
int value4 = sc.nextInt();
int diferenca = value1 * value2 - value3 * value4;
System.out.println("DIFERENCA = " + diferenca);
```
</details>

<details>
<summary><strong>Exercício — Cálculo de salário</strong></summary>

```java
int horasTrabalhadas = sc.nextInt();
double valorHora = sc.nextDouble();
double salario = horasTrabalhadas * valorHora;

System.out.printf("HORAS = %d%n", horasTrabalhadas);
System.out.printf("SALARIO = %.2f", salario);
```
</details>

<details>
<summary><strong>Exercício — Nota fiscal de dois produtos</strong></summary>

Combina **entrada** (código, quantidade e valor de duas peças), **processamento** (cálculo do total) e **saída** (valor formatado como moeda) — o ciclo completo da seção 3.4.

```java
System.out.println("Informe os valores do produto 01");
int pecaCode1 = sc.nextInt();
int pecaNumber1 = sc.nextInt();
double pecaValue1 = sc.nextDouble();

System.out.println("Informe os valores do produto 02");
int pecaCode2 = sc.nextInt();
int pecaNumber2 = sc.nextInt();
double pecaValue2 = sc.nextDouble();

double total = pecaNumber1 * pecaValue1 + pecaNumber2 * pecaValue2;

System.out.printf("VALOR A PAGAR: R$ %.2f", total);
```
</details>
