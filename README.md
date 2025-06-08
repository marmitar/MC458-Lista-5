# Analysis of Algorithms I (MC458) - Test 5

- [Questions](./Enunciado.pdf)
- [Answers](./Resposta.pdf)
- [Turn in](./Entrega.pdf)

## Dynamic Programming

---

### Question 1

Given three strings over an alphabet $\Sigma$-$X$ of length $n$, $Y$ of length $m$, and $Z$ of length $n+m$-determine whether $Z$ is an **interleaving** of $X$ and $Y$.

A string $Z$ is an interleaving of $X$ and $Y$ if $Z$ can be split into two disjoint subsequences, one equal to $X$ and the other to $Y$.
For example, with $n = 11$, $X = \texttt{programacao}$; $m = 8$, $Y = \texttt{dinamica}$; and $Z = \texttt{prdoingramamaciaoca}$, the string $Z$ **is** an interleaving of $X$ and $Y$ (the letters of $X$ are bolded inside $Z$).

Design a **top-down dynamic-programming algorithm with memoization** that, given $n$, $m$, and the strings $X$, $Y$, and $Z$, returns $1$ if $Z$ is an interleaving of $X$ and $Y$ and $0$ otherwise.

**Mandatory steps**

1. **(50 %)** Prove that the problem has optimal substructure by deriving a recurrence relation to be used in your algorithm. Explain every term and give the base cases and their values.
2. **(30 %)** *Only after finishing (1)*, describe your algorithm at a high level (or in pseudo-code).
3. **(20 %)** Analyse the time and space complexities of your algorithm as functions of $n$ and $m$.


---

### Question 2

Travelling downstream on the Azamonas River, you encounter $n$ villages $A_1, A_2, \dots, A_n$.
You start at $A_1$ and must reach $A_n$ to catch a flight back to Campinas.
With no roads available, you have to rent canoes in the villages.
You receive a price table: for every $1 \le i < j \le n$ it lists the cost $t_{ij} > 0$ to rent a canoe in village $A_i$ and return it in village $A_j$.
The costs are **arbitrary**-not linked to distance, travel time, or any other obvious factor (e.g. $t_{1,3}=4$, $t_{3,4}=16$, $t_{1,4}=15$, $t_{1,2}=7$, $t_{2,4}=3$).

Design a **bottom-up dynamic-programming algorithm** with running time $O(n^{2})$ that finds the minimum total rental cost to travel from $A_1$ to $A_n$.

**Mandatory steps**

1. **(50 %)** Prove that the problem has optimal substructure by deriving a recurrence relation for your algorithm. Explain every term and state the base cases and their values.
2. **(30 %)** *Only after finishing (1)*, describe your algorithm at a high level (or in pseudo-code).
3. **(20 %)** Analyse the time and space complexities of your algorithm as functions of $n$.


---

### Question 3

Describe how to modify your **Question 2** algorithm so that it also outputs the sequence of villages where you must return each rented canoe during the trip down the Azamonas River.
