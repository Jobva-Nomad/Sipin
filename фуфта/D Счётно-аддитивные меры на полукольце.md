Мера $m$ на полукольце называется счётно-фддитивным, если $\forall A, A_1, A_2,..., ...\in S,$ таких, что
$A = \bigsqcup^\infty_{i=1}m(A_i)$

#Лемма 
Длина являтся счётно-аддитивной мерой на полукольце интервалов вида $[\alpha, \beta)\  в \ R^n$ 
![[Pasted image 20240926103033.png]]
Доказательство приведём при $n=1$
$[\alpha; \beta) = \bigsqcup^\infty_{i=1} [\alpha_i;\beta_i)$
![[Pasted image 20240926103634.png]]
Доказательство основано на $m$ Бореля
$$(\alpha_i - \delta_i;\ \beta_i + \delta_i) \ \ \delta_i = \frac{\epsilon}{2^i}; \ \ \ i=1,2,... \ \ \ [\alpha; \beta] \subset \bigcup^\infty_{i=1}(\alpha_i - \delta_i; \ \beta_i + \delta_i)$$
$$] \ n: \ [\alpha;\beta] \subset \ \bigcup^n_{i=1}\  (\alpha_i - \delta_i; \ \beta_i + \delta_i)\subset \ \bigcup^n_{i=1}\  [\alpha_i - \delta_i; \ \beta_i + \delta_i) \ \ \ \ [\alpha;\beta) \subset  \ \bigcup^n_{i=1}\  [\alpha_i - \delta_i; \ \beta_i + \delta_i)$$
Заметим, что исходный интервал и объединение интервалов входят в кольцо, порождённое полукольцом.
На это кольцо мера продолжается однозначно

$$m([\alpha; \beta)) \subseteq m(\bigcup^n_{i=1}[\alpha_i - \delta_i; \ \beta_i + \delta_i))\leq \sum^n_{i=1}m([\alpha_i - \delta_i; \ \beta_i+\delta_i))= \sum^n_{i=1}((\beta_i - \alpha_i) + 2 \delta_i) \leq$$
$$\leq (\sum^n_{i=1} m([\alpha_i; \ \beta_i)) + (2\sum^\infty_{i=1} \delta_i) = 2 \epsilon ) \leq \sum^n_{i=1} m([\alpha_i; \ \beta_i)) + 2 \epsilon \ при \ \epsilon \ \rightarrow 0 $$
$$m([\alpha; \ \beta)) \leq \sum^n_{i=1} m([\alpha_i; \ \beta_i))$$
обратное неравенство получается из
$$[\alpha; \ \beta) \in R(S)\ \ \ \bigsqcup^n_{i=1} [\alpha_i; \ \beta_i) \in R(S) \ \ \ m(\bigsqcup^n_{i=1} [\alpha_i; \ \beta_i)) \leq m ([\alpha; \ \beta)) $$
$$\sum^n_{i=1}m[\alpha_i; \ \beta_i) \leq m ([\alpha; \ \beta) \ \ \ n \rightarrow \infty \text{ и получаем обратное неравенство}  $$
$$\sum^\infty_{i=1}m[\alpha_i; \ \beta_i) \leq m[\alpha; \ \beta) $$
--------

*****Продолжение меры счётно-аддитивной на полукольце с единицей ****

S - полукольцо множеств
E - единица кольца
$S \subset 2^E$
m - счётно-аддитивная мера на S
$m(S) < + \infty$ 
Введем понятие внешней меры

Внешняя мера определена для $\forall A \in 2^E$
$$\mu^*(A) = \inf_{\{ e_i \}^\infty \subset S} \sum^\infty_{i=1}m(e_i)$$
#свойства :

0) $\mu^*(A) \leq m(E) < +\infty\ \ таких, \ что \ A \subset \bigcup^\infty_{i=1}e_i$ 
1) $\mu^*(e) = m(e), \ если  \ e \in S$ 
2) Внешняя мера счётна полуаддитивна на системе всех подмножеств в множестве E
тоесть $\forall A,A_1,A_2,... \subset E$ таких, что $A \subseteq \bigcup^\infty_{i=1}A_i$
$\mu^*(A) \leq \sum^\infty_{i=1}\mu^*(A_i)$ предположим, что ряд сходится
$$\forall \epsilon >0 \ \ \exists N\  |\ \sum^\infty_{i=1}\mu^*(A_i) \leq \sum^n_{i=1}\mu^*(A_i) + \epsilon $$
В силу определения $\exists \{ e^{(i)}_j \}^\infty_{j=1} \subset S$
$$\mu^*(A_i) \leq \sum^\infty_{j=1}m(e^{(i)}_j) \leq \mu^*(A_i) + \frac{\epsilon}{2^i} \ \ \ \ $$
$$\sum^\infty_{i=1} \mu^*(A_i) \leq \sum^\infty_{i=1} \sum^\infty_{j=1} m (e^{(i)}_j) \leq \sum^\infty_{i=1} \mu^*(A_i) + \epsilon\ \  \ \ $$
$$A_i \subset \bigcup^\infty_{j=1}e^{(i)}_j \Rightarrow A \subset \bigcup^\infty_{i=1} A_i \subset \bigcup^\infty_{i=1} \ \bigcup^\infty_{j=1}e^{(i)}_j $$
$\{ e^{(i)}_j \}^{\infty \ \ \infty}_{i=1 \ \ j=1}$ - покрытие A множествами из S и оно счётно $\Rightarrow$ Внешняя мера A не превосходит сумм мер этого покрытия
$$\mu^*(A) \leq \sum^\infty_{i=1} \ \sum^\infty_{j=1} m(e^{(i)}_j) \leq \sum^\infty_{i=1} \mu^*(A_i) + \epsilon$$
осталось $\epsilon \rightarrow 0$ и получится требуемое неравенство

#Лемма $\forall A, B \subset E$
$$|\mu^*(A) - \mu^*(B)| \leq \mu^*(A \ \triangle \ B)$$
Докажем на основании свойства полуаддитивности:
$A = B \sqcup A \setminus B \ \Rightarrow \mu^*(A) \subseteq \mu^*(B) + \mu^*(A \setminus B) \leq \mu^*(B) + \mu^*(A \triangle B)$
$B = A \sqcup B \setminus A \ \Rightarrow \mu^*(B) \subseteq \mu^*(A) + \mu^*(B \setminus A) \leq \mu^*(A) + \mu^*(B \triangle A)$

лемма доказана

#Лемма $] A_1, A_2, B_1, B_2 \subset E$

$\mu^*((A_1 \cup A_2)\triangle(B_1 \cup B_2)) \leq \mu^*(A_1 \triangle B_1) + \mu^*(A_2 \triangle B_2)$
проверим, что $(A_1 \cup A_2) \triangle (B_1 \cup B_2) \subset \mu^*(A_1 \triangle B_1) + \mu^*(A_2 \triangle B_2)$ 
если элемент попал в $A_1$ то и в $A_1 \triangle B_1$ 

#Лемма $\forall A_1, A_2, B_1, B_2 \subset E$
$\mu^*((A_1 \cap A_2)\triangle(B_1 \cap B_2)) \leq \mu^*(A_1 \triangle B_1) + \mu^*(A_2 \triangle B_2)$

всё тоже самое 
для ряда $(A_1 \setminus A_2) \triangle (B_1 \setminus B_2) \leq (A_1 \triangle B_1) \cap (A_2 \triangle B_2)$
такого нет, для разности не работает

Для продолжения меры 
Будем расширять класс $S$ некоторыми новыми множествами, которые будем называть измеримыми
#определение $A\subset E$ называется **измеримым**, если $\forall \epsilon > 0 \ \ \ \exists B \in R(S): \mu^*(A \triangle B)<\epsilon$
$\mu^*(A \triangle B) = \rho(A,B)$ - обладает всеми свойствами метрики, кроме свойства : $\rho(A,B) = 0 \Rightarrow A =B$ 

1) $\rho(A,B) = \rho(B,A)$
2) $\rho(A,B) \leq \rho(A,C) + \rho(C, B)$

Пусть $\mathfrak{A}$ - система измеримых множеств, покажем, что $\mathfrak{A}$ содержит полукольцо и измеримые множества образуют ?алгебру?

#теорема Измеримые множества образуют ?алгебру? и $S \subset \mathfrak{A}$
	        замкнутость относительно объединений

$]A, B$ - измеримы
$\forall \epsilon > 0 \ \exists \cases{A_1 \in R(S) \\ B_1 \in R(S)}$  такие, что $\cases{\mu^*(A \triangle A_1) \leq \frac{\epsilon}{2}\\ \mu^*(B \triangle B_1) \leq \frac{\epsilon}{2}}$

$A_1 \cup B_1$ - кандидат
$\mu^*((A \cup B)\triangle (A_1 \cup B_1)) \leq \mu^*(A \triangle A_1) + \mu^*(B \triangle B_1) < \epsilon$

замкнутость относительно пересечений основаано на лемме выше(первая что будет выше)
докажем замкнутость относительно дополнений

пусть $A \in \mathfrak{A}$, тогда $A^c \in \mathfrak{A}$
$\forall \epsilon > 0 \ \ \exists A_1 \in R(S) \ \ \ \ \mu^*(A \triangle A_1) \leq \epsilon$ ![[Pasted image 20240928201835.png]]
$A^C \triangle A^C_1 = A \triangle A_1 \Rightarrow \mu^*(A^C \triangle A^C_1) \leq \epsilon$
$A^C_1 \in R(S)$ так как кольцо замкнуто относительно дополнений 

$A \setminus B = A \cap B^C$ 

A и B - измеримы
