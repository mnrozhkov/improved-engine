# Example for R&D repository structure

## Installation

```bash
python -m venv .venv
echo "PYTHONPATH=$PWD" >> .venv/bin/activate
source .venv/bin/activate
pip install -r requirements.txt
```

## Run

### 1 - Study `bio-1023`

> Example of workflow using Jupyter Notebooks & DVCLive

Workflow:
- Navigate to the study directory: `cd bio-1023`
- Run code in JN: `jupyter lab`
- Commit & push results with Git and DVC
  
### 2 - Study `gen-2024`

> Common DVC pipeline with multiple stages

```mermaid
graph TD;
    data --> train_rf["Random Forest"];
    data --> train_lr["Linear Regression"];
    train_rf --> evaluate;
    train_lr --> evaluate;
```

Workflow:
- Navigate to the study directory: `cd gen-2024`
- Run the pipeline: `dvc exp run`
- Commit & push results with Git and DVC
