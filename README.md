# Assignment Template

This repository contains the starter code and infrastructure for the assignment. Follow the instructions below to set up your environment and submit your work.

## 1. Setup
- Install [uv](https://docs.astral.sh/uv/getting-started/installation/) (one-time setup). 

- Initialize your environment to download Python 3.10, install required libraries (NumPy, Matplotlib, SciPy, CasADi, CVXPY).

  ```sh
  git clone <REPO_URL> && cd <REPO>
  make setup      # runs `uv sync`
  source .venv/bin/activate
  ```

## 2. Solutions

The repository is organized into directories for each question. Each directory contains a `src/` folder where you must place your implementation.

**Authorized Modifications:**

- Files inside any `src/` directory.
- `config.yaml` within question directories.
  
> [!CAUTION] 
> **Locked Files**: Modifying scripts outside of `src/` (such as `main.py`, `visualizer.py`, or GitHub workflows) will trigger **Integrity Violations** (check [RULES](#rules) section). These violations will block your submission. You are advised to run `make validate` to verify the status.

## 3. Submission Workflow

1. **Verify Code Quality**: Run the linter to detect unused imports and logic errors.
    ```sh
    make check
    ```

2. **Auto-Fix Issues**: Auto-repair formatting and minor syntax mistakes.
    ```sh
    make fix
    ```

3. **Validate Rules**: Check against course constraints (line counts, file limits, and asset sizes).
    ```
    make validate
    ```

4. **Submit**: Stage and push your changes to the remote repository.
    ```sh
    git add .
    git commit -m "<COMMIT-MSG>"
    git push
    ```


## Rules

Your submission is auto-validated against the following constraints. Failure to meet these will result in a failed build on GitHub. 

- **Script Count**: Maximum of 5 Python scripts allowed per `src/` directory
- **Script Length**: Maximum of 500 lines of code per script
- **Integrity**: Modifications are forbidden outside `src/` (except `config.yaml`)
- **Assets**: PDF, Image, or Video files must NOT exceed 5 MB each

> [!Note]
> Bypassing local hooks with `--no-verify` will be caught and blocked by the GitHub Actions Compliance runner

