---
abstract: |
  In a room of 23 people, the chance that at least two share a birthday is just over one half. This note derives the result, explains why intuition underestimates it, and gives the group sizes at which the probability crosses common thresholds.
---

# Shared birthdays in small rooms

## The question

How many people must be in a room before it is more likely than not that two of them share a birthday? Most people guess a number in the hundreds. The answer is 23 [@feller1968].

## The calculation

Assume 365 equally likely birthdays and ignore leap years. The probability that $n$ people all have different birthdays is

```{math}
:label: eq-distinct
\bar{p}(n) = \prod_{k=0}^{n-1} \frac{365 - k}{365},
```

and the probability of at least one shared birthday is $p(n) = 1 - \bar{p}(n)$. Evaluating [](#eq-distinct) gives $p(23) \approx 0.507$.

## Why it surprises

Intuition compares each person with oneself, which gives only $n - 1$ chances. The relevant count is the number of pairs, $n(n-1)/2$, which is already 253 for 23 people. Each pair matches with probability $1/365$, so the expected number of matching pairs is about 0.69.

| Group size | Probability of a shared birthday |
|---|---|
| 10 | 0.117 |
| 23 | 0.507 |
| 30 | 0.706 |
| 50 | 0.970 |
| 70 | 0.999 |

## Conclusion

Coincidences that seem unlikely for any one person become likely across a group, because the number of pairs grows with the square of the group size.
