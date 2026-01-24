![Python Version from PEP 621 TOML](https://img.shields.io/python/required-version-toml?tomlFilePath=https%3A%2F%2Fraw.githubusercontent.com%2Fulgens%2Fuv-lock-check%2Fmain%2Fpyproject.toml)
![GitHub Actions Workflow Status](https://img.shields.io/github/actions/workflow/status/ulgens/uv-lock-check/lint.yml?label=lint)

# uv-lock-check
A pre-commit hook to validate pyproject.toml and uv.lock files are in sync

## Usage
Add the hook to your `.pre-commit-config.yaml`:

```yaml
  - repo: https://github.com/ulgens/uv-lock-check
    rev: v0.1.0
    hooks:
      - id: uv-lock-check
        language: python
        additional_dependencies:
          - uv==0.9.26
```

`additional_dependencies` definition is optional, but I recommend to match the uv version to your project's uv version, to ensure consistent results. `language: python` is necessary only if you want to make use of `additional_dependencies` and Renovate to update the dependency automatically: https://docs.renovatebot.com/modules/manager/pre-commit/#additional-dependencies

## Story
[The original inline version](https://github.com/ulgens/django-blasphemy/pull/690) of this hook was created with the help of https://til.unessa.net/git/pre-commit-hook/

## Contributing
This repo solves a very specific need, and I can't think of what could be added or improved. If you can think of any, please feel free to open an issue or a pull request.

## Similar Projects
- https://github.com/hbelmiro/uv-lock-check - A GitHub Action that validates if your uv.lock file and optionally requirements.txt files are in sync with your pyproject.toml file.

## Professional Support 📝
This repo is maintained as part of my ongoing work with CI tools. If your organization needs help with

- CI/CD pipeline design/improvements
- Dependency management automation
- Code quality and linting standards
- Backend development best practices

or other sort of assistance with a Python project, I'm available for consulting engagements. [Connect with me on LinkedIn](https://www.linkedin.com/in/ulgens/) and let's discover how I can help your team succeed!
