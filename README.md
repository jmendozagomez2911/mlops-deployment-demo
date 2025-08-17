# MLOps Deployment Demo

Project created with MLOps-Template cookiecutter. For more info: [https://mlopsstudygroup.github.io/mlops-guide/](https://mlopsstudygroup.github.io/mlops-guide/)

---

## 📋 Requirements

* Python 3.12+
* pip
* DVC
* Access to IBM Cloud Object Storage
* Git
* (Optional) pre-commit

---

## 🚀 Project Setup (What We’ve Done So Far)

1. Installed Cookiecutter:
   `pip install cookiecutter`

2. Generated the project from the official template:
   `cookiecutter https://github.com/MLOPsStudyGroup/mlops-template.git`

3. Answered interactive questions (author, project name, model type, etc.)

4. The template was generated inside an extra folder ("MLOps Deployment Demo"). We moved its contents up to the project root for a clean structure.

5. Created a virtual environment:
   `python -m venv venv`

6. Activated the environment:

   * On Windows: `venv\Scripts\activate`
   * On macOS/Linux: `source venv/bin/activate`

7. Installed dependencies:
   `pip install -r requirements.txt`

8. Selected the correct Python interpreter in VS Code:
   Press `Ctrl + Shift + P` → "Python: Select Interpreter" → choose the one inside `venv`

9. Initialized Git and pushed to GitHub:

   * Initialized the local Git repo:
     `git init`
   * Verified that `.gitignore` (provided by the template) correctly excludes folders like `venv/`, `__pycache__/`, etc.
   * Made the initial commit:
     `git add .`
     `git commit -m "Initial commit: MLOps project generated with Cookiecutter"`
   * Created a new repository on GitHub (without initializing it with a README)
   * Connected the local repo to GitHub:
     `git remote add origin https://github.com/your-username/mlops-deployment-demo.git`
   * Pushed the code:
     `git branch -M main`
     `git push -u origin main`

## 🏃🏻 Running Project

### 🔑 Setup IBM Bucket Credentials for IBM COS

On macOS and Linux, set up your credentials in:

* `~/.aws/credentials`
* `~/.aws/config`

Although DVC uses the S3 protocol, it works seamlessly with IBM Object Storage.

Example:

```
[default]
aws_access_key_id = {Key ID}
aws_secret_access_key = {Access Key}
```

---

### ✅ Pre-commit Testing

1. Install pre-commit:
   `pip install pre-commit`

2. Install the Git hook:
   `pre-commit install`

Now, every time you commit, the rules defined in `.pre-commit-config.yaml` will run automatically.

Example:

```
$ git commit -m "Example commit"

black....................................................................Passed
pytest-check.............................................................Passed
```

---

### ⚗️ Using DVC

Download data from the DVC remote:

```
dvc pull
```

Reproduce the data pipeline:

```
dvc repro
```


# Commands
venv\Scripts\activate
mlflow ui
