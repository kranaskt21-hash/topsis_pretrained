# 📊 Pretrained Text Generation Model Selection using TOPSIS

## 📌 Objective
The objective of this project is to evaluate multiple pretrained text generation models 
from Hugging Face and select the best model using the TOPSIS (Technique for Order Preference 
by Similarity to Ideal Solution) method.

---

## 🤖 Models Evaluated
The following pretrained models were evaluated:

1. GPT-2  
2. DistilGPT-2  
3. GPT-Neo 125M  
4. GPT-Neo 1.3B  
5. GPT-Neo 2.7B

---

## 🧪 Evaluation Criteria

The models were evaluated based on the following criteria:

| Criteria        | Type     | Description |
|-----------------|----------|------------|
| Generation Time | Cost     | Time taken to generate output |
| Output Length   | Benefit  | Number of words generated |
| Repetition      | Cost     | Redundancy in generated text |
| Model Size      | Cost     | Approximate model size (MB) |

---

## ⚖️ Weights Assigned

| Criteria        | Weight |
|-----------------|--------|
| Time            | 0.3    |
| Length          | 0.2    |
| Repetition      | 0.3    |
| Size            | 0.2    |

---

## 📊 Decision Matrix

| Model | Time | Length | Repetition | Size |
|-------|------|--------|------------|------|
| GPT-Neo 125M      | 12.626682    | 201    |  82  | 520   |
| DistilGPT-2      | 8.976235| 140| 114| 250|
| GPT-2    | 12.558358    | 224 | 106 | 500 |
| GPT-Neo 1.3B       | 84.722383| 212   | 66 | 5000|
| GPT-Neo 2.7B    | 179.609851| 215 | 71| 10000|

---

## 🧮 TOPSIS Methodology

The following steps were applied:

1. Constructed Decision Matrix  
2. Normalized the matrix  
3. Applied weights  
4. Determined ideal best and ideal worst  
5. Calculated separation distances  
6. Computed TOPSIS score  

Formula used:

Cᵢ = S⁻ / (S⁺ + S⁻)

Where:
- S⁺ = Distance from ideal best
- S⁻ = Distance from ideal worst

---

## 📈 Results

Best Model Selected:

**Model Name:** GPT-Neo 125M  
**TOPSIS Score:** 0.892513 

Dataset Used: Custom Prompt

---

## 📊 Ranking Graph

<img width="454" height="458" alt="image" src="https://github.com/user-attachments/assets/9f818b48-ba0b-4daf-8458-23fd6d8e6f3e" />


---

## 🏆 Conclusion

Based on the multi-criteria decision analysis using TOPSIS, 
**GPT-Neo 125M** was found to be the most suitable pretrained 
text generation model among the evaluated alternatives.

The selection balances efficiency, quality, and model complexity.

---

## 🧠 Tools & Libraries Used

- Python
- Hugging Face Transformers
- PyDecision
- NumPy
- Pandas
- Matplotlib
- Kaggle Notebook
