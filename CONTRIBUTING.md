# Contributing to Customer Segmentation Analysis

Thank you for your interest in contributing to the Istanbul Shopping Customer Segmentation Analysis project! This document provides guidelines and instructions for contributing.

## 🎯 How Can You Contribute?

There are many ways to contribute to this project:

- 🐛 **Report bugs** - Help us identify issues
- 💡 **Suggest features** - Share ideas for improvements
- 📝 **Improve documentation** - Make it easier for others to use
- 🔧 **Submit code** - Fix bugs or add new features
- 📊 **Add visualizations** - Enhance data presentation
- 🧪 **Add tests** - Improve code reliability
- 🎨 **Improve analysis** - Add new clustering algorithms or techniques

## 🚀 Getting Started

### 1. Fork the Repository

Fork the repository to your GitHub account and clone it locally:

```bash
git clone https://github.com/your-username/Customer-Segmentation-Analysis.git
cd Customer-Segmentation-Analysis
```

### 2. Set Up Development Environment

Create a virtual environment and install dependencies:

```bash
# Create virtual environment
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Install development dependencies (if available)
pip install -r requirements-dev.txt  # If exists
```

### 3. Create a Branch

Create a new branch for your feature or bug fix:

```bash
git checkout -b feature/your-feature-name
# or
git checkout -b fix/your-bug-fix
```

## 📋 Contribution Guidelines

### Code Style

- Follow PEP 8 style guide for Python code
- Use meaningful variable and function names
- Add comments for complex logic
- Keep functions small and focused

### Documentation

- Update README.md if you add new features
- Add docstrings to functions and classes
- Include comments in Jupyter notebooks
- Update requirements.txt if you add dependencies

### Commits

Write clear and descriptive commit messages:

```bash
# Good examples
git commit -m "Add K-Means clustering with optimal k selection"
git commit -m "Fix data preprocessing bug for missing values"
git commit -m "Update README with new visualizations section"

# Avoid
git commit -m "fix stuff"
git commit -m "updates"
```

### Pull Requests

1. **Update your fork** before creating a PR:
   ```bash
   git fetch upstream
   git merge upstream/main
   ```

2. **Test your changes** thoroughly

3. **Create a Pull Request** with:
   - Clear title describing the change
   - Detailed description of what and why
   - Reference to related issues (if any)
   - Screenshots for visual changes

4. **Respond to feedback** - Be open to suggestions and discussions

## 🐛 Reporting Bugs

When reporting bugs, please include:

- **Description** - Clear description of the issue
- **Steps to reproduce** - How to recreate the bug
- **Expected behavior** - What should happen
- **Actual behavior** - What actually happens
- **Environment** - OS, Python version, package versions
- **Screenshots** - If applicable

Example:

```markdown
**Bug**: Data preprocessing fails with missing values

**Steps to Reproduce**:
1. Load dataset with missing values
2. Run preprocessing function
3. Error occurs

**Expected**: Missing values should be handled gracefully

**Actual**: Script crashes with KeyError

**Environment**:
- OS: Windows 10
- Python: 3.9.7
- Pandas: 1.5.2
```

## 💡 Suggesting Features

When suggesting features, please include:

- **Use case** - Why is this feature needed?
- **Description** - What should it do?
- **Implementation ideas** - How might it work?
- **Alternatives** - Other approaches considered

## 🧪 Testing

- Test your code before submitting
- Include test cases for new features
- Ensure existing functionality still works
- Test with different data scenarios

## 📊 Adding New Analyses

When adding new clustering algorithms or analysis techniques:

1. **Document the approach** - Explain the algorithm
2. **Include visualizations** - Show results clearly
3. **Compare with existing methods** - Benchmark performance
4. **Add business interpretation** - Explain business value

## 🎨 Visualization Guidelines

- Use consistent color schemes
- Add clear labels and titles
- Include legends where appropriate
- Make visualizations publication-ready
- Use appropriate chart types for data

## 📝 Documentation Standards

### Code Documentation

```python
def calculate_rfm(df, customer_id, date, amount):
    """
    Calculate RFM (Recency, Frequency, Monetary) scores.
    
    Parameters:
    -----------
    df : pandas.DataFrame
        Input dataframe with customer transactions
    customer_id : str
        Column name for customer ID
    date : str
        Column name for transaction date
    amount : str
        Column name for transaction amount
        
    Returns:
    --------
    pandas.DataFrame
        DataFrame with RFM scores for each customer
        
    Example:
    --------
    >>> rfm_df = calculate_rfm(df, 'CustomerID', 'Date', 'Amount')
    """
    # Implementation
    pass
```

### Notebook Documentation

- Use markdown cells to explain analysis steps
- Include section headers
- Add context before code blocks
- Explain visualizations and findings

## 🔍 Code Review Process

1. **Automated checks** - CI/CD pipeline will run tests
2. **Maintainer review** - Project maintainer will review code
3. **Discussion** - Feedback and suggestions
4. **Approval** - Once all checks pass and changes approved
5. **Merge** - Changes merged into main branch

## ✅ Checklist Before Submitting PR

- [ ] Code follows project style guidelines
- [ ] All tests pass
- [ ] Documentation updated
- [ ] Commit messages are clear
- [ ] PR description is complete
- [ ] No merge conflicts
- [ ] Changes are focused and minimal

## 🌟 Recognition

Contributors will be:
- Listed in the project acknowledgments
- Credited in release notes for significant contributions
- Mentioned in relevant documentation

## 📧 Questions?

If you have questions:
- Open an issue for discussion
- Check existing issues and PRs
- Reach out to the maintainer

## 📜 Code of Conduct

Be respectful and professional:
- Be welcoming and inclusive
- Respect differing viewpoints
- Accept constructive criticism
- Focus on what's best for the project
- Show empathy towards others

## 🎓 Learning Resources

New to open source contributions? Check out:
- [GitHub Flow](https://guides.github.com/introduction/flow/)
- [How to Contribute to Open Source](https://opensource.guide/how-to-contribute/)
- [First Contributions](https://github.com/firstcontributions/first-contributions)

## 📦 Project Structure

```
Customer-Segmentation-Analysis/
├── Customer_Segmentation_Analysis.ipynb  # Main analysis
├── data/                                 # Data files
├── src/                                  # Source code (future)
├── tests/                                # Test files (future)
├── requirements.txt                      # Dependencies
└── README.md                             # Documentation
```

## 🚀 Development Roadmap

See [README.md](README.md#-future-enhancements) for planned features and enhancements.

---

Thank you for contributing to making this project better! 🙏

---

**Note**: By contributing, you agree that your contributions will be licensed under the same license as the project (MIT License).
