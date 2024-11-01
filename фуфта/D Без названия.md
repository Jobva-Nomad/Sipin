$S$ - полукольцо
$A$ - измеримо, если $(\forall \epsilon > 0)(\exists B \in R(S) )(\mu^*(A \ \triangle \  B) \leq \epsilon)$ 

#теорема 3 Внешняя мера является мерой на алгебре $\mathfrak{A}$ измеримых множеств. 
$\forall A \in \mathfrak{A} \ \ \ \ \mu^*(A) \geq 0$ 
----

---
$(\forall \epsilon > 0)(\exists B_1, B_2 \in R(S))\cases{\mu^*(A_1 \ \triangle \ B_1) < \epsilon \\ \mu^*(A_2 \ \triangle \ B_2) < \epsilon}$ 
$| \ \mu^*(A_1) - \mu^*(B_1) \ | \leq \mu^*(A_1 \ \triangle \ B_1) \leq \epsilon$
$| \ \mu^*(A_1) - \mu^*(B_1) \ | \leq \epsilon$ 
$\mu^*(A_1) + \mu^*(A_2) \leq \mu^*(B_1) + \mu^*(B_2) + 2 \epsilon = m(B_1) + m(B_2) + 2\epsilon  = m(B_1 \cup B_2) + m(B_1 \cap B_2) + 2 \epsilon$
$\mu^*(B_1 \cup B_2) + \mu^*(B_1 \cap B_2) +2 \epsilon \leq \mu^*(A_1 \cup A_2) + 2 \epsilon + \mu^*(A_1 \cap A_2)[= \emptyset] +2\epsilon + 2 \epsilon$

Получаем неравенство:
$\mu^*(A_1) + \mu^*(A_2) \leq \mu^*(A_1 \sqcup A_2) + 6 \epsilon$
$\mu^*(A_1 \sqcup A_2) \leq \mu^*(A_1) + \mu^*(A_2)$ (полуаддиттивность)

Итог:
$| \ \mu^*(A_1 \sqcup A_2) - (\mu^*(A_1) + \mu^*(A_2)) \ | \leq 6 \epsilon$

При $\epsilon \rightarrow 0: \ \  \mu^*(A_1 \sqcup A_2) = \mu^*(A_1) + \mu^*(A_2)$

#теорема 4 Внешняя мера счётного аддитивна на алгебре измеримых множеств

$] \ A, A_1, A_2, ...,$ - измеримые множества $\in \mathfrak{A}$
$A_i \cap A_j = 0$ при $i \neq j$ и $\bigsqcup^\infty_{i=1}A_i$

Рассмотрим конечную сумму $\bigsqcup^n_{i=1}A_i \subset A$
$\mu^*( \bigsqcup^n_{i=1}A_i) \leq \mu^*(A)$
$\sum^n_{i=1}\mu^*(A_i) \leq \mu^*(A)$
$\sum^\infty_{i=1} \mu^*(A_i) \leq \mu^*(A)$

С другой стороны $\mu^*(A) \leq \sum^\infty_{i=1}\mu^*(A_i)$ по счётной полуаддитивности

!Измеримые множества образуют $\sigma$ - алгебру!

$] A_i \in \mathfrak{A}$ , тогда $A = \bigcup^\infty_{i=1}A_i \in^? \mathfrak{A}$ 
$A = \bigsqcup^\infty_{i=1} C_i$ ,где $C_i = A_i \backslash \bigcup^{i=1}_{j=1} A_j$ 
$C_i \in \mathfrak{A}$ (Замкнуто относительно операций)
$\bigsqcup^n_{i=1}C_i \subset A$

$\mu^* (\bigsqcup^n_{i=1}C_i) \leq \mu^*(A) < + \infty \Rightarrow \sum^\infty_{i=1} \mu^* (C_i) < +\infty$
$\forall \epsilon > 0 \ \ \ \exists n: \sum^\infty_{i=n+1}\mu^*(C_i)< \frac{\epsilon}{2}$ (Остаток ряда)

$A = \bigsqcup^n_{i=1}C_i(\in \mathfrak{A}) \sqcup \bigsqcup^\infty_{i=n+1}C_i$
$\exists B \in R(S): \mu^*((\bigsqcup^n_{i=1}C_i) \ \triangle \ B) < \frac{\epsilon}{2}$ по определению измеримого множества
$\mu^*(A) \leq \mu^*(\bigsqcup^n_{i=1}C_i) + \sum^\infty_{i=n+1} \mu^*(C_i)$ по счётной полуаддитивности
$A \ \triangle \ B \subset (\bigsqcup^n_{i=1}C_i \ \triangle \ B) \cup \bigsqcup^\infty_{i=n+1}C_i$
$\mu^(A \ \triangle \ B) \leq \mu^*(\bigsqcup^n_{i=1}C_i \ \triangle \ B) + \sum^{\infty}_{i=n+1}\mu^*(C_i) < \frac{\epsilon}{2} + \frac{\epsilon}{2} = \epsilon$

Множество $B$ апроксимирует множество $A$ с требуемой точность 

$!\mu(A) = \mu^*(A)!$ - счётно аддитивная мера на $\sigma-$ алгебре $\mathfrak{A} \supset S \ and \ (\forall A \in S)(\mu(A) = m(A))$

#Пример 1 Меры Лебега на отрезке
$[a; \ b]$ - конечный отрезок на $R^1$
$S = \{ <\alpha; \ \beta> | a \leq \alpha, \ \beta \leq b \}$
$l(<\alpha; \ \beta>) = \beta - \alpha$
$\beta \geq \alpha$
при $\beta < \alpha \ \ \ \ \ <\alpha; \ \beta> = \emptyset \ \ \ and \ \ \ l(<\alpha; \ \beta>) = 0$
$l$ счётно-аддитивно на $S$

Мы можем продолжить $l$ на $\sigma$- алгебру измеримых множеств. Получившиеся при этом счётно фддитивная мера над мерой Лебега (Обозначения):
$\lambda -$ мера Лебега
$\mathfrak{A} -$ измеримые подмножества отрезка $[a; \ b]$
$\mathfrak{A} - \sigma-$ алгебра
$S \subset \mathfrak{A} \Rightarrow \sigma(S) \subset \mathfrak{A}$
$\sigma(S) = B([a; \ b])$ - Борелевская $\sigma$ алгебра порождённа открытыми множествами

Замкнутые множества тоже будут измеримы. Аналогичная конструкция может выполняться и в пространстве $R^n$:
$[a; \ b] \subset R^n$ - n - мерный параллелелепипед, $\lambda^n$ - мера Лебега в нём

**(2) Мера Лебега - Стилтьеса
$] \  F(x) -$ неубывающая непрерывная слева функция + она ограничена на числовой прямой 

тогда $\cases{F(+ \infty) = \lim_{x \rightarrow + \infty}F(x) \\ F(- \infty) = \lim_{x \rightarrow - \infty}F(x) \\}$  (Можем определить эту функцию в точках $+ \ \infty$ и $- \ \infty$)
$S -$ полкуольцо интервалов вида $[\alpha; \ \beta)$ $(- \ \infty \leq \alpha \leq \beta \leq + \ \infty )$ 
$m_F([\alpha; \ \beta)) = F(\beta) - F(\alpha)$ 

Докажем, что $m_F$ - мера на $S$. 
Пусть $A, A_1, A_2, ... ,A_n \in S$
$A_i \cap A_j = \emptyset$    $[\alpha; \ \beta) = \bigsqcup^n_{i=1}[\alpha_i; \ \beta_i)$  и пусть $\alpha = \alpha_1 < \beta_1 = \alpha_2 < \beta_2 = ... < \beta_{n-1} = \alpha_n < \beta_n = \beta$ 
$m_F ([\alpha; \ \beta)) = F(\beta) - F(\alpha ) = F(\beta_n) - F(\alpha_n)[= \beta_{n-1}] + F(\alpha_n) - F(\alpha) = m_F([\alpha_n; \ \beta_n))+m_F([\beta_{n-1}; \ \alpha))=...$
$... = m_F([\alpha_n; \ \beta)) + m_F([\alpha_{n-1}; \ \beta_{n-1})) +... + m_F([\alpha_1; \ \beta_1))$

Нужно доказать счётную аддитивность этой меры на полукольце, но мы этого делать не будем.
Её можно продолжить по Лебегу. Получившееся продолжение обозначается $\mu_F$. Оно заведомо определено на Борелевской $\sigma -$ алгбре.

!!! Если F является функцией распределения какой-либо случайной величины, то сужение меры $\mu_F$ на Борелевскую $\sigma -$ алгебру совпадает с распределением этой случайной величины

! Всякая функция, обладающая свойствами (1) - (5) позволяет построить меру Лебега - Стилтьеса на Борелевских подмножествах числовой прямой.

Рассмотрим теперь вероятностное пространство $(R^1, \ B(R^1), \ \mu_F)$

$\zeta(w) = w$,     $w \in R^1$ 
$P(\{ \zeta < x \}) = P([- \ \infty; \ x)) = \mu_F([- \ \infty; \ x)) = F(x) - F(- \ \infty) = F(x) - 0 = F(x)$ 