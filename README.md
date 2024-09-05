# Central-Limit-Theorem-CLT-
Central Limit Theorem (CLT)- titanic dataset(test and train)

The **Central Limit Theorem (CLT)** is a fundamental principle in statistics that states that, given a sufficiently large sample size, the distribution of the sample means will approximate a normal distribution (bell curve), regardless of the shape of the original population distribution. This concept is central to many statistical practices, including hypothesis testing and confidence interval estimation.

### Key Points of the Central Limit Theorem:

1. **Sampling Distribution of the Mean**:
   - If you take a large number of random samples from a population and calculate the mean of each sample, the distribution of these sample means will form a normal (Gaussian) distribution, even if the population itself is not normally distributed.

2. **Conditions for the CLT**:
   - The sample size should be "sufficiently large." In practice, a sample size of 30 or more is often considered sufficient, though the required size can vary depending on the shape of the population distribution.
   - The samples must be independent of each other.

3. **Mean and Standard Deviation of the Sampling Distribution**:
   - The mean of the sampling distribution (mean of sample means) will be equal to the population mean (\(\mu\)).
   - The standard deviation of the sampling distribution (also known as the **standard error**) is given by:
   \[
   \text{Standard Error (SE)} = \frac{\sigma}{\sqrt{n}}
   \]
   where:
   - \(\sigma\) is the standard deviation of the population.
   - \(n\) is the sample size.

4. **Implications**:
   - The CLT allows us to make inferences about a population from a sample. For example, it justifies the use of the **z-test** and **t-test** for hypothesis testing when the sample size is large, even if the original data is not normally distributed.

### Example

Consider a population that is **uniformly distributed** between 0 and 1. If we repeatedly take random samples of size \(n = 30\) from this population and compute the mean of each sample, the distribution of these sample means will tend to be normally distributed.

```python
import numpy as np
import matplotlib.pyplot as plt

# Set seed for reproducibility
np.random.seed(0)

# Generate sample means from a uniform distribution
sample_means = [np.mean(np.random.uniform(0, 1, 30)) for _ in range(1000)]

# Plot the distribution of the sample means
plt.hist(sample_means, bins=30, edgecolor='k', density=True)
plt.title('Distribution of Sample Means (n=30)')
plt.xlabel('Sample Mean')
plt.ylabel('Density')
plt.show()
```

### Output

The histogram will show a bell-shaped curve, illustrating how the sample means follow a **normal distribution** due to the Central Limit Theorem, even though the original population is **uniformly distributed**.

### Summary

- The CLT is crucial because it enables statisticians to use the normal distribution as an approximation for various types of data.
- It forms the foundation for many statistical methods and tests used in hypothesis testing, confidence intervals, and regression analysis.
    
