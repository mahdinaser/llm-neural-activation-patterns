# Neural Activation Patterns Across Language Model Architectures

This repository contains the complete dataset and analysis code for the paper:

**"Neural Activation Patterns Across Language Model Architectures: A Comprehensive Analysis of Cognitive Task Performance"**

## 📊 Dataset Overview

This repository provides comprehensive analysis of neural activation patterns across **six distinct large language model (LLM) architectures**, examining their performance on **twelve cognitive task categories**. Through systematic measurement of final activation values, attention entropy, and sparsity patterns, we reveal fundamental differences in how encoder and decoder architectures process diverse cognitive tasks.

### Key Findings

- **144 task-model combinations** analyzed across 6 architectures and 12 cognitive tasks
- **Mathematical reasoning** consistently produces the highest attention entropy (195.66 ± 46.66) across all architectures
- **Decoder models** exhibit significantly higher sparsity (0.276 average) compared to encoder models (0.039) - **7× difference**
- **GPT2-117M** dominates final activation metrics, occupying all top 10 positions
- **Non-monotonic relationships** between parameter scale and activation intensity challenge simple scaling assumptions

## 🗂️ Repository Structure

```
llm-neural-activation-patterns/
├── data/
│   ├── raw/                    # Original analysis data
│   │   ├── llm_brain_analysis_tables_20250803_232237.txt  # Complete results tables
│   │   ├── comprehensive_brain_analysis_results.xlsx
│   │   └── comprehensive_brain_analysis_tables.xlsx
│   └── processed/              # Cleaned and processed data
├── scripts/
│   └── brain.py               # LLM Brain Activity Analyzer framework
├── results/                   # Analysis results and outputs
├── figures/                   # Generated visualizations
├── paper/                     # Paper manuscript
└── README.md                  # This file
```

## 🧠 Model Architectures Analyzed

### Encoder Architecture
- **BERT-Base** (109.5M parameters): Bidirectional encoder-only architecture
  - Final Activation: -0.0130
  - Attention Entropy: 125.58
  - Max Sparsity: 0.0390

### Decoder Architectures
- **GPT2-117M** (124.4M parameters): Autoregressive decoder
  - Final Activation: 0.3281
  - Attention Entropy: 51.09
  - Max Sparsity: 0.0666

- **Qwen-1.5-0.5B** (464.0M parameters): Modern multilingual decoder
  - Final Activation: -0.0727
  - Attention Entropy: 69.24
  - Max Sparsity: 0.4224

- **Phi-1** (1.4B parameters): Efficiency-optimized decoder
  - Final Activation: 0.0009
  - Attention Entropy: 98.63
  - Max Sparsity: 0.2377

- **BLOOM-560M** (559.2M parameters): Multilingual autoregressive model
  - Final Activation: -1.8360
  - Attention Entropy: 61.93
  - Max Sparsity: 0.0358

- **StableLM-3B** (3.6B parameters): Large-scale decoder architecture
  - Final Activation: 0.0047
  - Attention Entropy: 106.43
  - Max Sparsity: 0.6161

## 🎯 Cognitive Task Categories

1. **Factual Questions**: Retrieval of encyclopedic knowledge
2. **Creative Writing**: Open-ended text generation requiring imagination
3. **Mathematical Reasoning**: Multi-step quantitative problem solving
4. **Emotional Content**: Sentiment analysis and emotional understanding
5. **Technical Code**: Programming and software engineering tasks
6. **Philosophical Queries**: Abstract reasoning about existence and ethics
7. **Conversational Chat**: Natural dialogue and social interaction
8. **Logical Puzzles**: Deductive and inductive reasoning challenges
9. **Scientific Explanations**: Domain-specific knowledge application
10. **Language Tasks**: Linguistic analysis and translation
11. **Instruction Following**: Task comprehension and execution
12. **Commonsense Reasoning**: Everyday knowledge application

## 📈 Key Metrics

### Final Activation (Af)
Mean activation magnitude of the final hidden layer, indicating processing intensity.

### Attention Entropy (Hatt)
Shannon entropy of attention weight distributions across all heads and layers, measuring computational complexity.

### Maximum Sparsity (Smax)
Peak sparsity level across all network layers, measuring computational efficiency.

## 🔬 Key Results

### Architecture Comparison (Table II)
- **Decoder Average**: Final Act. -0.315, Att. Entropy 77.47, Max Sparsity 0.276
- **Encoder (BERT)**: Final Act. -0.013, Att. Entropy 125.58, Max Sparsity 0.039

### Task-Specific Patterns (Table III)
- **Mathematical Reasoning**: Highest entropy (195.66 ± 46.66) across all architectures
- **Scientific Explanations**: Lowest entropy (47.03 ± 19.10), suggesting focused attention patterns
- **Technical Code**: High complexity (94.11 ± 35.08 entropy)
- **Logical Puzzles**: Second highest entropy (108.27 ± 44.75)

### Parameter Scale Effects (Table V)
- **Non-monotonic relationships**: BLOOM-560M shows most negative activation (-1.84)
- **StableLM-3B**: Highest sparsity (0.616), indicating efficient selective activation
- **Phi-1**: Remarkably low activation (0.0009), suggesting architectural optimization

### Top Performers
- **Final Activation**: GPT2-117M dominates all top 10 positions (0.3071 to 0.3740)
- **Attention Entropy**: Mathematical reasoning tasks occupy top 4 positions and 6 of top 10
- **Lowest Sparsity (Highest Density)**: BERT-Base and BLOOM-560M dominate, with mathematical reasoning requiring most comprehensive activation

## 📊 Data Files

### Primary Data File
- **llm_brain_analysis_tables_20250803_232237.txt**: Complete results with all tables matching the paper
  - Table 1: Complete Analysis Results (144 task-model combinations)
  - Table 2: Model Summary (6 models)
  - Table 3: Category Performance Across Models (12 cognitive tasks)

### Excel Files
- **comprehensive_brain_analysis_results.xlsx**: Complete results dataset
- **comprehensive_brain_analysis_tables.xlsx**: Formatted tables

## 🚀 Usage

### Loading the Data
```python
import pandas as pd

# The main data is in the text file with structured tables
# You can parse it or use the Excel files for easier access

# Load Excel results
results_df = pd.read_excel('data/raw/comprehensive_brain_analysis_results.xlsx')
tables_df = pd.read_excel('data/raw/comprehensive_brain_analysis_tables.xlsx')
```

### Key Statistics
```python
# Example: Calculate architecture averages
decoder_models = ['GPT2-117M', 'Qwen-1.5-0.5B', 'Phi-1', 'BLOOM-560M', 'StableLM-3B']
encoder_models = ['BERT-Base']

# Mathematical reasoning has highest entropy across all models
math_reasoning_entropy = 195.66  # Mean across all models
```

## 📋 Key Tables from Paper

### Table II: Architecture Comparison
- **Decoder**: Final Act. -0.315, Att. Entropy 77.47, Max Sparsity 0.276
- **Encoder**: Final Act. -0.013, Att. Entropy 125.58, Max Sparsity 0.039

### Table III: Category Performance
- **Mathematical Reasoning**: Highest entropy (195.66 ± 46.66)
- **Scientific Explanations**: Lowest entropy (47.03 ± 19.10)

### Table V: Parameter Scale Analysis
- Reveals non-monotonic relationships between size and activation

### Table VI: Complete Model Summary
- All 6 models with their complete statistics

## 🔗 Citation

If you use this dataset in your research, please cite:

```bibtex
@article{neural2024activation,
  title={Neural Activation Patterns Across Language Model Architectures: A Comprehensive Analysis of Cognitive Task Performance},
  journal={arXiv preprint},
  year={2024}
}
```

## 📄 License

This dataset is released under the MIT License. See LICENSE file for details.

## 🤝 Contributing

We welcome contributions to extend this analysis:
- Additional model architectures
- New cognitive task categories
- Extended activation metrics
- Cross-architecture optimization strategies

## 📞 Contact

For questions about this dataset, please open an issue in this repository.

## 🙏 Acknowledgments

Special thanks to:
- Hugging Face for the transformers library
- PyTorch team for the machine learning framework
- Open-source community for model availability

---

**This comprehensive analysis reveals fundamental differences in neural activation patterns across LLM architectures, providing critical insights for model selection and optimization in cognitive task applications.**