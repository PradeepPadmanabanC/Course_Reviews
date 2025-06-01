
# 18.650 Statistics for Applications — Fall 2016  
**Problem Set 1**  
**Due**: Friday, Sep. 16 at 12 noon

---

## Problem 1: Convergence of random variables

1. For \( n \in \mathbb{N}^* \), let \( X_n \) be a random variable such that  
   \[
   \mathbb{P} \left( X_n = \frac{1}{n} \right) = 1 - \frac{1}{n^2}, \quad 
   \mathbb{P}(X_n = n) = \frac{1}{n^2}
   \]  
   Does \( X_n \) converge in probability? In \( L^2 \)?

2. Let \( (X_n)_{n \in \mathbb{N}^*} \) be a sequence of i.i.d. Bernoulli random variables with parameter \( p \in [0, 1] \). For \( n \in \mathbb{N}^* \), let  
   \[
   \bar{X}_n = \frac{1}{n} \sum_{i=1}^n X_i
   \]  
   a) What is the distribution of \( n \bar{X}_n \)?  
   b) Prove that \( \bar{X}_n \to p \) in \( L^2 \).

3. For \( n \in \mathbb{N}^* \), let \( X_n \sim \text{Poisson}(1/n) \).  
   a) Prove that \( X_n \xrightarrow{\mathbb{P}} 0 \).  
   b) Prove that \( nX_n \xrightarrow{\mathbb{P}} 0 \).

---

## Problem 2: True or False

For each statement below, state whether it is true or false. If false, provide a counterexample.

1. If \( X_n \xrightarrow{\text{a.s.}} X \) and \( Y_n \xrightarrow{\text{a.s.}} Y \), then  
   \[
   X_n + Y_n \xrightarrow{\text{a.s.}} X + Y
   \]

2. If \( X_n \xrightarrow{\mathbb{P}} X \) and \( Y_n \xrightarrow{\mathbb{P}} Y \), then  
   \[
   X_n + Y_n \xrightarrow{\mathbb{P}} X + Y
   \]

3. If \( X_n \xrightarrow{d} X \) and \( Y_n \xrightarrow{d} Y \), then  
   \[
   X_n + Y_n \xrightarrow{d} X + Y
   \]

4. Consider a coin with unknown head probability \( p \). After 100 tosses, 43 heads are observed.  
   The unknown parameter \( p \) lies in the interval \([0.33, 0.53]\) with 95% probability.

---

## Problem 3: A Confidence Interval for Bernoulli Random Variables

Let \( X_1, \dots, X_n \) be i.i.d. Bernoulli with unknown parameter \( p \in (0, 1) \), and let  
\[
\bar{X}_n = \frac{1}{n} \sum_{i=1}^n X_i
\]

1. Show that  
   \[
   \sqrt{n} \cdot \frac{\bar{X}_n - p}{\sqrt{p(1 - p)}} \xrightarrow{d} Z \sim \mathcal{N}(0, 1)
   \]

2. Prove that for all \( t > 0 \):  
   \[
   \mathbb{P}[|Z| \le t] = 2\mathbb{P}[Z \le t] - 1
   \]

3. For \( t > 0 \), let  
   \[
   I_t = \left[ \bar{X}_n - t \sqrt{\frac{p(1-p)}{n}}, \ \bar{X}_n + t \sqrt{\frac{p(1-p)}{n}} \right]
   \]  
   Show that  
   \[
   \mathbb{P}[p \in I_t] \to 2\Phi(t) - 1, \quad \text{as } n \to \infty
   \]  
   where \( \Phi \) is the standard normal CDF.

4. In practice, we want a small interval not depending on the unknown \( p \). Find \( t_0 \) such that the interval contains \( p \) with probability \( \to 95\% \) as \( n \to \infty \).  
   _Hint_: The 97.5%-quantile of standard normal is 1.96.

---

### Three Ways to Adjust the Interval \( I_{t_0} \)

5. **Conservative Method**  
   a) Prove:  
   \[
   p(1 - p) \le \frac{1}{4} \text{ for all } p \in (0, 1)
   \]  
   b) Use this to find interval \( J_1 \) around \( \bar{X}_n \) independent of \( p \), covering \( p \) with at least 95% probability for large \( n \).  
   c) If it's known \( p \le 0.3 \), can you find a smaller interval than \( J_1 \) still covering \( p \) with 95% confidence?

6. **Solving an Inequality**  
   a) Show: \( p \in I_{t_0} \) ⇔ a quadratic inequality in \( p \)  
   b) Solve it  
   c) Propose new interval \( J_2 \) not depending on \( p \), with coverage → 95%

7. Show: replacing \( p \) with \( \bar{X}_n \) in \( I_{t_0} \) gives interval \( J_3 \) covering \( p \) with probability → 95% as \( n \to \infty \)

8. **Election Forecast Example**  
   Sample \( n \) registered voters with replacement, ask about voting preference (Hillary or Donald). Let  
   - \( p \): true proportion voting Hillary  
   - \( \hat{p} \): proportion in the sample  

   a) If \( n = 10{,}000 \), \( \hat{p} = 0.7341 \), compute intervals \( J_1, J_2, J_3 \) and compare their lengths  
   b) Find minimal sample size \( n \) for an interval of length ≤ 0.05 (independent of \( p \)) that contains \( p \) with ≈ 95% confidence

---

*MIT OpenCourseWare*  
[https://ocw.mit.edu](https://ocw.mit.edu)  
[Terms of Use](https://ocw.mit.edu/terms)
