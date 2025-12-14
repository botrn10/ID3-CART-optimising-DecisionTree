# Introduction

This project implements a **hybrid decision tree model** that combines the strengths of the **ID3** and **CART** algorithms to optimize decision tree performance.  
The proposed approach is applied to the **Social_Media_vs_Productivity** dataset to analyze the relationship between social media usage and productivity.

ID3 uses entropy and information gain to select splits, while CART relies on the Gini impurity measure. By integrating both criteria through a weighted mechanism, the hybrid model aims to improve classification accuracy, robustness, and overall tree quality.

---

# Dataset Description

- Dataset name: Social_Media_vs_Productivity
- Data type: Structured tabular dataset
- Domain: Social media usage and productivity analysis
- Target variable: actual_productivity_score (after processing)

The dataset is preprocessed prior to model training, including encoding categorical variables and splitting the data into training and testing sets.

---

# Model and Methodology

- Base algorithms:
  - ID3 (Entropy and Information Gain)
  - CART (Gini Index)
- Proposed approach:
  - Hybrid weighted decision tree model
- Key techniques:
  - Feature selection using entropy and Gini impurity
  - Weighted combination of split criteria
  - Recursive tree construction
- Optimization objective:
  - Improve classification accuracy and model stability

---

# Model Description

At each decision node, the model evaluates candidate splits using both **entropy-based information gain** and **Gini impurity**.  
These two measures are then combined using a weighting factor to determine the optimal split.

This hybrid strategy leverages:

- The sensitivity of ID3 to information gain
- The robustness and simplicity of CART

As a result, the split evaluation is performed using a weighted combination of ID3 and CART criteria controlled by the parameter alpha. Due to visualization limitations in scikit-learn, the final results are presented as two separate decision trees, although the split selection process is jointly influenced by both methods.

---

# Technologies Used

- Programming Language: Python
- Development Environment: Jupyter Notebook
- Libraries:
  - NumPy
  - Pandas
  - Scikit-learn
  - Matplotlib

---

# Installation and Requirements

Ensure that Python version 3.8 or higher is installed.

Install the required libraries using the following command:

```bash
pip install numpy pandas scikit-learn matplotlib
```

---

## How to Run

1. Open the project folder in **Visual Studio Code** or **Jupyter Notebook**.
2. Open the file `Hybrid-Weighted-alpha.ipynb`.
3. Run all cells sequentially to:
   - Load and preprocess the dataset
   - Train the hybrid decision tree model
   - Evaluate model performance
4. Review the results and visualizations generated in the notebook.

---

## Output Description

- Trained hybrid decision tree model
- Classification accuracy on both training and testing datasets
- Decision tree visualizations
- Performance comparison between ID3, CART, and the hybrid model

---

## Evaluation Metrics

- Accuracy
- F1-score
- Precision
- Recall
- Depth & nodes
- Confusion matrix
- Classification report

These metrics are used to assess the effectiveness of the proposed hybrid decision tree approach.

---

## Learning Outcomes

Through this project, the following outcomes were achieved:

- Implementation and understanding of ID3 and CART decision tree algorithms
- Design of a hybrid model combining multiple split criteria
- Application of decision tree learning to a real-world dataset
- Performance evaluation and comparison of different decision tree methods
