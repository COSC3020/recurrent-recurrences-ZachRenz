[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/8KYthzwp)
# Recurrent Recurrences

Give big $\Theta$ bounds for the following recurrence relations.

1.
$$ T(n) =
    \begin{cases}
        1 & n \leq 1\\
        T\left(\frac{n}{13}\right) + 5 & n > 1
    \end{cases}
$$

$T(n/13) = T(n/13/13) + 5 \Rightarrow T(n/13^2) + 5$ </br>
$T(n/13^2) + 5 + 5 \Rightarrow T(n/13^2) + 10$ </br>
$T(n/13) = T(n/13^3) + 10$ </br>
$T(n/13^3) + 10 + 5 \Rightarrow T(n/13^3) + 15$ or $T(n/13^i) + 5i$ </br>
Let $i = log_{13}n$ </br>
$T(n/n) + 5log_{13}n \Rightarrow T(n) \in \Theta(5logn)$

2.
$$ T(n) =
    \begin{cases}
        1 & n \leq 1\\
        13 T\left(\frac{n}{13}\right) + 5 & n > 1
    \end{cases}
$$

$T(n/13) = 13T(n/13/13) + 5 \Rightarrow 13T(n/13^2) + 5$ </br>
$13(13T(n/13^2) + 5) + 5 \Rightarrow 13^2T(n/13^2) + 65 + 5$ </br>
$T(n/13) = 13^2T(n/13^3) + 70$ </br>
$13(13^2T(n/13^3 + 70) + 5 \Rightarrow 13^3T(n/13^3) + 915$ or $13^iT(n/13^i) + C$ </br>
Let $i = log_{13}n$ </br>
$nT(n/n) + C \Rightarrow T(n) \in \Theta(n)$

3.
$$ T(n) =
    \begin{cases}
        1 & n \leq 1\\
        13 T\left(\frac{n}{13}\right) + 2n & n > 1
    \end{cases}
$$
