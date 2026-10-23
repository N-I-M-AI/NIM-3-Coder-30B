# NIM 3 - Coder - 30B

<p align="center">
  <img src="https://img.shields.io/badge/Architecture-Sparse_MoE-7928CA?style=for-the-badge&logo=cpu" alt="Architecture" />
  <img src="https://img.shields.io/badge/Total_Params-30.5B-0070F3?style=for-the-badge" alt="Total Params" />
  <img src="https://img.shields.io/badge/Active_Params-~3.0B-10B981?style=for-the-badge" alt="Active Params" />
  <img src="https://img.shields.io/badge/Quantization-Q4__K__M_GGUF-F5A623?style=for-the-badge" alt="Quantization" />
  <img src="https://img.shields.io/badge/License-Apache_2.0-blue?style=for-the-badge" alt="License" />
</p>

<p align="center">
  <b>Developed by NIM-AI</b><br>
  <i>A high-efficiency, deliberative Sparse Mixture-of-Experts (MoE) reasoning engine built for production software engineering and systems programming.</i>
</p>

---

## ⚡ Overview

**NIM 3 - Coder - 30B** delivers deep architectural reasoning and multi-language software engineering capabilities without the infrastructure overhead of massive monolithic models. 

By employing a fine-grained **Sparse Mixture-of-Experts (MoE)** architecture, the model dynamically routes token predictions through specialized expert pathways—activating only **~3 billion parameters per token** from its 30.5-billion-parameter capacity. This delivers the knowledge depth of a 30B-tier model at the execution latency and memory profile of a lightweight edge model.

### Key Capabilities
- **Chain-of-Thought (CoT) Deliberation:** Pre-conditions solutions with structured `<think>...</think>` traces to verify edge cases, time/space trade-offs, and state boundaries before emitting code.
- **Systems & Concurrency Specialization:** Trained for complex systems domains, including lock-free memory bounds, async runtimes, distributed consensus, and low-level networking.
- **Production-Ready Artifacts:** Shipped as an optimized standalone GGUF binary (`Q4_K_M`) for zero-dependency local orchestration via Ollama, `llama.cpp`, and LM Studio.

---

## 📊 Technical Specifications

| Parameter | Specification |
| :--- | :--- |
| **Total Parameters** | 30.5 Billion |
| **Active Parameters / Token** | ~3.0 Billion (Sparse Dynamic Routing) |
| **Quantization Format** | GGUF (`Q4_K_M`, ~18.6 GB) |
| **Context Window** | 4,096 tokens (native ChatML) |
| **Primary Target Stacks** | Rust, Go, C++, Python, TypeScript, Distributed SQL, Bash |
| **Primary Model Hub** | [Hugging Face (`NIM-AI/NIM-3-Coder-30B`)](https://huggingface.co/NIM-AI/NIM-3-Coder-30B) |

---

## 🚀 Quickstart & Inference

### 1. One-Command Run with Ollama
Launch NIM 3 - Coder directly from the Hugging Face hub without manual downloads:

```bash
ollama run hf.co/NIM-AI/NIM-3-Coder-30B:Q4_K_M

📁 Repository Structure
.
├── README.md                  # Model documentation & architecture overview
├── nim3.ipynb                 # End-to-end training, QLoRA distillation & GGUF export pipeline
├── generate_nim3_data.py      # Synthetic distillation dataset orchestrator
└── nim3_coder_distill.jsonl   # Curated reasoning dataset across complex systems topics

🛡️ License & Organization
Maintained by NIM-AI. Distributed under the permissive Apache 2.0 License for open research and commercial software automation.
