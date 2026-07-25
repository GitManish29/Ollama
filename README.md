# Ollama

Check the demonstration of Ollama Base Model Gemma-3B Using Jupyter Notebook

<p align="center">
  <a href="https://shields.io/"><img alt="Build" src="https://img.shields.io/badge/build-passing-brightgreen?style=flat-square" /></a>
  <a href="https://about.codecov.io/"><img alt="Codecov" src="https://codecov.io/gh/GitManish29/Ollama/branch/main/graph/badge.svg" /></a>
  <a href="https://snyk.io/"><img alt="Snyk Security" src="https://img.shields.io/badge/security-snyk-blue?style=flat-square" /></a>
  <a href="./LICENSE"><img alt="License" src="https://img.shields.io/badge/license-GPL--3.0-blue?style=flat-square" /></a>
</p>

---

## 📋 Table of Contents

- [About](#about)
- [Installation](#installation)
- [Requirements](#requirements)
- [Usage](#usage)
- [Security & Quality](#security--quality)
- [Contributing](#contributing)
- [License](#license)

---

## About

This project demonstrates the **Ollama** base model **Gemma-3B** using Jupyter Notebook, providing an interactive environment for exploring and testing the model's capabilities. Fully compliant with security standards, licensing requirements, and industry best practices.

### Key Features

- ✅ Gemma-3B Model Integration
- ✅ Jupyter Notebook Environment
- ✅ Security Hardened
- ✅ CI/CD Pipeline with GitHub Actions
- ✅ Codecov Coverage Tracking
- ✅ Snyk Dependency Scanning
- ✅ GPL-3.0 Licensed

---

## Installation

### Prerequisites

- **Node.js** (v14 or higher)
- **npm** (v6 or higher)
- **Python** (v3.7 or higher)
- **Jupyter Notebook**
- **Ollama** (running locally)

### Quick Start

1. **Clone the repository:**
   ```bash
   git clone https://github.com/GitManish29/Ollama.git
   cd Ollama
   ```

2. **Install Node.js dependencies:**
   ```bash
   npm install
   ```

3. **Setup Python environment:**
   ```bash
   python -m venv venv
   source venv/bin/activate  # Windows: venv\Scripts\activate
   ```

4. **Install Python dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

5. **Start Jupyter Notebook:**
   ```bash
   jupyter notebook
   ```

6. **Access in browser:**
   - Navigate to `http://localhost:8888`
   - Open notebook file
   - Ensure Ollama is running: `ollama serve`

---

## Requirements

### Node.js Dependencies
- **badge-maker** ^5.5.0

### Python Dependencies

Key packages (see `requirements.txt`):
- **jupyter** >= 1.0.0
- **numpy** >= 1.21.0
- **pandas** >= 1.3.0
- **pytest** >= 7.0.0
- **black** >= 23.0.0

Install all:
```bash
pip install -r requirements.txt
```

---

## Usage

### Running the Notebook

```bash
# Start Ollama (in separate terminal)
ollama serve

# Start Jupyter
jupyter notebook

# Open http://localhost:8888 and run cells
```

### Example

```python
import requests

OLLAMA_HOST = "http://localhost:11434"

# Generate text with Gemma-3B
response = requests.post(
    f"{OLLAMA_HOST}/api/generate",
    json={
        "model": "gemma:3b",
        "prompt": "Explain machine learning",
        "stream": True
    }
)

for line in response.iter_lines():
    print(line.decode())
```

---

## Security & Quality

### 🛡️ Security Tools

**Snyk** - Vulnerability Scanning
- Automated dependency scanning
- CI/CD integration
- [Learn more](https://snyk.io/)

**GitHub Dependabot**
- Automated updates
- Security patches
- Pull request automation

### 📊 Code Quality

**Codecov** - Coverage Tracking
- 70% minimum coverage required
- Automated reporting
- [Learn more](https://about.codecov.io/)

**Linting**
- ESLint (JavaScript)
- Flake8/Pylint (Python)
- Black (Python formatter)

### 📜 Compliance

- **License**: GNU General Public License v3.0
- **Security Policy**: [SECURITY.md](./SECURITY.md)
- **Contributing**: [CONTRIBUTING.md](./CONTRIBUTING.md)

---

## CI/CD Pipeline

Automated workflows on every commit:

✅ **Tests**
- Node.js (v14, v16, v18)
- Python (3.8, 3.9, 3.10, 3.11)
- Coverage reporting

✅ **Security**
- npm audit
- Snyk scanning
- Python security checks

✅ **Quality**
- ESLint
- Flake8/Pylint
- Coverage enforcement

✅ **Schedules**
- Weekly dependency updates
- Security scans
- Health checks

---

## Contributing

We welcome contributions! See [CONTRIBUTING.md](./CONTRIBUTING.md) for guidelines.

### Quick Start
1. Fork the repository
2. Create feature branch: `git checkout -b feature/your-feature`
3. Make changes and commit
4. Push and submit Pull Request

---

## Project Structure

```
Ollama/
├── .github/workflows/      # CI/CD pipelines
├── .gitignore             # Git ignore rules
├── LICENSE                # GPL-3.0 License
├── README.md              # This file
├── SECURITY.md            # Security policy
├── CONTRIBUTING.md        # Contribution guidelines
├── PROJECT.md             # Project config
├── package.json           # Node.js deps
├── requirements.txt       # Python deps
└── notebooks/             # Jupyter notebooks
```

---

## Resources

- [Ollama Documentation](https://github.com/ollama/ollama)
- [Jupyter Documentation](https://jupyter.org/)
- [Security Policy](./SECURITY.md)
- [Contributing Guide](./CONTRIBUTING.md)
- [Project Config](./PROJECT.md)

---

## License

**GNU General Public License v3.0** - See [LICENSE](./LICENSE)

### Key Terms
- ✅ Free to use, modify, distribute
- ✅ Source code must be available
- ✅ Derivative works same license
- ℹ️ No warranty provided

---

## Quick Links

| Resource | Link |
|----------|------|
| Security | [SECURITY.md](./SECURITY.md) |
| Contributing | [CONTRIBUTING.md](./CONTRIBUTING.md) |
| Project Config | [PROJECT.md](./PROJECT.md) |
| Issues | [GitHub Issues](https://github.com/GitManish29/Ollama/issues) |
| Discussions | [GitHub Discussions](https://github.com/GitManish29/Ollama/discussions) |

---

**Author**: [@GitManish29](https://github.com/GitManish29)  
**Repository**: [GitManish29/Ollama](https://github.com/GitManish29/Ollama)  
**License**: GNU General Public License v3.0  
**Last Updated**: 2026-07-25  
**Status**: ✅ Production Ready
