# ⚡ Sparse Convolution Benchmarking with PyTorch  

This project demonstrates a **sparse convolution implementation** in Python 🐍 using **NumPy, SciPy, and PyTorch**.  
It compares a **pure Python sparse convolution algorithm** with **PyTorch’s optimized conv2d** and analyzes performance at different sparsity levels.  

---

## 🚀 Features  
- 🧮 Implements **Direct Sparse Algorithm** (ICLR ‘17 paper inspired)  
- 🔁 Converts filters into **sparse weight matrices**  
- 📊 Benchmarks execution times at **different sparsity levels**  
- ⚡ Compares with **PyTorch’s conv2d** performance  
- ✅ Verifies correctness of outputs against PyTorch  

---

## 📂 Project Structure  
- `sparse_convolution()` → Implements convolution using Python loops  
- `generate_sparse_weight()` → Builds sparse weight matrices  
- **Benchmarking results** included for:  
  - 50% sparsity → ~25s  
  - 90% sparsity → ~9s  
  - 100% sparsity → ~38ms  
  - PyTorch conv2d → ~4ms (constant)  

---

## 📊 Performance Overview  

| Sparsity Level | Python Sparse Convolution ⏱️ | PyTorch conv2d ⏱️ |
|----------------|-------------------------------|-------------------|
| 50%            | ~25 s                         | ~4 ms             |
| 90%            | ~9 s                          | ~4 ms             |
| 100%           | ~38 ms                        | ~4 ms             |

✅ Algorithm produces **correct results** (difference = 0.0)  
⚡ Huge speedup observed with **higher sparsity**  

---

## 🛠️ How to Run  

1. Install dependencies:  
```bash
pip install torch numpy scipy
# insurance
