# Cognitive Agent with RLHF

An adaptive cognitive agent that combines memory, reasoning, and reinforcement learning from human feedback (RLHF).
The project compares a simple baseline agent with an advanced cognitive model to measure improvements in decision-making, context retention, and task performance.

---

# 📦 Project Structure

```
cognitive-agent-rlhf/
├─ README.md
├─ environment.yml
├─ requirements.txt
├─ Dockerfile
├─ Makefile
├─ CHECKLIST.md
├─ .gitignore
│
├─ configs/
│   ├─ baseline.yaml
│   └─ rlhf_experiment.yaml
│
├─ src/
│   ├─ data/loader.py
│   ├─ agents/
│   │   ├─ baseline_agent.py
│   │   └─ cognitive_agent.py
│   ├─ models/policy_network.py
│   ├─ rlhf/
│   │   ├─ reward_model.py
│   │   └─ trainer.py
│   ├─ utils/memory.py
│   ├─ utils/logger.py
│   ├─ train.py
│   ├─ evaluate.py
│   └─ app.py
│
├─ notebooks/
│   ├─ 01_data_exploration.ipynb
│   └─ 02_train_baseline.ipynb
│
├─ outputs/
│   ├─ models/
│   ├─ figures/
│   └─ feedback/
│
└─ docs/
```

---

# 🛠️ Installation

## Clone repo

```bash
git clone https://github.com/your-username/cognitive-agent-rlhf.git
cd cognitive-agent-rlhf
```

## Conda environment

```bash
conda env create -f environment.yml
conda activate cognitive-agent-rlhf
```

## Pip

```bash
pip install -r requirements.txt
```

---

# ⚙️ Usage

## Train Baseline Agent

```bash
python src/train.py --config configs/baseline.yaml
```

## Train Cognitive Agent with RLHF

```bash
python src/train.py --config configs/rlhf_experiment.yaml
```

## Evaluate Model

```bash
python src/evaluate.py --model outputs/models/best_model.pt
```

## Interactive Demo

```bash
python src/app.py
```

---

# 📊 Evaluation Metrics

* Task completion rate
* Decision quality (reward model score)
* Memory retention performance
* Latency
* Human preference scores

Plots automatically saved in:

```
outputs/figures/
```

---

# 📁 Notebooks

```
notebooks/
├─ 01_data_exploration.ipynb
└─ 02_train_baseline.ipynb
```

---

# 🔧 Config Files

```
configs/
├─ baseline.yaml
└─ rlhf_experiment.yaml
```

---

# 🧪 Makefile

```
env:
	conda env create -f environment.yml

train:
	python src/train.py --config configs/rlhf_experiment.yaml

eval:
	python src/evaluate.py --model outputs/models/best_model.pt

demo:
	python src/app.py
```

---

# 🐳 Dockerfile

```dockerfile
FROM python:3.10-slim

WORKDIR /app

COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

COPY . /app

CMD ["bash"]
```

---

# 📄 environment.yml

```yaml
name: cognitive-agent-rlhf
channels:
  - defaults
  - conda-forge
dependencies:
  - python=3.10
  - pip
  - numpy
  - pandas
  - scikit-learn
  - pytorch
  - matplotlib
  - jupyterlab
  - pip:
    - transformers
    - datasets
    - wandb
    - fastapi
    - uvicorn
```

---

# 📄 requirements.txt

```
numpy
pandas
scikit-learn
torch
transformers
datasets
matplotlib
wandb
fastapi
uvicorn
```

---

# 📄 .gitignore

```
__pycache__/
*.pyc
*.pyo
*.pyd

.venv/
.env
*.egg-info/

.ipynb_checkpoints/

outputs/models/
outputs/figures/
outputs/feedback/

.DS_Store
Thumbs.db
```

---

# ✔️ CHECKLIST.md

```
# Deliverable Checklist

## 1. Prototype
- [ ] Baseline agent implemented
- [ ] Cognitive agent implemented
- [ ] RLHF training loop functional
- [ ] End-to-end demo ready

## 2. Evaluation
- [ ] Metrics generated
- [ ] Baseline vs cognitive comparison
- [ ] Plots saved in outputs/figures
- [ ] Human feedback logs saved

## 3. Report
- [ ] Methodology complete
- [ ] Implementation documented
- [ ] Results + discussion written
- [ ] Ethics + reproducibility ready

## 4. Slides & Demo
- [ ] 10-slide presentation
- [ ] Demo script (2-3 min)
- [ ] Backup video stored
```

---

# 🧩 GitHub Issue Template (bug_report.md)

```
### Bug Summary
Describe the bug.

### Steps to Reproduce
1.
2.

### Expected Behaviour
### Actual Behaviour

### Environment
- OS:
- Python version:
- Commit:
```

---

# 🧩 GitHub Pull Request Template

```
## What this PR does
Explain changes.

## Why
Reason + linked issue number.

## Checklist
- [ ] Tested locally
- [ ] Documentation updated
- [ ] No breaking changes

## How to Test
Command to reproduce:
```

---

# 📄 License (MIT)

```
MIT License

Copyright (c) 2025
Khelifi Mohamed Yacine

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the “Software”), to deal
in the Software without restriction…

(full MIT license text)
```

---

# ✨ Author

**Khelifi Mohamed Yacine**
University of Exeter — 2025

---

# 🚀 Final Notes

This Markdown bundle contains:

✔ README
✔ Environment files
✔ Dockerfile
✔ Makefile
✔ Issue/PR templates
✔ Checklist
✔ Gitignore

Everything you need is here.
