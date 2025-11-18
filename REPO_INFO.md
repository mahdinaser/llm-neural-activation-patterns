# Repository Information

## Repository Name
**`llm-neural-activation-patterns`**

## Short Description (GitHub)
**"Comprehensive analysis of neural activation patterns across 6 LLM architectures on 12 cognitive tasks - reveals mathematical reasoning has highest attention entropy (195.66) across all models"**

## Alternative Shorter Description
**"144 task-model combinations: neural activation analysis showing decoder models have 7× higher sparsity than encoders"**

## Paper Title
"Neural Activation Patterns Across Language Model Architectures: A Comprehensive Analysis of Cognitive Task Performance"

## ✅ Verified Data Location
- **Primary Data**: `/Users/mahdinaser/workspace/hobby/brain_llm/report/llm_brain_analysis_tables_20250803_232237.txt`
- **Analysis Script**: `/Users/mahdinaser/workspace/hobby/brain_analysis/brain.py`
- **Excel Files**: `/Users/mahdinaser/workspace/hobby/brain_analysis/comprehensive_brain_analysis_*.xlsx`

## ✅ Data Verification
The data has been verified to match the paper's tables:
- ✅ **Table II (Architecture Comparison)**: Decoder vs Encoder metrics match
- ✅ **Table III (Category Performance)**: Mathematical reasoning entropy (195.66 ± 46.66) matches
- ✅ **Table V (Parameter Scale)**: All 6 models with correct parameters and metrics
- ✅ **Table VI (Model Summary)**: All values verified:
  - BERT-Base: -0.0130, 125.58, 0.0390 ✓
  - GPT2-117M: 0.3281, 51.09, 0.0666 ✓
  - Qwen-1.5-0.5B: -0.0727, 69.24, 0.4224 ✓
  - Phi-1: 0.0009, 98.63, 0.2377 ✓
  - BLOOM-560M: -1.8360, 61.93, 0.0358 ✓
  - StableLM-3B: 0.0047, 106.43, 0.6161 ✓

## Key Statistics
- **6 LLM architectures** analyzed (BERT-Base, GPT2-117M, Qwen-1.5-0.5B, Phi-1, BLOOM-560M, StableLM-3B)
- **12 cognitive task categories** evaluated
- **144 task-model combinations** (6 models × 12 tasks × 2 samples)
- **3 neural activation metrics**: Final Activation, Attention Entropy, Max Sparsity

## Main Findings
1. Mathematical reasoning consistently produces highest attention entropy (195.66 ± 46.66)
2. Decoder models show 7× higher sparsity (0.276) than encoder models (0.039)
3. GPT2-117M dominates final activation metrics (all top 10 positions)
4. Non-monotonic relationships between parameter scale and activation intensity