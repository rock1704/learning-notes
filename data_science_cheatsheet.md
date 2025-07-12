# Key Intuitions & Formulas for Data Science/Math Problems

## 1. Probability & Statistics

### **Expected Value (Discrete/Continuous)**  
- **Intuition**: Long-run average value of a random variable.  
- **Formula**:  
  - Discrete: \( E[X] = \sum x_i P(X = x_i) \)  
  - Continuous: \( E[X] = \int_{-\infty}^{\infty} x f(x) dx \)  
- **Linear Transform**: \( E[aX + b] = aE[X] + b \).

### **Variance**  
- **Intuition**: Measures spread around the mean.  
- **Formula**: \( \text{Var}(X) = E[X^2] - (E[X])^2 \).  
- **Linear Transform**: \( \text{Var}(aX + b) = a^2 \text{Var}(X) \).

### **Conditional Probability & Bayes’ Theorem**  
- **Intuition**: Updates probability given new evidence.  
- **Formula**:  
  \( P(A \mid B) = \frac{P(B \mid A) P(A)}{P(B)} \).  
- **Total Probability**:  
  \( P(B) = \sum P(B \mid A_i) P(A_i) \).

### **Binomial Distribution**  
- **Intuition**: Counts successes in \( n \) independent trials.  
- **Formula**:  
  \( P(X = k) = \binom{n}{k} p^k (1-p)^{n-k} \).  
- **Mean**: \( np \), **Variance**: \( np(1-p) \).

### **Independence of Events**  
- **Intuition**: \( A \) and \( B \) do not affect each other.  
- **Check**: \( P(A \cap B) = P(A) P(B) \).

---

## 2. Linear Algebra

### **Eigenvalues & Eigenvectors**  
- **Intuition**: Directions unchanged by matrix multiplication.  
- **Formula**: \( A\mathbf{v} = \lambda \mathbf{v} \).  
- **For \( A^k \)**: Eigenvalue becomes \( \lambda^k \).

### **Matrix Inverse**  
- **Intuition**: "Undoes" the matrix transformation.  
- **Property**: \( A^{-1}A = I \).  
- **Eigenvalues**: If \( \lambda \) is eigenvalue of \( A \), \( \lambda^{-1} \) is eigenvalue of \( A^{-1} \).

### **Rank & Null Space**  
- **Intuition**:  
  - **Rank**: Number of linearly independent rows/columns.  
  - **Null Space**: Solutions to \( A\mathbf{x} = \mathbf{0} \).  
- **Formula**: \( \text{Rank}(A) + \text{Nullity}(A) = n \) (for \( m \times n \) matrix).

### **Covariance Matrix**  
- **Intuition**: Captures pairwise feature variances/covariances.  
- **Size**: \( n \times n \) for \( n \) features.  
- **PCA**: Eigenvectors of covariance matrix are principal components.

---

## 3. Optimization & ML

### **Gradient Descent**  
- **Update Rule**:  
  \( x_{k+1} = x_k - \alpha \nabla f(x_k) \).  
- **Convergence Criteria**:  
  - \( \|\nabla f(x_k)\| < \epsilon \) (optimality).  
  - \( \|x_{k+1} - x_k\| < \epsilon \) (stopping condition).  

### **Logistic Regression**  
- **Sigmoid Function**:  
  \( \sigma(x) = \frac{1}{1 + e^{-x}} \).  
  - **Properties**:  
    - \( \sigma(x) \to 0 \) as \( x \to -\infty \).  
    - \( \sigma(x) \to 1 \) as \( x \to \infty \).  
    - \( \sigma'(x) = \sigma(x)(1 - \sigma(x)) > 0 \) (always increasing).  

### **k-Means Clustering**  
- **Centroids**: Mean of points in a cluster.  
- **Objective**: Minimize within-cluster variance.  

### **k-NN Algorithm**  
- **Larger \( k \)**: Smoother decision boundaries (reduces overfitting).  

---

## 4. Data Analysis

### **Confusion Matrix**  
- **Metrics**:  
  - Sensitivity: \( \frac{TP}{TP + FN} \).  
  - Specificity: \( \frac{TN}{TN + FP} \).  
- **Rows**: Predicted labels, **Columns**: True labels.  

### **Cross-Validation**  
- **k-Fold**: Divides data into \( k \) subsets; trains on \( k-1 \), validates on 1.  
- **LOOCV**: \( k = n \) (leave-one-out).  

### **PCA (Dimensionality Reduction)**  
- **Key Idea**: Projects data onto eigenvectors of covariance matrix (principal components).  

---

## Quick Tips

1. **Eigenvalues**:  
   - For \( A \) and \( A^{-1} \), eigenvalues are inverses.  
   - Symmetric matrices have real eigenvalues.  

2. **Probability**:  
   - Use Bayes’ Theorem when given conditional probabilities.  
   - Binomial: Count successes, Poisson: Count rare events.  

3. **Gradient Descent**:  
   - Small learning rate (\( \alpha \)) slows convergence; large \( \alpha \) may diverge.  

4. **Independence**:  
   - Check \( P(A \cap B) = P(A)P(B) \). If true, \( A \) and \( B \) are independent.  

---

**Save this as `cheatsheet.md` for quick reference!** 🚀