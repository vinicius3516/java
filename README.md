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
5. [Exercícios Resolvidos](#5-exercícios-resolvidos)

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

---

## 5. Exercícios Resolvidos

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
