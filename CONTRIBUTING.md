# Contributing to Aion-Medsafety-AI

Thank you for your interest in contributing to Aion-Medsafety-AI! We welcome contributions from the community and are grateful for your help in making this project better. This document provides guidelines and instructions for contributing.

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [Types of Contributions](#types-of-contributions)
- [Getting Started](#getting-started)
- [Development Setup](#development-setup)
- [Contribution Workflow](#contribution-workflow)
- [Pull Request Process](#pull-request-process)
- [Review Process](#review-process)
- [Coding Standards](#coding-standards)
- [Commit Guidelines](#commit-guidelines)
- [Testing Requirements](#testing-requirements)
- [Documentation](#documentation)
- [Reporting Issues](#reporting-issues)
- [Contact](#contact)

## Code of Conduct

### Our Pledge

We are committed to providing a welcoming and inclusive environment for all contributors, regardless of age, body size, disability, ethnicity, gender identity and expression, level of experience, nationality, personal appearance, race, religion, or sexual identity and orientation.

### Expected Behavior

- **Be Respectful**: Treat all contributors with respect and courtesy.
- **Be Inclusive**: Welcome contributors of all backgrounds and experience levels.
- **Be Constructive**: Provide helpful feedback and criticism in a constructive manner.
- **Be Professional**: Maintain professional language and tone in all interactions.
- **Be Collaborative**: Work together toward common goals and solutions.

### Unacceptable Behavior

The following behaviors are considered unacceptable and may result in removal from the project:

- Harassment, intimidation, or bullying of any kind
- Discrimination based on protected characteristics
- Offensive comments or behavior
- Trolling or deliberate disruption
- Any form of abuse or threats
- Unwelcome sexual advances or attention

### Enforcement

Instances of unacceptable behavior may be reported to the project maintainers. All reports will be handled confidentially and investigated promptly. Contributors who violate the Code of Conduct may be temporarily or permanently banned from the project.

## Types of Contributions

We welcome various types of contributions:

### Bug Reports
- Report issues you've discovered
- Provide detailed descriptions and reproduction steps
- Include relevant system information
- Help us understand the impact and severity

### Feature Requests
- Suggest new features or improvements
- Explain the use case and benefits
- Provide examples or mockups if applicable
- Be open to discussion and refinement

### Code Contributions
- Fix bugs and implement features
- Improve code quality and performance
- Add tests and improve coverage
- Optimize algorithms and refactor code

### Documentation
- Improve README and guides
- Add API documentation
- Create tutorials and examples
- Fix typos and clarify existing docs

### Testing
- Write and improve unit tests
- Create integration tests
- Perform manual testing
- Report edge cases and regressions

### Code Review
- Review pull requests from other contributors
- Provide constructive feedback
- Help maintain code quality
- Share knowledge and best practices

## Getting Started

### Prerequisites

Before you begin, ensure you have:

- A GitHub account
- Git installed on your local machine
- Knowledge of the project's primary programming languages
- Familiarity with the project's goals and documentation

### Initial Setup

1. **Fork the Repository**
   ```bash
   # Visit https://github.com/AionSystem/Aion-Medsafety-AI
   # Click the "Fork" button in the top-right corner
   ```

2. **Clone Your Fork**
   ```bash
   git clone https://github.com/YOUR_USERNAME/Aion-Medsafety-AI.git
   cd Aion-Medsafety-AI
   ```

3. **Add Upstream Remote**
   ```bash
   git remote add upstream https://github.com/AionSystem/Aion-Medsafety-AI.git
   ```

4. **Verify Setup**
   ```bash
   git remote -v
   # Should show both 'origin' (your fork) and 'upstream' (main repo)
   ```

## Development Setup

### System Requirements

- Python 3.8 or higher
- pip or conda package manager
- Virtual environment support
- Git version 2.25 or higher

### Installation Steps

1. **Create Virtual Environment**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

2. **Install Dependencies**
   ```bash
   pip install -r requirements.txt
   pip install -r requirements-dev.txt
   ```

3. **Install Pre-commit Hooks**
   ```bash
   pre-commit install
   ```

4. **Verify Installation**
   ```bash
   python -m pytest
   python -m flake8 --version
   python -m black --version
   ```

### Development Tools

- **pytest**: Testing framework
- **black**: Code formatter
- **flake8**: Linting
- **mypy**: Type checking
- **coverage**: Test coverage analysis
- **pre-commit**: Git hooks management

## Contribution Workflow

### Step 1: Create a Feature Branch

```bash
# Update your local main branch
git fetch upstream
git checkout main
git merge upstream/main

# Create a new feature branch
git checkout -b feature/your-feature-name
# or for bug fixes:
git checkout -b fix/issue-description
```

### Step 2: Make Your Changes

- Keep commits focused and logical
- Write clear, descriptive commit messages
- Follow the project's coding standards
- Add tests for new functionality
- Update documentation as needed

### Step 3: Commit and Push

```bash
# Stage your changes
git add .

# Commit with a descriptive message
git commit -m "Brief description of changes"

# Push to your fork
git push origin feature/your-feature-name
```

### Step 4: Create a Pull Request

1. Visit your fork on GitHub
2. Click "New Pull Request"
3. Select your branch and the main repository's main branch
4. Fill in the PR template with:
   - Clear description of changes
   - Related issue numbers (if applicable)
   - Type of change (bug fix, feature, etc.)
   - Testing performed
   - Screenshots (if applicable)

### Step 5: Respond to Feedback

- Monitor your PR for comments and suggestions
- Respond constructively to feedback
- Make requested changes and push updates
- Keep the conversation professional and collaborative

## Pull Request Process

### Before Submitting

- [ ] Fork the repository
- [ ] Create a feature branch from main
- [ ] Make your changes with clear, logical commits
- [ ] Write or update tests
- [ ] Update documentation
- [ ] Run tests locally: `pytest`
- [ ] Run linters: `flake8 .`
- [ ] Format code: `black .`
- [ ] Run type checker: `mypy .`

### PR Template

```markdown
## Description
Brief description of the changes

## Type of Change
- [ ] Bug fix
- [ ] New feature
- [ ] Breaking change
- [ ] Documentation update

## Related Issues
Closes #(issue number)

## Testing Performed
Description of testing done

## Checklist
- [ ] My code follows the style guidelines
- [ ] I have performed a self-review
- [ ] I have added tests
- [ ] Tests pass locally
- [ ] I have updated documentation
- [ ] No new warnings generated
```

## Review Process

### Initial Review (1-3 days)

1. **Automated Checks**
   - CI/CD pipeline runs automatically
   - Code coverage is checked
   - Linting and formatting verified

2. **Maintainer Review**
   - Code quality and style assessment
   - Logic and functionality verification
   - Test coverage evaluation
   - Documentation review

### Feedback and Iteration

- Reviewers provide constructive feedback
- Contributors make requested changes
- Reviewers verify improvements
- Process repeats until approval

### Approval and Merge

- At least one maintainer approval required
- All CI checks must pass
- No conflicts with main branch
- Squash and merge or rebase merge strategy

### Post-Merge

- Automatic deployment may occur
- PR is closed and archived
- Branch may be deleted
- Contributor is credited

## Coding Standards

### Python Style Guide

- Follow [PEP 8](https://www.python.org/dev/peps/pep-0008/) guidelines
- Use 4 spaces for indentation
- Maximum line length: 88 characters (Black default)
- Use meaningful variable and function names

### Code Quality

```bash
# Format code
black .

# Check linting
flake8 .

# Type checking
mypy .

# Run tests
pytest -v --cov=.
```

### Best Practices

- Write clear, documented code
- Keep functions small and focused
- Avoid global state and side effects
- Use type hints for functions
- Handle errors gracefully
- Write defensive code

### Example

```python
"""Module docstring."""

from typing import List, Optional


def process_data(items: List[str], filter_empty: bool = True) -> List[str]:
    """
    Process a list of items.
    
    Args:
        items: List of string items to process
        filter_empty: Whether to filter empty strings
        
    Returns:
        Processed list of items
        
    Raises:
        ValueError: If items is None
    """
    if items is None:
        raise ValueError("items cannot be None")
    
    result = []
    for item in items:
        if filter_empty and not item.strip():
            continue
        result.append(item.strip())
    
    return result
```

## Commit Guidelines

### Commit Message Format

```
<type>(<scope>): <subject>

<body>

<footer>
```

### Types

- **feat**: New feature
- **fix**: Bug fix
- **docs**: Documentation changes
- **style**: Code style changes (formatting, missing semicolons, etc.)
- **refactor**: Code refactoring
- **perf**: Performance improvements
- **test**: Adding or updating tests
- **chore**: Build, dependencies, or tooling changes

### Examples

```
feat(auth): add two-factor authentication support

docs(readme): update installation instructions

fix(api): handle null responses gracefully

refactor(models): simplify data processing logic
```

### Best Practices

- Use imperative mood ("add feature" not "added feature")
- Don't capitalize first letter after type
- Limit subject to 50 characters
- Reference issues in body or footer
- Explain what and why, not how

## Testing Requirements

### Test Coverage

- Minimum 80% code coverage required
- New features must include tests
- Bug fixes should include regression tests
- All tests must pass before merge

### Running Tests

```bash
# Run all tests
pytest

# Run with coverage
pytest --cov=. --cov-report=html

# Run specific test file
pytest tests/test_module.py

# Run with verbose output
pytest -v

# Run specific test
pytest tests/test_module.py::test_function
```

### Test Structure

```python
"""Test module for feature."""

import pytest
from module import function


class TestFeature:
    """Test cases for feature."""
    
    def setup_method(self):
        """Set up test fixtures."""
        self.data = {"key": "value"}
    
    def test_basic_functionality(self):
        """Test basic functionality."""
        result = function(self.data)
        assert result is not None
    
    def test_error_handling(self):
        """Test error handling."""
        with pytest.raises(ValueError):
            function(None)
```

## Documentation

### README Updates

- Update if you change functionality
- Add examples for new features
- Keep it clear and concise
- Include setup instructions

### Code Comments

- Explain the "why" not the "what"
- Use docstrings for modules, classes, and functions
- Keep comments up-to-date
- Use clear, professional language

### Docstring Format

```python
def function(param1: str, param2: int = 5) -> bool:
    """
    Brief description of function.
    
    Longer description if needed. Explain the purpose,
    behavior, and any important details.
    
    Args:
        param1: Description of param1
        param2: Description of param2 (default: 5)
        
    Returns:
        Description of return value
        
    Raises:
        ValueError: When something is invalid
        TypeError: When type is incorrect
        
    Examples:
        >>> function("example", 10)
        True
    """
    pass
```

## Reporting Issues

### Finding Existing Issues

- Search for similar issues before creating a new one
- Check closed issues for workarounds
- Review pull requests for ongoing work

### Creating an Issue

Use the appropriate template and include:

**For Bug Reports:**
- Clear, descriptive title
- Detailed description
- Steps to reproduce
- Expected vs. actual behavior
- System information
- Screenshots/logs if applicable
- Related issues

**For Feature Requests:**
- Clear, descriptive title
- Detailed description
- Use case and motivation
- Proposed solution (if applicable)
- Alternative solutions
- Additional context

### Issue Labels

- `bug`: Something isn't working
- `feature`: New feature or enhancement
- `documentation`: Documentation improvement
- `good first issue`: Good for new contributors
- `help wanted`: Need assistance
- `in progress`: Currently being worked on
- `wontfix`: Not planned to be fixed

## Contact

### Getting Help

- **GitHub Issues**: Report bugs or request features
- **Discussions**: Ask questions and discuss ideas
- **Project Wiki**: Find documentation and guides
- **Email**: Contact maintainers directly if needed

### Code of Conduct Questions

If you have questions about the Code of Conduct or need to report a violation, please contact the project maintainers.

---

## Recognition

We appreciate all contributions and will recognize your work through:

- GitHub contributor badges
- Release notes credits
- Project documentation
- Community acknowledgment

Thank you for contributing to Aion-Medsafety-AI! Your efforts help make this project better for everyone.

---

**Last Updated**: January 2026

For the latest contribution guidelines, visit our [GitHub repository](https://github.com/AionSystem/Aion-Medsafety-AI).
