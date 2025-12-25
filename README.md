# uv-lock-check
A pre-commit hook to validate pyproject.toml and uv.lock files are in sync

## Usage

Add the hook to your `.pre-commit-config.yaml`:

```yaml
  - repo: https://github.com/ulgens/uv-lock-check
    rev: ""  # Update to latest tag with `prek (pre-commit) autoupdate`
    hooks:
      - id: uv-lock-check
        # additional_dependencies definition is optional, but I recommend you to match uv version
        # to your project's uv version, to ensure consistent results.
        additional_dependencies:
          - uv==0.9.18
```


## Contributing
This repo solves a very specific need, and I can't think of what can be added/improved but if you think it can be improved, please feel free to open issues or pull requests.

## Similar Projects
- https://github.com/hbelmiro/uv-lock-check - A GitHub Action that validates if your uv.lock file and optionally requirements.txt files are in sync with your pyproject.toml file.

## Professional Support 📝

These repo is maintained as part of my ongoing work with CI tools. If your organization needs help with

- CI/CD pipeline design/improvements
- Dependency management automation
- Code quality and linting standards
- Backend development best practices

or other sort of assistance with a Python project, I'm available for consulting engagements. [Connect with me on LinkedIn](https://www.linkedin.com/in/ulgens/) and let's discover how I can help your team succeed!
