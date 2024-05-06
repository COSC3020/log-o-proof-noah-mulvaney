[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/fbkbKZ5N)
# Asymptotic Equivalences

In the lectures, we said that logarithms with different bases don't affect the
asymptotic complexity of an algorithm. Prove that $O(\log_{2} n)$ is the same as
$O(\log_{5} n)$. Use the mathematical definition of $O$ -- do a formal proof,
not just the intuition.

$T(n) \in O(g(n)) \iff (\exists c)(\exists n_0) T(n) \leq c g(n) (\forall n \geq n_0)$  
$f(n) \in O(\log_2 n) \iff (\exists c)(\exists n_0)(\forall n \geq n_0) f(n) \leq c \log_2 n$  
$\log_m n = \frac{\ln n}{\ln m}$  
$\alpha := \frac{c}{\ln 2} \qquad f(n) \in O(\log_2 n) \iff (\exists n_0)(\forall n \geq n_0) f(n) \leq \alpha\ln n$  
$f(m) \in O(\log_5 m) \iff (\exists c)(\exists m_0)(\forall m \geq m_0) f(m) \leq c \log_5 m$  
$\beta := \frac{c}{\ln 5} \qquad f(m) \in O(\log_2 m) \iff (\exists m_0)(\forall m \geq m_0) f(m) \leq \beta \ln m$  
$(\exists n_0)(\forall n \geq n_0) f(n) \leq \alpha \ln n \equiv (\exists m_0)(\forall m \geq m_0) f(m) \leq \beta \ln m$  
$\therefore f(n) \in O(\log_2 n) \iff f(n) \in O(\log_5 n)$

If $f(n) \leq c \log_2 n$, then $f(n) \leq c \frac{\ln n}{\ln 2}$. This can be rewritten as $f(n) \leq \frac{c}{\ln2} \ln2$. Because $f(n) \leq c\log_2n$, a non-negative real number $c$ exists. Therefore $\alpha = \frac{c}{\ln2}$ also exists and is a non-negative real number. Likewise, $\beta = \frac{c}{\ln5}$ exists such that $f(m) \leq \beta \ln m$. Because both $\alpha$ and $\beta$ exist and are non-negative, $f(n) \in O(\log_2n) \iff O(\log_5n)$ since $f(n) \leq \alpha\ln n \equiv f(m) \leq \beta \ln m$ for some $n_0$ and $m_0$.
