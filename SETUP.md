# Environment Setup & Usage

This guide explains how to set up the local development environment for this statistics repository using `uv` and how to run the provided notebooks.

---

## 🛠 Prerequisites

Ensure you have [uv](https://github.com/astral-sh/uv) installed on your system. If you haven't installed it yet, you can do so via Homebrew:
```bash
brew install uv
```

## 🚀 Environment Setup

This project uses **Python 3.11+** and a specific stack of data science libraries.

1. **Initialize the project:**
   ```bash
   uv init --python 3.11
   ```

2. **Create and sync the virtual environment:**
   ```bash
   uv venv
   uv sync
   ```

3. **Activate the environment:**
   ```bash
   source .venv/bin/activate
   ```

### Installed Packages
The environment includes the following core libraries:
* `jupyter` / `jupyterlab`
* `numpy`
* `scipy`
* `pandas`
* `matplotlib`
* `seaborn`
* `statsmodels`

---

## 📓 Running the Notebooks

You have two primary ways to work with the `.ipynb` files in this repository.

### Option 1: Jupyter Lab (Browser)
If you prefer the classic browser-based interface, run the following command in your terminal:

```bash
uv run jupyter lab
```
* **Access:** Click the `http://127.0.0.1:8888...` link generated in the terminal.
* **Kernel:** Ensure the kernel is set to **Python 3 (ipykernel)**.

### Option 2: VS Code (Recommended)
For an integrated experience, use VS Code's built-in Jupyter support:

1. Open this folder in VS Code.
2. Open any `.ipynb` file.
3. Click **Select Kernel** in the top right corner.
4. Select **Python Environments...** and choose the path pointing to `./venv/bin/python`.

---

## 🧹 Maintenance

To add new libraries to your environment:
```bash
uv add <package-name>
```

To remove the environment and start fresh:
```bash
rm -rf .venv
```
