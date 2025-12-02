**Purpose**

This file gives concise, repository-specific guidance to AI coding assistants so they can be immediately productive. The repo is a tiny learning workspace with a couple of small Python scripts and a notebook. Focus edits on minimal, well-scoped changes and ask the human for clarification on broader changes.

**Big Picture**

- **Project Type:** Learning/intro Python examples — small scripts and a Jupyter notebook (`exemplo.py`, `teste.py`, `exemplo2.ipynb`).
- **Primary intent:** Demonstrations of `print` and `input` and simple notebook cells. No service boundaries, no web or CI integrations discovered.

**How To Run Locally**

- **Run a script:** Use `python3 exemplo.py` or `python3 teste.py` from the project root.
- **Run notebook:** Start Jupyter with `jupyter notebook` or execute the notebook headlessly:

  ```bash
  jupyter nbconvert --to notebook --execute exemplo2.ipynb --inplace
  ```

**Repository Patterns & Conventions (discoverable)**

- **Single-file examples:** Each example is a standalone script. Make edits that preserve this isolation.
- **IO style:** Scripts use direct `print` and `input` calls (see `exemplo.py` and `teste.py`). Avoid changing to frameworks or introducing external deps unless requested.
- **Notebook usage:** Cells keep simple demonstrations (e.g., `print("Hellow World")`, expression `5+9`). Keep notebooks runnable and cell outputs deterministic where possible.

**When You Edit Code**

- Prefer minimal diffs: small, explicit edits to existing files rather than broad refactors.
- If adding functionality (helpers, tests, or packaging), propose the change and include a short set of runnable commands to validate.
- Do not add new heavy dependencies without asking the maintainer.

**Examples From This Repo**

- `exemplo.py` / `teste.py`: simple CLI interaction:

  ```python
  print("Hello world")
  idade = 38
  nome = input("Digite seu nome ")
  print(nome, idade)
  ```

- `exemplo2.ipynb`: contains a markdown title, a `print` cell and a cell with `5+9`. Keep added notebook cells consistent with the learning tone.

**What Not To Assume**

- No automated tests or CI configured — do not add CI config unless requested.
- No packaging or module layout expected — converting these scripts into packages is a proposal, not an automatic improvement.

**If You Need More Context**

- Ask the human which learning goal to prioritize (e.g., input handling, control flow examples, or notebook demos).
- For multi-file changes, request a short design note before implementation.

**Commit / PR Guidance**

- Keep commits small and focused (one behavior change per commit).
- In PR descriptions, include exact commands used to validate changes (e.g., `python3 exemplo.py` or `jupyter nbconvert --execute ...`).

If anything above is unclear or you'd like this adapted to a different workflow (tests, CI, packaging), tell me what to change and I will update this file.
