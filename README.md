# Visualize Population, Sample and Variance

## I. Introduction

This website is created to illustrate and explain one of the core problems in statistics: **why do we divide by (n-1) instead of n when calculating sample variance?**

This project provides a visual and interactive experience to understand:

- The difference between **population** and **sample**
- The concept of **unbiased estimation** in statistics
- The mathematical reasoning behind using **degrees of freedom (n-1)** in the sample variance formula
- The impact of using sample mean instead of population mean

## II. Statistical Background

### Basic Problem

In applied statistics, we often encounter situations where:
- **Population**: The entire set of objects under study (e.g., 200,000 mice in a laboratory)
- **Sample**: A subset selected from the population (e.g., 5 randomly selected mice)

### Challenge in Estimation

When calculating variance from a sample to estimate population variance, using the simple formula:

```
Variance = (1/n) × Σ(xi - x̄)²
```

creates a **biased estimate** - tends to systematically underestimate the true value.

### Solution: Bessel's Correction

The correct formula for unbiased estimation:

```
s² = (1/(n-1)) × Σ(xi - x̄)²
```

Dividing by (n-1) instead of n is called **Bessel's correction**.

## III. Mathematical Principles

### Degrees of Freedom

- In a sample of n observations, initially there are n independent values
- When calculating sample mean x̄, we create one constraint
- Only (n-1) independent information about variation remains
- Therefore, we must divide by (n-1) to get an accurate estimate

### Optimal Property of Sample Mean

The sample mean x̄ has a special property:
- It minimizes the sum of squared deviations: `Σ(xi - z)²`
- Therefore: `Σ(xi - x̄)² ≤ Σ(xi - μ)²`
- This leads to systematic underestimation without correction

## IV. Purpose of This Website

This website helps users:

1. **Visualize** the difference between population and sample
2. **Experiment** with different sample sizes
3. **Compare** results from formulas dividing by n and n-1
4. **Understand** why Bessel's correction is necessary
5. **Apply** knowledge to practical research

## V. Features

- Generate populations with customizable parameters
- Random sampling with different sizes
- Visual display of data distribution
- Compare variance calculated by two methods
- Simulate multiple sampling to observe trends

## VI. References

Content developed based on:
- "Analysis of Population Mean, Sample Mean and Sample Variance Estimation Problems" by AIVietnam
- Basic inferential statistics theory and concepts of degrees of freedom and unbiased estimation

## VII. Usage

**Live Demo**: [https://quang2719.github.io/Visualize-Population-Sample-and-Variance/]

1. Open the website using the link above
2. Adjust population parameters
3. Perform sampling
4. Observe the difference between two variance calculation methods
5. Experiment with different sample sizes

